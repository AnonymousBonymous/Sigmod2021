# Sigmod2021

Accepts the following program arguments:
- manditory: path to JSON file where each row is a JSON record
- optional: log {outputFileName} (outputs renamed log file)
- optional: kse 1.0 (set key-space entropy to double value, ommit to disable collection rewriting)
- optional: train 10.0 (set training size to 10% of the input file size, must be double)
- optional: val 1000 (set number of rows to reserve for validation to 1000, must be int)
- optional: seed 23 (set seed of random split to 23)
- optional: merge bimax (set merge algorithm to bimax(default) options are: {bimax,subset,verbose})

 example:
 sbt run data/yelp.json log yelp.log kse 1.0 train 20.0 val 3000 seed 11
 
 Log files output 2 rows per run, the fist being the config options, the second being a json-schema for the data set.
 This format can then be read and validated using https://github.com/AnonymousBonymous/SIGMOD2021-Validator
 
 Thanks!
