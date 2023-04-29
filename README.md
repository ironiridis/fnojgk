# fnojgk
A CloudFormation template for your sensible multi-account infrastructure

## Elevator Pitch
Your AWS infrastructure should be organized in a hierarchy of accounts in an AWS Organization.
You should have an account for each well-delineated workload, as well as a separate account for each of your public Route53 zones, if any.
Your application source code should be in version control. Repos to accounts should map approximately `1:n`, where `n` is the number of distinct environments you have.
Assuming you're using Git, you should have one branch per environment. This could be as simple as `prod` and `test`.
Each repo (in each environment branch, of course) should contain a CloudFormation template that defines how the app is built and defined.

This tool helps you create that structure through generating a CloudFormation template that reflects the design.
It makes opinionated choices that may not be right for everyone, but in general the choices are safe, cost effective, and sensible.

