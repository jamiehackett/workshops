# Exercise - Notifications

## Table Contents

* [Objective](#objective)
* [Guide](#guide)
* [Create a Notification Template](#create-a-notification-template)
* [Create a Template with a Survey](#create-a-template-with-a-survey)
  * [Add the Notification](#add-the-notification)
* [Launch the Template](#launch-the-template)

## Objective

Demonstrate the use of Ansible Tower [notifications feature](https://docs.ansible.com/ansible-tower/latest/html/userguide/notifications.html). A Notification is a manifestation of the notification template; for example, when a job fails, a notification is sent using the configuration defined by the notification template.

## Guide

You have installed Apache on all hosts in the previous job combining that with a survey. Now we’re going to ensure a notification is sent into a slack channel when this job is successfully ran. This is what you're going do:


> **Note**
>
> **For the purposes of todays workshop, we have already created the Slack bot needed for notifications to be sent from Ansible Tower.**



* Create a notification template.

* Assign a notification template to the Job Template we just created in the previous excercise.

* Launch the job **Template**

* View a notification in the "general" slack channel.

### Join the slack channel 

For this example to work, please join the slack channel using this link: https://join.slack.com/t/esbansibleworkshop/shared_invite/zt-o9rzheld-cVKeNUTCqWZJLfVSqiddsQ 



### Create a Notification template

Now you create a new notfication template.

#### Create Notification Template

* Go to **Notifications**, click the plus green button.

* Fill out the following information:

<table>
  <tr>
    <th>Parameter</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>ORGANIZATION</td>
    <td>Default</td>
  </tr>
   <tr>
    <td>NAME</td>
    <td>Slack alert</td>
  </tr>
  <tr>
    <td>TYPE</td>
    <td>Slack</td>
  </tr>
  <tr>
    <td>DESTINATION CHANNELS</td>
    <td>#general</td>
  </tr>
  <tr>
    <td>TOKEN</td>
    <td>Ask in the google meet chat for the token.</td>
</table>

* Click **SAVE**

> **Warning**
>
> **Do not run the template yet!**

#### Add the Notification

* Click into a job template that you've previously created - for example Install Apache, click the **NOTIFICATIONS** button

* On the right side of **Slack Alert** tick the following boxes:
* START
* SUCCESS
* FAILURE


### Launch the Template

Now launch **Install Apache** job template.

After launching you should see a notification from the Ansible Tower bot in Slack that the job has started, and another message when it finishes.

---
**Navigation**
<br>
[Previous Exercise](../2.4-surveys) - [Next Exercise](../2.6-schedules)

[Click here to return to the Ansible for Red Hat Enterprise Linux Workshop](../README.md#section-2---ansible-tower-exercises)
