# Exercise - Notifications

**Read this in other languages**:
<br>![uk](../../../images/uk.png) [English](README.md),  ![japan](../../../images/japan.png)[日本語](README.ja.md), ![brazil](../../../images/brazil.png) [Portugues do Brasil](README.pt-br.md), ![france](../../../images/fr.png) [Française](README.fr.md), ![Español](../../../images/col.png) [Español](README.es.md).

## Table Contents

* [Objective](#objective)
* [Guide](#guide)
* [The Apache-configuration Role](#the-apache-configuration-role)
* [Create a Template with a Survey](#create-a-template-with-a-survey)
  * [Create Template](#create-template)
  * [Add the Survey](#add-the-survey)
* [Launch the Template](#launch-the-template)
* [What About Some Practice?](#what-about-some-practice)

## Objective

Demonstrate the use of Ansible Tower [notifications feature](https://docs.ansible.com/ansible-tower/latest/html/userguide/notifications.html). A Notification is a manifestation of the notification template; for example, when a job fails, a notification is sent using the configuration defined by the notification template.

## Guide

You have installed Apache on all hosts in the job you just ran along with a survey. Now we’re going to ensure notifications when this job is successfully ran are sent into a slack chat. This is what you're going do:

* Create a notification template.

* Assign a notification template to the Template we just created in the previous excercise.

* Launch the job **Template**

* View a notification in the "general" slack channel.


### Create a Notification template

Now you create a new notfication template.

#### Create Notification Template

* Go to **Notifications**, click the ![plus](images/green_plus.png) button/

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

{% if page.url contains 'ansible_rhel_90' %}
[Previous Exercise](../1.4-variables) - [Next Exercise](../../ansible_rhel_90/6-system-roles/)
{% else %}
[Previous Exercise](../2.3-projects) - [Next Exercise](../2.5-rbac)
{% endif %}
<br><br>
[Click here to return to the Ansible for Red Hat Enterprise Linux Workshop](../README.md)
