# Airflow-tutorial
Orchestration:-To automate repeatitive task in data pipelines hence,we use Airflow.
s3->Cleaned Date->s3->Transformed Date ->Redshift

Interval based:-(Schedule 9:am| every 4 hours)
Event Based:-(Arrival File |API call)
Manual Trigger

Why not Airflow?
Not a Data Processing Engine.
Not a Data Streaming Tool.
Not a GUI based Tool.
Should not used for short lived tasks-causes overhead due to logging data.
Not to be used real time data prcessing.

Features
Organization
Visibility
Flexible
Scaling

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

MetaDataBase:store the state of DAGs tasks and other execution metadata
Scheduler:schedules DAG and store task statuses
Web Server:-fetches execution logs and history
Executor:-store task execution results
Plugins:-store custom metadata

Executor:-assigns task to Works to execute as per scheduler(local-not for production,sequential,celery,kubernetes-autoscaling)
Scheduler:receives tasks to execute
Workers:execute task in a distributed execution models as directed by executor
Queues:-retrieve tasks to execute
Logs:-store task execution logs
Config Files:-uses configuration for execution behaviour

![image](https://github.com/user-attachments/assets/01f0a9bc-b49a-4ad1-b5d0-1cece889479e)






