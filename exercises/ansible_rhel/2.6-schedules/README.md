# Exercise - Schedules

## Table Contents

* [Objective](#objective)
* [Guide](#guide)
* [Create a Schedule](#create-a-schedule)

## Objective

Demonstrate the use of Ansible Tower [schedule feature](https://docs.ansible.com/ansible-tower/latest/html/userguide/scheduling.html). 

## Guide

If you remember on excercise 2.3 you created an "Install Apache" job template, one of the playbook tasks on that template was to ensure that firewalld was installed and enabled on all hosts. Now we are going utilize a schedule to run this job template on regular basis. This is what you're going do:

* Create a schedule for the **Install Apache** template.


### Create a Schedule

Now you need to create a new schedule for the **Install Apache** template.

#### Create Notification Template

* Go to the **Install Apache** job template, click the schedules button.

* Fill out the following information:

<table>
  <tr>
    <th>Parameter</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>NAME</td>
    <td>Firewall Enable</td>
  </tr>
  <tr>
    <td>START DATE</td>
    <td>Today</td>
  </tr>
  <tr>
    <td>START TIME</td>
    <td>Now</td>
  </tr>
  <tr>
    <td>LOCAL TIME ZONE</td>
    <td>Europe/London</td>
 </tr>
  <tr>
    <td>REPEAT FREQUENCY</td>
    <td>Hour</td>
  </tr>
   <tr>
    <td>EVERY</td>
    <td>1</td>
  </tr>
   <tr>
    <td>END</td>
    <td>Never</td>
  </tr>
</table>

* Click **SAVE**

After about 1 hour you should see a notification from the Ansible Tower bot in Slack that the job has started, and another message when it finishes.

Feel free to edit the timings on the schedule to test this feature. 

---
**Navigation**
<br>

[Click here to return to the Ansible for Red Hat Enterprise Linux Workshop](../README.md)
