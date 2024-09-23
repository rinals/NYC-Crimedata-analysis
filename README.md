## Real estate price range prediction using NYPD crime data
NYPD Crime data provides severity, nature and precise location of recorded crimes. This can be used to train a machine learning model that predict real estate pricing range.

## Crime data
NYPD Crime data contains details like:
1. Time
2. Location - latitude, longitude
3. Severity - violation, Misdemeanor, felony, etc.
4. Nature of crime - drugs, robbery, homicide, violent offense, etc.
5. Suspect age
6. Victim age

## Real estate data
1. Home details (beds, batsh, sq footage, etc.)
2. Home price
3. Location (longitude, latitude)

## ETL
Will transform data from NYPD Crime database and real estate pricing to match location, area, crime information.

## Machine learning
Transformed data will be split into training and test, to train a model using supervised learning techniques.
The model will then be able to predict home price range based on input data:
1. home type (2 bed, 2 bath, etc.)

