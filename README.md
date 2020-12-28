# Multi-Classification-Problem: Predict wind turbine downtime


The Darwin platform, Engie Digital’s software suite dedicated to renewable energies, would like to provide Darwin users, at the moment where a wind turbine stop occurs, with an estimation of the probable duration of this stop (downtime). 

One underlying business need is that, when a stop occurs on a wind turbine, discussions start between the wind farm operator and the energy aggregator; the operator provides iteratively information on the expected downtime. This process is often manual; it would be worth automating this process and improving reliability in downtimes duration estimation. 

Some additional details

There are many reasons that may lead to a wind turbine stop. We usually classify stops in three categories: “planned”, “unplanned”, and “external”. Planned events refer to stops that have been anticipated beforehand; such as a planned maintenance or a site visit. External events refer to stops whose cause is not controllable, such as lighting strikes or wind gusts. Unplanned events refer to all other types of stops, and especially include breakdowns.

###  Data description: 
For this challenge we provide you with data recording all unplanned stop events since 2017 on a series of wind turbines. 

Train data file:

File containing logs from 2017 to 2019, describing each downtime for each wind turbine. The Duration_categoriesis the column we want to predict; the categories have been mapped into numbers for computing a metric, but behind the numbers are the following stopping times categories:
<=30 minutes: 1
]30 minutes-3hours]: 2
]3 hours-24 hours]: 3
]24 hours-7 days]: 4
> 7 days: 5
Turbines names MAC_CODE have been anonymized, but consistently refer to the same wind farm when relevant.
You are also given Duration column, as it is more precise than Duration_categories and could possibly help for training ; but it does not exist in the test file and we want to predict Duration_categories.
