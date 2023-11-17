# Oscar Prediction

## Datasets
This folder contains the data for the prediction of Oscar winners. The data is not complete yet and will be updated later.

The `oscar_data.csv` was created by Raphael Fontes and David Lu which can be found on [GitHub here](https://github.com/DLu/oscar_data/blob/main/oscars.csv). 
This dataset includes information about Oscar nominees and winners from the 1st to the 95th Academy Awards. Here is the list of the variables and a brief description:


| Header       | Description                              | Data Type |
| ------------ | ---------------------------------------- | --------- |
| `Ceremony` | Ordinal for which ceremony the nomination was for (starting at 1)| int |
| `Year` | Year(s) from which the films are honored | string |
| `Class` | A custom broad grouping for categories. Values include: Title, Acting, Directing, Music, Production, SciTech and Special | string |
| `CanonicalCategory` | Removes the variations on the exact wording of the category name over the years | string |
| `Category` | The precise category name according to Oscars.org | string |
| `NomId` | Unique string representing the IMDb Nomination ID | uuid |
| `Film` | The title of the film (optional) | string |
| `FilmId` | Unique string representing the IMDb Title ID | uuid |
| `Name` | The precise text used for who is being nominated | string |
| `Nominees` | The names of who is nominated in a comma separated list (without any extra text like "Written by") | comma separated strings |
| `NomineeIds` | Unique strings (or question marks) representing the IMDb Name ID | comma separated uuids |
| `Winner` | True if the award was won | bool |
| `Detail` | Detail about the nomination, which could be the character name, song title, etc. | string |
| `Note` | Additional information provided about the award/nomination | string |
| `Citation` | Official text of the award statement, for Scientific/Technical/Honorary awards | sring |
| `MultifilmNomination` | Generally the data is one nomination per row, but for certain early nominations (Ceremonies 1, 2, 3 & 8), people were nominated for multiple films, and so one nomination could be spread over multiple rows | bool |


According to this dataset, Mate Varadi compiled data for predicting the Oscars, incorporating additional variables that may influence Oscar votes. The dataset includes the six Oscar awards people are most concerned about: Best Picture, Best Director, Best Actress, Best Actor, Best Supporting Actress, and Best Supporting Actor. He added variables encompassing Genre, MPAA rating, IMDB score, Rotten Tomatoes Critics and Audience scores, total number of nominations, number of previous nominations and wins, as well as the nominations and results of Oscar precursor award ceremonies, including BAFTA, Golden Globe, Critics Choice Award, Screen Actors Guild Award, Directors Guild of America Award, and Producers Guild of America Award. The original data can be [found here](https://github.com/MateVaradi/OscarPrediction/tree/main/data). I selected datasets specifically covering Oscar winners from 1961 to 2022, see `oscardata_acting`, `oscardata_bestdirector` and `oscardata_bestpicture`.
