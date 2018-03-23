# Tutorial scenario and prerequisites

This tutorial introduces you to the key features of Operational Decision Manager on IBM Cloud Private \(ODM on IBM Cloud Private\). Prepare for the tutorial by reviewing its objectives and prerequisites.

In this tutorial, you work in the Decision Center Business console to update a decision service that a loan company uses to determine whether borrowers are eligible for loans. The fictitious company makes changes to its loan policies, and you must reflect the changes in the decision service.

The tutorial uses a simple decision service that has only one project. The rules are grouped into two folders in the project:

|Folder|Description|
|------|-----------|
|eligibility|These rules determine whether the loan can be approved.|
|validation|These rules make preliminary checks to determine whether data is rejected immediately.|

As you go through the tutorial, you will log in as two different users to get a feel of the collaborative work that takes place in the Business console. The two users log in with different user names:

-   odmAdmin: A manager who initiates, reviews, and deploys changes.
-   rtsUser1: A rule author who implements the change.

## Prerequisites

Do the following steps before you start the tutorial:

-   Install ODM on IBM Cloud Private \(ODM for developers or ODM for production\), and note the URL of your instances of the Decision Center Business console and the Decision Server console.
-   Review the product overview to understand the main goals of the product, some of its modules, and rule-oriented terminology.
-   Download the Getting Started for ODM on IBM Cloud Private sample project from the [ODMDev GitHub repository](https://odmdev.github.io/#/odm) by clicking **Clone or download** \> **Download ZIP**. Create a new folder called GettingStartedDirectory on your computer, and extract the project into this new folder. You will need both the zipped and the extracted version of the sample project to perform this tutorial.
-   \(optional\) Install the cURL command-line tool to perform [Step 3 \(optional\): Testing the execution of the ruleset using curl](../gs_topics/tut_icp_gs_test_ruleset_lsn.md#step-3-optional-testing-the-execution-of-the-ruleset-using-curl).

## Best practices

This tutorial includes the following best practices:

-   Use the Business console to follow changes to rules, especially when you assign work to other people.
-   Create a snapshot of a branch before modifying it. You can use the snapshot for comparisons or to rollback the branch.
-   Post comments for other users. The comments can direct work and serve as part of the history of changes.
-   Use the search feature to find rule artifacts.
-   Test a rule set for REST execution in the Decision Server console.
-   Delete projects from the databases when you no longer use them. [**Next** ![Next icon](../gs_images/next.jpg)](../gs_topics/tut_icp_gs_evaluate_changes_lsn.md)

[![](../gs_images/home.jpg) **Back to table of contents**](../README.md)

