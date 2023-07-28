# EAR (Event aggregator)

## Note and Disclaimer
This project has been recently started and is not production ready. If you find this interesting and want to contribute in completing this to be production ready please join us and let me know.

## What is EAR?
The EAR is a light weight rule engine for aggregating events based on the defined rules in it. The basic usage of this project in for OLAP purposes and we want to create some meaningfull data based on our operations in parallel but in a reasonable time (near real time reports for a finite time).

## EAR usages
EAR is manily for analytic data preparation for
- Finding the kpi for different parts of our system
- Have required data for decision making
- Finding bottlenecks in the system
- Finding bugs in our flows

## How EAR works?
EAR have an endpoint for getting the events and saving them into its database. We define some rules for aggregating the events and creating meaningfull and usefull data to our business in a table and we could focus extracting our data just from one single point of truth.

## EAR rule structure
EAR input rule file format is in json format. We have 2 types of rule in our system (Current time)
- Single rule
This rule define aggregation based on the defined duration in the database. The event in this scenario is single and there is no related event to that.
- Bundle rule
This rule define aggregation of events based on related events. We have a core event that starts the bundle and then we have some other events that the aggregation is based on them.

## Architecture
![image](https://github.com/goldenreflection/ear/assets/20452906/daac176d-b70a-48b4-a6a3-0fba1ea11634)

