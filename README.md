# autoscaling-load-balancing-Cloudwatch
configure auto scaling and Load balancing, Cloudwatch log


configure auto scaling, LB, Cloudwatch log

Step 1:- Create Ec2 Instance and attach cloudwatch

Step 2:- Create Cloud watch alarm from aws cloud watch
➔ Visit the CloudWatch console and choose ALARM under Alarms.
➔ Choose Create alarm.
➔ Choose Select metric and then ec2 in that By Auto Scaling Group then select the auto-scaling group id which you want to trigger and for CPU Utilisation.

➔ Select Select metric to continue.

Step 3:- Specify metric and conditions

➢ Under Statistics, choose a statistic or a predefined percentile, or specify a custom percentile (for example, p95.45).
➢ Under Duration, select the evaluation period for the alarm. When evaluating an alarm, each period is aggregated into a single data point.
➢ Whenever there is a metric for , specify whether the metric should be greater than, less than, or equal to the limit. Less than, specify a threshold value.

Step 4:- Configure actions

➢ Under Notification, choose an SNS topic to be notified when there is an alarm in the ALARM STATUS, OK STATUS, or INSUFFICIENT_DATA STATUS.
➢ To have an alarm send multiple notifications for the same alarm status or for different alarm conditions, select Add notification.
➢ Here you can select an existing SNS topic or create a new topic or you can use topic ARN to notify other accounts.
➢ if you create new topic you need to give topic name & Email endpoints that will receive the notification then create topic.

Step 5:- If you do not want to send notifications to the alarm, select Remove.
➢ To have the alarm perform Auto Scaling, EC2, or System Manager actions, select the appropriate button and select the alarm status and action to perform. Alarm system managers can perform actions only when they go into the alarm state.

Step 6:-Add name and description
➢ Enter a name and description for the alarm.
➢ Under Preview and Create, confirm that the information and conditions are the ones you want, then select Create alarm.

Now we want to create a CloudWatch alarm for an instance:
You can create a CloudWatch alarm that monitors CloudWatch metrics for one of your instances. When the metric reaches the limit you specify, CloudWatch will automatically send you a notification.

You can create a CloudWatch alarm using the Amazon EC2 console or by using the more advanced options provided by the CloudWatch console.

To create an alarm using the Amazon EC2 console

Step 7:-Open the Amazon EC2 console

Step 8:-In the navigation pane, select Instances, choose Action, Monitor and troubleshoot, Manage CloudWatch alarms.

Step 9 : On the Manage CloudWatch alarm details page, under Add or edit alarms, select Create alarm.

Step 10 : For alarm notification, choose to turn the toggle on or off to configure Amazon Simple Notification Service (Amazon SNS) notifications. Enter an existing Amazon SNS topic or enter a name to
create a new topic.Step 11 : For alarm action choose to turn the toggle on for Specifying the action to take when the alarm is triggered.

Step 12 : Choose Create

➔ Now when your threshold reaches the value you will get
notification to your email and the instance will be terminated or it will be rebooted or stopped which you have specified.
