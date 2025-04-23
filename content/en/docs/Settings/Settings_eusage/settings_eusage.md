---
title: "Settings > eUsage"
linkTitle: "eUsage"
date: 2024-11-15
weight: 100
tags: ["subtopic"]   
---

The eUsage application offers additional settings options. You can manage these settings in the eUsage section of the Settings app. 

## General

### Settings > General > Aggregators

An aggregator is a service that aggregates pre-processing statistics for multiple statistics providers and offers an endpoint to download the reports. eUsage allows you to harvest statistics for a usage data provider either directly from the provider via SUSHI or from an aggregator. Please note: The only aggregator service currently supported in FOLIO is the German National Statistics Server.

#### Add an aggregator

1. Open FOLIO's **Settings** app.
2. Choose the application **eUsage**.
3. In the **General** section click on **Aggregators**.
4. Click on the button **+ New**.
5. A new form opens where you have to enter the following data.

* **General information**
    * **Name** A freely selectable name for the entry. We recommend choosing the name of the aggregator.
    * **Service type** You can currently only select the German National Statistics Server in the selection list.
    * **Service URL** Enter the address for the end point here. Example: https://sushi.url-to-nss.de/Sushiservice/GetReport
* **Aggregator configuration** For German National Statistic Server you can specify the keys **apiKey**, **requestorId**, **customerId**, **reportRelease** by clicking on the button **Add config parameter**. To enter the values, there are the **key** and **value** fields as a pair. Every time you click the button **Add config parameter**, a new pair of fields appears. If you want to delete a pair, click the pair delete icon next to it.
    * **Key** = reportRelease and **Value** = 5
    * **Key** = apiKey and **Value** = *Your API key*
    * **Key** = requestorId and **Value** = *Your requestor ID*
    * **Key** = customerId and **Value** = *Your customer ID*
* **Account configuration**
    * **Type** Select the configurtion type between **Mail**, **API** and **Manual**.
    * **Mail** Here you can enter an email address.
    * **Contacts** You can add a contact as a short note by clicking on the button **+ Add contact**. Example: John Doe, Phone +49 0000 0000000. If you want to delete a line, click on the **Remove** button next to the contact's entry.

6. Then click **Save & close**.


#### Edit an aggregator

1. Open FOLIO's **Settings** app.
2. Choose the application **eUsage**.
3. In the **General** section click on **Aggregators**.
4. If you have entered one or more aggregator, they will be listed in the detailed view.
5. Click on the aggregator you want to edit.
6. The detail view for the aggregator opens.
7. Click on **Edit**.
8. You can make the changes.
9. Click on **Save & close**.


#### Delete an aggregator

1. Open FOLIO's **Settings** app.
2. Choose the application **eUsage**.
3. In the **General** section click on **Aggregators**.
4. If you have entered one or more aggregator, they will be listed in the detailed view.
5. Click on the aggregator you want to edit.
6. The detail view for the aggregator opens.
7. Click on **Edit**.
8. Click on **Delete**.
9. Confirm the question in the dialog **Delete aggregator** by clicking on the button **Submit**.


### Settings > General > Display settings

If you want, you can hide the display of SUSHI credentials in the detailed view for a usage data provider in the UI.

1. Open FOLIO's **Settings** app.
2. Choose the application **eUsage**.
3. In the **General** section click on **Display settings**.
4. In the detailed view of this setting you will find a checkbox **Hide sushi credentials in detail views**. If the checkbox is selected, the SUSHI credentials will be hidden in the UI.
5. Then click **Save**.


## Harvester

### Settings > Harvester > Number of failed attempts

If the automatic harvesting process fails, it will be restarted later. You can set a number of times the auto-scheduled harvest process can fail to fetch a report. If the specified number is exceeded, no attempt will be made to retrieve the report.

1. Open FOLIO's **Settings** app.
2. Choose the application **eUsage**.
3. In the **Harvester** section click on **Number of failed attempts**.
4. In the detailed view of this setting you will find a field **Number of failed attempts**. Here you can enter the maximum number of attempts as a number.
5. Then click **Save**.

If you want to change the setting, repeat the steps.


### Settings > Harvester > Start harvester

**Starting the harvester for all usage data providers** manually is an optional way. This can be done in the **Settings app**.

1. Open FOLIO's **Settings** app.
2. Choose the application **eUsage**.
3. In the **Harvester** section click on **Start Harvester**.
4. In the detailed view of this setting you will find a button **Start havester**. If you click on this button, the harvesting process for all usage data providers for the current tenant starts.
5. A dialog informs you that the a harvesting job has been successfully scheduled for immediate execution and the harvesting jobs usually take some time to complete. You can monitor the progress by checking the Harvesting jobs page.
6. Then click **OK**


### Settings > Harvester > Periodic harvesting

It is possible to use a automatic harvesting process to retrieve reports continuously from providers. You can set the interval for the automatic harvesting process. This can be done in the **Settings app**. Please note: You can only use one interval.


#### Add a new interval

1. Open FOLIO's **Settings** app.
2. Choose the application **eUsage**.
3. In the **Harvester** section click on **Periodic harvesting**.
4. In the detailed view of this setting you will find at the first time no entries, but the explanation how you can add an interval for the periodic harvesting.
5. Click **+** to define periodic harvesting.
6. A new form opens where you have to enter the following data.
* **Start Date** the day on which the interval should first start. The automatic harvesting process then starts after the specified interval, which is set under **Periodic interval**.
* **Start time** the time on which the interval should first start. The automatic harvesting process then starts after the specified interval, which is set under **Periodic interval**.
* **Periodic interval** the interval for the automatic harvesting process.
    * Daily
    * Weekly
    * Monthly
* **Last triggered at** informs you about the last started automatic harvesting job. Example: **September 12, 2024 3:01 AM**. If no interval has been started before, you see **--**.
7. Then click **Save**.


#### Edit an interval

1. Open FOLIO's **Settings** app.
2. Choose the application **eUsage**.
3. In the **Harvester** section click on **Periodic harvesting**.
4. In the detailed view of this setting you can see your current interval, if it has been set.
5. Click on the **editing icon** at the top right of the detailed view.
6. The form in which you entered the data for the interval opens.
7. You can edit your entries.
8. Then click **Save**.


#### Delete an interval

1. Open FOLIO's **Settings** app.
2. Choose the application **eUsage**.
3. In the **Harvester** section click on **Periodic harvesting**.
4. In the detailed view of this setting you can see your current interval, if it has been set.
5. Click on the **editing icon** at the top right of the detailed view.
6. The form in which you entered the data for the interval opens.
7. Click on **Delete**.
8. Confirm the question **Delete periodic harvesting config?** by clicking on the **Submit** button.


### Settings > Harvester > Harvester logs

In this setting you can specify how many days the harvester will keep the logs.

1. Open FOLIO's **Settings** app.
2. Choose the application **eUsage**.
3. In the **Harvester** section click on **Harvester logs**.
4. In the detailed view of this setting you can see the field **Number of days to keep harvesting logs** where you can enter the number for the days as a number. 
5. Then click **Save**.

If you want to change the setting, repeat the steps.
