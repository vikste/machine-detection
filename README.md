# Machine detection from behavior

## About the data

On today's networks, there not only humans. Many machines also use it. The IoT devices for instance.

The operators have a huge interest in recognizing this machines to increase the QoE, to detect the fraudulent use of SIM and to design new data plan.

This dataset is made with various metrics from EEA about user's behavior. For example, there is information about the video usage, the ARPU level, the use of iMessage...

It also comes with a label that identify the humans and the machines.



## Challenge

The goal of this project is to build a classifier able to identify the machines among the users using only the information about their behavior.



## About the files

### train_set.csv

This file is the main dataset that you should use for the challenge. There are 175 123 rows in the file. Every row is a different user that can be a human or a machine.

There are 97 columns. 96 of them are the metrics that you should be used by your classifier.

The column called 'type', identifies the machines. In this column, a user is either labeled as 'Machine' or as 'Mobile phone' (= human). This is your goal label.



### test_set.csv

In order to accurately compare the models, all of the teams will test their models on the same dataset. This is the purpose of this file.

This file has the same columns than **train_set.csv**. It contains 19 479 users that are not in **train_set.csv**. You must use it to evaluate the performances of your model.



### features_description.csv

This file is documentation. It describes every columns of **train_set.csv** and **test_set.csv**. For every feature there is :

* the feature name (attribute)
* the data type (data_type)
* a description of the feature



For instance:

| attribute    | data_type | description                           |
| ------------ | --------- | ------------------------------------- |
| arpu_grp_eea | String    | ARPU level based on ARPU for an IMSI  |
| type         | String    | Nature of the IMSI (human or machine) |
| sli_mms_eea  | Double    | MMS SLI over time for an IMSI         |



