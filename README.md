Rally-RQM-Toolkit
=================

This is a series of apps which support Rally's test functions and provide test status iteratively and per release.

This toolkit is comprised of many different RQM-enhancing apps which could comprise 5+ custom pages in Rally for a test group.

Please note these apps are really only valid for progress on the current iteration or release. They can look back at tests included in past iterations but results and progress will not be available.  They can also be used to verify planned tests for an upcoming iteration or release.  Percent complete on release MAY be off by a percentage point or 3 depending on how many tests are re-used, as the Last Result verdict is the only one used for the release-focused apps.

The apps can be grouped into three categories:

Scheduled Test Case tables:

Scheduled Test Case List per Iteration - no Summary:  This app lists all test cases scheduled for the Iteration in a tabular format, including columns for if the test was newly created this iteration, its last run date, last verdict, test method, project, associated work product, work product state, and more.  Pulls all tests assigned to test sets, defects, and stories for a given iteration.
Scheduled Test Cases per Iteration with Summary: This app is the same as the item above but adds a textual summary of the iteration test progress, including items like test counts, automated and manual breakdowns, percent pass/fail, and percent complete.
Scheduled Test Cases per Release - no Summary: This app is the same as the iterative app (as listed above) with the tabular data output of all tests scheduled for the release.
Scheduled Test Cases per Release with Summary: This app is the same as the iterative app (as listed above) which includes the tabular output as well as detailed textual release summary.

Iteration Table Screenshot:<P>
![Alt text](https://github.com/jkrooswyk/Rally-RQM-Toolkit/raw/master/Screen Shot - Iterative Test List 1.0.png)

Test Case Summaries:

Test Case CUMULATIVE Summary per Iteration: This app represents progress for the current iteration in a graphical manner, with a CSS-based % done bar for important test data such as tests executed to date (number and % complete), tests remaining, passing tests, failing tests, other results (blocked, etc), and a breakdown of work product associations.  Creating a test dashboard using the 3 graphical apps (Cumulative, Automated, and Manual) makes for a nice view into the iteration. 
Test Case CUMULATIVE Summary per Release: This app is the same as the iterative summary app listed above, but is around the release.  The colors for the release app are darker than that of the iteration app to help distinguish.  As with the iterative apps, putting the 3 release apps together makes a nice view into the release status. 
Test Case AUTOMATED Summary per Iteration: Same as the Cumulative iterative app, but filters for the automated tests.
Test Case AUTOMATED Summary per Release: Same as the Cumulative release app, but filters for the automated tests.
Test Case MANUAL Summary per Iteration: Same as the Cumulative iterative app, but filters for the manual tests.
Test Case MANUAL Summary per Release: Same as the Cumulative release app, but filters for the manual tests.

Test Summaries Screenshot:<P>
![Alt text](https://github.com/jkrooswyk/Rally-RQM-Toolkit/raw/master/Screen Shot - Release Progress Dashboard 1.0.png)

CSV-exportable Test table with steps:

Exportable Test Cases with Steps - Chrome, FF: This app presents an iterative table with the test steps.  It is exportable to CSV, which downloads within Chrome.  Note the limitations, since this uses Data URLs - no single quote, double quote, or commas are allows in test names or export will fail. Firefox has a habit of assigning random names to downloaded files!
Exportable Test Cases with Steps - Explorer, any other browser: This app is the same as listed above, except for any browser - since not all browsers support downloads of Data URL files the same way, this app presents the CSV in a web page for copy and paste into an actual file, which can be saved and used with Excel.  Same limitations apply around quotes and commas in test name fields.