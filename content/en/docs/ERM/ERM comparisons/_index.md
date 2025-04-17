---
title: "ERM comparisons"
linkTitle: "ERM comparisons"
date: 2024-12-06
weight: 15
tags: ["parenttopic"]
---

The ERM comparisons app is used to compare the contents of two different packages or agreements to check whether there are any overlaps in content.

Definition of terms related to the ERM comparisons app:

* **Comparison.** A record that compares the contents of two collections of e-resources (agreements or packages) and as a result shows, which titles are contained in which set and whether titles in the collections overlap or not.
* **Package.** A collection of e-resource titles bundled together as a unit and distributed by a provider.
* **Agreement.** An agreement outlines the content your library can access.

## Permissions

The Capability sets listed below allow you to interact with the ERM comparisons app and determine what you can or cannot do within the app. You can assign Capability sets to users in the section **Authorization roles** of the Settings app. 

The following are the ERM comparisons Capability sets:

* **UI-Erm-Comparisons Jobs.** Choose **View**, **Edit**, and **Delete**. The Capability set allows the user to view, create and delete existing comparisons.

The following Capability sets are also needed to create a comparison:

* **UI-Agreements Agreements.** Choose **View**. The Capability set allows the user to search and view existing agreements. This also allows the user to see and access the Agreements app in the FOLIO interface.
* **UI-Agreements Resources.** Choose **View**. The Capability set allows the user to search and view e-resources (packages and titles in those packages) in the internal KB.

## Creating a comparison

1. In the **ERM comparisons** pane, click **New**.
2. Select a name.
3. Add as a first comparison point either a package or an agreement to the comparison.
4. Select a date. All titles that where an active component of the collection on this date are included in the comparison. The current day is preset by default.
5. Add as a second comparison point either a package or an agreement to the comparison.
6. Select a date. All titles that where an active component of the collection on this date are included in the comparison. The current day is preset by default.
7. Once you have included all of the information you want about the comparison, click **Save & close**. A confirmation message appears, and the comparison is saved and appears in the comparison pane. The comparison will start automatically.

## Searching for a comparison

You can search for a comparison in the **Search & filter** pane. To search for comparisons, enter your search terms in the search box and click **Search**. It will be searched for the name of the comparison.

You can also search for comparisons by selecting any of the filters in the **Search & filter** pane. Additionally, you can apply the filters before or after you perform a search via search box to limit your results. See the sections below for more information.

###  Running status

To filter comparisons by their status, select one of the following:

* **Ended.** The comparison of the two comparison points is finished. The outcome/result can be checked.
* **In progress.** The comparison of the two comparison points is currently running.
* **Queued.** The comparison of the two comparison points has not started yet. It will be automatically started at some point.

### Result

To filter comparisons by their result, select one of the following:

* **Failure.** The comparison of the two comparison points was not successful. The comparison report is empty.
* **Interrupted.** The comparison of the two comparison points was interrupted.
* **Partial success.** The comparison of the two comparison points was partially successful.
* **Success.** The comparison of the two comparison points was successful. A comparison report can be viewed. The report only contains titles if at least one of the two comparison points contained titles.

### Comparison point 1 & 2

To filter for comparisons that contain specific packages or the components of a specific agreement, select one or both of the following:

* **Select agreement.** Select an existing agreement from the Agreements app.
* **Select package.** Select a package from the internal KB.

## Viewing a comparison

Once you search for a comparison, the following information appear in the ERM comparisons pane:

* **Name.** The name of the comparison.
* **Running status.** The running status of the comparison.
* **Outcome.** The outcome of the comparison as soon as the running status is set to *ended*.
* **Errors.** The number of errors that occured during the comparison.
* **Started.** The time and date the comparison process started.
* **Ended.** The time and date the comparison process ended.

In the search results, click a comparison to view it. The **comparisons details** pane displays the following additional information:

* **Comparison report.** The listing of the compared titles with the information in which comparison point the titles are and whether they overlap or not.
* **Comparison points.** The listing of the e-resouce collections (agreements and/or packages) that were being compared.
* **Error log.** An error log will be shown if the comparison was not successful.
* **Info log.** An info log will be shown if the comparison was not fully successful.

## Viewing a comparison report

To view a comparison report, click on the comparison whose report you would like to view. In the **comparisons details** pane, click **View comparisons report**. The report displays the following information:

* **Title.** The title of each e-resource that is whether in one or the other or both packages, shown in alphabetical order.
* **Available via.** The name of the platform of the specific e-resource and a link to the e-resource on this platform.
* **Coverage.** If available, the start date and/or end date of the e-resource. Coverage is typically only displayed for e-Journals.
* **Agreement/Package #1 on MM/DD/YYYY.** The first comparison point with the name of the package or agreement and date of the comparison. The field will display a check mark circled in green if the comparison point contains the e-resource and an X circled in red if the comparison point does not contain the e-resource.
* **Agreement/Package #2 on MM/DD/YYYY.** The second comparison point with the name of the package or agreement and date of the comparison. The field will display a check mark circled in green if the comparison point contains the e-resource and an X circled in red if the comparison point does not contain the e-resource. 
* **Overlap.**
  * **None.** The e-resource does not overlap. The title is only found in one of the comparison points. No overlap will be displayed in a red color.
  * **Full.** The e-resource overlaps. The title including its metadata is found in both comparison points. Full overlap will be displayed in a green color.
  * **Partly.** The e-resource is partly overlapping. The title is found in both comparison points but with differentiating metadata, e.g. the coverage or plattform-URL. Partly overlap will be displayed in an orange color.

## Deleting a comparison

1. Find the comparison you want to delete.
2. In the **comparisons details** pane, click **Actions > Delete**.
3. In the **Delete comparison** dialog, click **Delete**. A confirmation message appears and the comparison is deleted.
