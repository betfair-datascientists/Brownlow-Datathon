# Betfair Australia Brownlow Datathon

## Aim
This repo aims to educate participants of the Betfair Brownlow Datathon on creating an end-to-end model to use in the competition. Whilst some coding experience is required to be able to follow the modelling workthrough, there are no restrictions on the tools you can use to complete the task - even Microsoft Excel should be powerful enough to create a competitive model!

## The Task
This repo will outline how the Betfair Data Scientists went about modelling the AFL Brownlow for the 2018 season. The task is: to provide a prediction for the number of Brownlow Votes each player will receive in the 2019 AFL season. We have included a dataset named 'brownlow_datathon_data.csv' which contains player level data from the 2010 to 2019 AFL seasons. You are not required to use this data, however if you choose to use your own dataset, please ensure that the player names in your submission match the ones that we provided.

The metric used to determine the winner will be the [Mean Squared Error](https://en.wikipedia.org/wiki/Mean_squared_error) over all predictions, based on the actual Brownlow votes received compared to predicted Brownlow Votes redeived. For example, the Betfair Data Scientists' Brownlow Model predicted Tom Mitchell to poll <img src="https://latex.codecogs.com/gif.latex?35.48" title="35.48" /> votes last season, while he only actually polled 28. Thus, the Squared Error for this individual prediction would was <img src="https://latex.codecogs.com/gif.latex?(35.48&space;-&space;28)^2&space;=&space;56.04" title="(35.48 - 28)^2 = 56.04" />. On the other hand, if our model had correctly predicted <img src="https://latex.codecogs.com/gif.latex?28" title="28" /> votes, the Squared Error would have been <img src="https://latex.codecogs.com/gif.latex?0" title="0" />. The winner of the datathon will be the partcipant with the lowest Mean Squared Error over all predictions.

For a detailed outline of the task, the prizes, and to sign up, click [here](https://www.betfair.com.au/hub/betfairs-brownlow-medal-datathon/).

To read how we went about modelling the 2018 Brownlow, read [this](https://github.com/betfair-datascientists/predictive-models/tree/master/brownlow).

## Prizes:
| Place         | Price         | 
| -             | -             | 
| 1             | $2000         | 
| 2             | $1000         |   
| 3             | $750          |   
| 4             | $500          |    
| 5             | $250          |   
| 6-10          | $100          |   
| Total         | $5100         |   

## Submission
To submit your model, email your final submission to datathon@betfair.com.au by 5.59pm AEST on 23 September 2019. Please rename the CSV to what you would like to call your model (this could be displayed on a leaderboard). Note that you don't need to email your code, just your predictions in the format that we have specified in the ‘Betfair Brownlow Datathon Submission.csv’. Any submissions that are not in the correct format will not be accepted.

Submissions should include a prediction for the number of votes each player will receive. We will assume a prediction of <img src="https://latex.codecogs.com/gif.latex?0" title="0" /> votes for any missing values and Mean Squared Error will be calculated accordingly. Please ensure player names are in the specified format, otherwise we will be unable to find you prediction and, once again, we will assume a prediction of 0 votes. Here is an example of what a submission would have looked like for a sample of 25 players in the 2018 season...

### Team_Betfair.csv
| PLAYER | PREDICTION |
| - | - |
| T Mitchell | 35.484614 |
| M Gawn |	21.544278 |
| D Martin |	20.444488 |
| B Grundy |	19.543511 |
| C Oliver |	19.009628 |
| J Macrae |	18.931594 |
| P Dangerfield |	18.621242 |
| D Beams |	17.621222 |
| E Yeo |	16.015638 |
| L Neale |	15.495083 |
| A Gaff |	15.165629 |
| D Heppell |	15.083797 |
| J Selwood |	14.989096 |
| S Sidebottom |	14.863136 |
| N Fyfe |	14.692243 |
| J Kennedy |	14.404489 |
| Z Merrett |	13.632131 |
| M Crouch |	13.503858 |
| R Laird |	13.274869 |
| P Cripps |	13.240568 |
| G Ablett |	13.01895 |
| L Franklin |	12.792476 |
| J Lloyd |	12.174224 |
| J Kelly |	11.982157 |
| C Ward |	11.892443 |

And here is how this sample would have been scored...

### Team_Betfair_MSE.csv
| PLAYER | PREDICTION | ACTUAL | SE |
| - | - | - | - | 
| T Mitchell | 35.484614 | 28 | 56.01944673 |
| M Gawn | 21.544278 | 20 | 2.384794541 |
| D Martin | 20.444488 | 19 | 2.086545582 |
| B Grundy | 19.543511 | 17 | 6.469448207 |
| C Oliver | 19.009628 | 13 | 36.1156287 |
| J Macrae | 18.931594 | 14 | 24.32061938 |
| P Dangerfield | 18.621242 | 17 | 2.628425623 |
| D Beams | 17.621222 | 18 | 0.143472773 |
| E Yeo | 16.015638 | 15 | 1.031520547 |
| L Neale | 15.495083 | 11 | 20.20577118 |
| A Gaff | 15.165629 | 16 | 0.696174966 |
| D Heppell | 15.083797 | 13 | 4.342209937 |
| J Selwood | 14.989096 | 14 | 0.978310897 |
| S Sidebottom | 14.863136 | 24 | 83.48228375 |
| N Fyfe | 14.692243 | 16 | 1.710228371 |
| J Kennedy | 14.404489 | 4 | 108.2533914 |
| Z Merrett | 13.632131 | 10 | 13.1923756 |
| M Crouch | 13.503858 | 8 | 30.29245288 |
| R Laird | 13.274869 | 19 | 32.77712497 |
| P Cripps | 13.240568 | 20 | 45.68992096 |
| G Ablett | 13.01895 | 14 | 0.962459103 |
| L Franklin | 12.792476 | 16 | 10.28821021 |
| J Lloyd | 12.174224 | 6 | 38.121042 |
| J Kelly | 11.982157 | 10 | 3.928946373 |
| C Ward | 11.892443 | 13 | 1.226682508 |
| - | - | - | - | 			
| MSE | - | - | 21.09389949 |

If you are happy to read through the Python tutorials on Github, but not run the code yourself, you can click [here](https://github.com/betfair-datascientists/predictive-models/blob/master/brownlow/Betfair%20Data%20Scientists'%20Brownlow%20Model.ipynb). If you are keen to try and run the code yourself and try different things out, you will need to install the following:

Python
Jupyter Notebook (Installed through the Anaconda Distribution)
If you don't already have Python installed, we advise you to install it through [Anaconda](https://www.anaconda.com/download/). This also installs Jupyter and is super convenient.

## Disclaimer
Note that whilst predictions are fun and rewarding to create, we can't promise that your betting strategy will be profitable. If implementing your own strategies please gamble responsibly and note that you are responsible for any winnings/losses incurred.

## FAQs:

- some of the players are missing. i.e. there is only one listing of A Brayshaw, when there should be two Brayshaws.

Player names are in the format {firstname initial}{surname} as some small merging of datasets was required to create the dataset for this competition. This means some players with identical names are not uniquely identifed. Don't worry about providing a submission for these players; you can provide a prediction or no prediction at all and you will not be penalised as we will have to exclude these players from scoring. However, do not make changes to the submission file to try and distinguish between these players.
