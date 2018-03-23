# Task 2: Creating and editing rules

In this task, you learn how to search for rules, modify a decision table, and create an action rule in the Business console.

Decision Center enables business experts to develop and deploy decision services. Distributed business teams can collaborate through the web-based environment to create and maintain the decision logic. Decisions can evolve as required by the immediate needs of the business without putting an extra load on the development of the application that calls it. With this separation, decisions and application architecture can be managed asynchronously. For example, developers can develop a new version of a decision service in response to changing application infrastructure and core business requirements, and business experts can work on new decisions that are delivered in response to an evolving market or a changing regulatory environment.

In this task, the company wants to make changes to its loan policies and your task is to reflect these changes in the Miniloan project. The changes to the loan approval policies that you must make are:

-   The length of a loan cannot be shorter than 6 months. You will add a check to all incoming requests for loans to make sure this policy is taken into account.
-   The company wants to increase the minimum credit score from 200 to 300 for all new loan requests.

## Step 1: Searching for rules

You do a search to find the rules in the decision service that handle the credit score.

1.   Log in to the Business console by using `rtsUser1` as the user name and password. In the **What's New** section of the home tab, rtsUser1 sees the post from odmAdmin.
2.   Open the **Library** tab.
3.  Hover over the Miniloan Service box, and click anywhere except the name to expand it. Then click **main** under **Recently updated branches** to open the **main** branch. 
4.   In the **Search for rules** field, type score, and press Enter.The results show all the action rules and decision tables in which the word score occurs. You look at all the rules, and conclude that you must edit the **repayment and score** decision table.

## Step 2: Modifying a decision table

You start by checking the history of changes to this decision table, and then you edit the rule. You make a mistake and correct it.

1.   Click **repayment and score** to display the decision table. 
2.   Click **Timeline**. The history of changes for the decision table shows that no changes have been made recently.
3.   Click **Exit Timeline**. 
4.   Click **Edit**. 
5.   Double-click the number `200` in row 1 of the **credit score** column and enter the value 300. Do not change this value in row 2 yet.
6.   Click **Details** and change the status to **Defined**. Rule properties may be used for different purposes in Decision Center, such as the organization and workflow, permissions, testing, and deployment.
7.   Close the property window. 
8.   Click **Save**. 
9.   Type the comment Changed credit score to 300, and click **Create New Version**. The decision table now displays v1.1. Decision Center creates a new version for all changes. The major version number 1 is assigned to the main branch. Any new branch, including the branches of the governance framework, take the next available number. The minor version number corresponds to the number of changes made in the branch.

## Step 3: Correcting an error

You check the decision table and find an error. You correct the error, save your work, and leave a comment about the error correction.

1.   Hover over one of the fields with a gold triangle in the table. It shows an overlap error:

 ![Image shows the error message displayed when you hover the gold triangle](../gs_images/scrn_classic_dterror.jpg)

2.   Click **Edit** to reopen the table. 
3.   Double-click the credit score condition for row 2, change the value 200 to 300, and press Enter. This change eliminates the overlap in rows 1 and 2. 
4.   Click **Save**. 
5.   In the Create New Version window, type the comment Fix for gap error and click **Create New Version**. 

## Step 4: Creating a new action rule

You implement the policy that the length of a loan cannot be shorter than 6 months.

1.   Click **main** in the breadcrumbs below the top banner to return to the contents of the branch. 
2.   Open the validation folder, which contains the rules for validating loan data. 
3.   Click the **Add** button ![Image shows the Add button](../gs_images/icon_merge_create_plus.jpg) button, and then click **New Rule**. 
4.   Type the name check duration, and click **Create**. 
5.   Copy and paste the following rule into the rule editor, or build the rule with the completion menu \(see the [Rule editor flash demo](http://public.dhe.ibm.com/software/websphere/techexchange/WODM/intellirule_viewlet_swf.html) on the IBM® Customer Support site for an English-only tour of the rule-editing features\). 
    
    if
          the duration of 'the loan' is less than 6
    then
          add "The duration of the loan is too short" to the messages of 'the loan';
          reject 'the loan';
    

6.  Click **Details** and change the status to **Defined**.
7.  Close the property window.
8.   Click **Save**. 
9.   Type Added for Summer policy, and click **Create New Version**. 
10.  Click the **HOME** tab, and then **Stream**, and respond to odmAdmin by typing the following message in the comment box below odmAdmin's post: 
    
    Hi odmAdmin. I'm all done!
    

11.  Click **Post** and then log out of the Business console. You finished the updates.

In the next task, you test and deploy the decision service. [**Next**![Next icon](../gs_images/next.jpg)](../gs_topics/tut_icp_gs_test_deploy_lsn.md)

[![](../gs_images/home.jpg) **Back to table of contents**](../README.md)

