# aws-ssm-automation-create-ami
This repository contains an Amazon Systems Manager automation document to create an AMI and tag it with the input parameters.

**This document requires following parameters as an input**
  1. InstanceId - _InstanceId of your EC2 instance for which AMI is to be created_
  2. AMINameKey - _Tag key of AMI Name. default is "Name"_
  3. AMINameValue -_ Meaningful name of the AMI_ 
  4. DeleteOnKey - _Default is "DeleteOn". You can use this tag key to used as a filter to delete older AMIs as per your data policy_
  5. DeleteOnValue - _This can be date in some defined format e.g. "DD-MM-YYYY" on which AMI deletion logic can be built._
  6. NoReboot - _AWS SSM Automation will create AMI with reboot or without reboot based on this value. By default it is "false"_


This SSM Automation document will help you to performance two operations in a single API if executed from your program.
1. Create AMI of the instance
2. Tag AMI created in #1
