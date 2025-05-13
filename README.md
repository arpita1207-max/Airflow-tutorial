# Airflow-tutorial
1. Orchestration:-To automate repeatitive task in data pipelines hence,we use Airflow.
   
s3->Cleaned Date->s3->Transformed Date ->Redshift

2. Scheduler Type
1.Interval based:-(Schedule 9:am| every 4 hours)
2.Event Based:-(Arrival File |API call)
3.Manual Trigger

4. Why not Airflow?
   
1.Not a Data Processing Engine.
2.Not a Data Streaming Tool.
3.Not a GUI based Tool.
4.Should not used for short lived tasks-causes overhead due to logging data.
5.Not to be used real time data prcessing.

Features

1.Organization

2.Visibility

3.Flexible

4.Scaling

5.WebServer

WebServer :-Acts as a frontend UI for mointorning,triggering & managing DAG and tasks in Airflow.
Scheduler:-to display DAG Status
Meta Database:- to fetch DAG execution plan
Logs:- To display logs for DAGs and Task
Plugins:-For extending UI functionalities

Purpose:-Continuously mointor DAGs determine which task to trigger task execution
MetaData :-To fetch DAG execution status &definition
Executor:-To send task for execution
Trigger:-To handle deferred task
Sensors:-To mointor external dependencies
Queues:-To send task for execution

6.MetaDataBase

MetaDataBase:store the state of DAGs tasks and other execution metadata
Scheduler:schedules DAG and store task statuses
Web Server:-fetches execution logs and history
Executor:-store task execution results
Plugins:-store custom metadata

7.Executor

Executor:-assigns task to Works to execute as per scheduler(local-not for production,sequential,celery,kubernetes-autoscaling)
Scheduler:receives tasks to execute
Workers:execute task in a distributed execution models as directed by executor
Queues:-retrieve tasks to execute
Logs:-store task execution logs
Config Files:-uses configuration for execution behaviour

![image](https://github.com/user-attachments/assets/01f0a9bc-b49a-4ad1-b5d0-1cece889479e)


8. Variables

Variable Name:-Key
Variable Value:-Value

Variable Type

1.String Type ex-max_record_to_process ->value=1000
2.Json Type-{"name':"arpita","city":"Lucknow"}

Benefits of using variables:
1.Implementing made easy
2.enviroment specific
3.security
4.Dynamic DAG

Masking Keywords
access_key
authorization
access_api
password
private_key
token,secret


Connections
connections are configuration objects  they store data required to connnect to external systems.
connection_id
connection_type
hostname
port
username
password

Benefits of Connection

1.Reusuability and Maintability
2.Enviroment specific
3.Implementing changes made easy
4.Security
