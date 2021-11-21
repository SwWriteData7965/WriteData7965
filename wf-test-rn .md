

*Hi! Here is a document that you need to review. Please convert this document to*

*Markdown using the editor of your choice (Atom, Sublime Text, etc.). Then, submit*

*your Markdown file to github.com. To do this, you may need to create an account*

*and a repository. Note that the repository needs to be public so we can review*

*your work.*

**Version 10.2**

**RELEASE DATE**

October 30, 2020

The new Intelligent Automation Cloud v.10.2 provides you with a set of innovations to increase

productivity and simplify your routine work. The release includes, but is not limited to, the

following features:

• **WorkSpace 2.0** is a human-in-the-loop tool designed to tackle various issues with the

exception-handling process, allowing faster completion and improving compliance.

Compared to the previous version, WorkSpace 2.0 is strengthened with a feature that

enables you to manipulate and adjust the workflow.

• With the new **A/B testing** feature, you can validate automation variations, review

Analytics dashboards for test results, and choose the most confident automation

version, thus improving performance of the pre-trained bots.

• **Automated retraining** allows you to start retraining on a collected training set, know the

estimated duration, and see analytics for validating models. The bot retraining workflow

becomes even more friendly to business users, now available in the Control Tower UI.

• **Centralized user management and role-based access control** are introduced to rule all

the ecosystem components, including Analytics dashboards and WorkSpace.

• **Analytics** introduces 20 new data points, drill-down capability, improved navigation, and

simplified, user-friendly analysis.

• **Intelligent Automation Cloud Developer** updates include the new Launcher application

for components management and other improvements to your local development

environment.

• **ML SDK** extensions address complex problems including (but not limited to) Hybrid

Models, Grouping, and Classification Cascade training.

• **Optimized orchestration** of services allows you to reduce hardware requirements to 11

servers for a high-availability environment.

• Additional bug fixes, improvements, and deprecations address user requests and solve

earlier flaws.

For more information on each improvement, see detailed descriptions below.





**A/B-testing of Use Cases**

The A/B testing functionality enables you to easily test adjustments or new versions of

automation and gather key metrics to determine whether to implement these changes in the

production environment.

The intuitive workflow makes the whole procedure easy to run, with data available for

comparison after actual testing.

With the help of A/B tests, you can perform the following:

• Safely run historical or live data through a new version without impacting the original

version.

• Manage variations of business processes to be tested.

• Test updated manual task efficiency and routing.

• Automatically gather data to measure and compare two different versions.

• Analyze business metrics and compare versions.

**Bug Fixes**

**Infrastructure**

• Fixed an issue with Logstash startup failing and secrets not taken from Secrets Vault.

• Fixed a bug with inoperative jobs when cloning from the current directory.

• Fixed a certificate error causing Logstash not to start.

• Fixed an issue with the "Run postmigrate SQL script" step.

• Fixed an issue with the Ports Prechecker not working when the FirewallD service blocks

ports.

• Fixed an issue with the update\_artifacts task failing when running on the HA

environment.

• Fixed a Liquibase error when upgrading.


