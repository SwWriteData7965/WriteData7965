

Hi! Here is a document that you need to review. Please convert this document t[o](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

[Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)[ ](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)[u](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)sing the editor of your choice (Atom, Sublime Text, etc.). Then,

submit your Markdown file to [github.com](https://github.com/)[.](https://github.com/)[ ](https://github.com/)To do this, you may need to create an

account and a repository. Note that the repository needs to be public so we can

review your work.

If you feel that some edits are a matter of style, follow th[e](https://developers.google.com/style/)[ ](https://developers.google.com/style/)[Google](https://developers.google.com/style/)[ ](https://developers.google.com/style/)[Developer](https://developers.google.com/style/)[ ](https://developers.google.com/style/)[Style](https://developers.google.com/style/)

[Guide](https://developers.google.com/style/)[,](https://developers.google.com/style/)[ ](https://developers.google.com/style/)or just leave your considerations as a comment. Thank you, and good luck!

—————

**Bot Tasks** contain work to be done by WorkFusion’s bots. These bots perform the

steps in your Business Process, which are more suited for automation than human

labor. Bot Tasks can exist only as a Business Processes step.

For example: address parsing, determining the width and height of an image,

interacting with your API or repository, or filtering content that does not meet

certain criteria.

**Bot Configs** are written using Web-Harvest Library and are executed for each

record separately. When writing Web-Harvest XML configs, you can use pre-

defined Web-Harvest XML elements described here, or use WorkFusion plugins.

**Bot Config Bundle** is a bundled java library containing a bot config and a java code

reference that can be used in this bot config.

**How to Create, Test, and Run**

\1. Create and test a Web-Harvest config using the WorkFusion Studio (Eclipse-

based IDE).

\2. Create a Bot Use Case in WorkFusion. Choose the Bot Use Case type. **Note:** ETL is

the best practice, as it accommodates reusability and adds flexibility.

\3. Create a BP and include a Bot Step based on this Use Case. Alternatively,

you can use WorkFusion Repository to import a Bot Config Bundle into WorkFusion.

\4. Test the Bot Config in BP using a small input batch.

\5. If needed, make changes to column names, use proxy, datastore connection,

and output column names.

\6. Update the created Bot Use Case and use it in your production BP.

Alternatively, you can create a Bot Task in BP (Design Process tab) from scratch

(Blank Use Case) and paste your code. However, this approach leads to multiple issues.

**Execution Details**

XML configuration is executing for each submission. If your input CSV file contains

40 records, the Web-Harvest XML configuration executes 40 times, once per record.

If any errors occur, the Bot Config runs five times.

**Results**

The results of a Bot Task are defined in the <export> plugin settings.

All the columns the Bot Task creates can be used in further BP steps (both

manual and bot).

**Hello World Example**

In the following example, the bot performs these steps:

\1. Gets the HTTP response from URLs listed in the input data file's **url\_to\_check** column.

\2. Records the HTTP response in the **http\_response** variable.

\3. Exports all original columns and appends a new **http** column containing the

**http\_response** variable value.

**Bot Config Example**

<?xml version="1.0" encoding="UTF-8"?>

<config>

<!--defining variable-->

<var-def name="http\_response">

<!--passing the appropriate value from url\_to\_check column in input data file

as a parameter for http plugin-->

<http url="${url\_to\_check}"></http> </var-def>

<!--exporting all original input columns-->

<export include-original-data="true">

<!--adding a new column with the http plugin result to the export file-->

<single-column name="http" value="${http\_response}"/> </export>

</config>


