# AWS AMIs
#
# What is an AMI?
AMI stands for Amazon Machine Image. It's a virutal machine image that is essentially a backup of an 
Instance/Virtual machine. If an Image is accidentally terminated, an AMI can be used to re-launch the image in its 
previous state.
With an AMI, you can re-launch an EC2 instance in seconds, rather than having to install and configure
the operating system and other software manually. It can also be used for version control.
They can also be used to create multiple copies of the same Instance.
#
# AMI Diagram:
![AMI_Diagram.png](AMI_Diagram.png)
#
# Creating the AMI
- At the AWS Instances list, select the instance you wish to create an AMI of.
- Select the Actions dropdown box and select 'Image and templates' -> 'Create image'
- Name the image, e.g - 'jake_tech221_nginx_AMI'
- Add a description for the Image
- Review the image options and select 'Create image'
- The AMI will now take a minute to generate
#
# Re-launching an Instance from an AMI
- Once the AMI status is 'Available':
- Select your instance and from the 'Instance state' dropdown box, select 'Terminate instance'
- Head back over to the 'Images -> AMIs' section and select your AMI from the list
- Now select 'Launch instance from AMI'
- Name the Instance and select the 'Key pair name' e.g - tech221
- Select 'Existing security group' and select your security group from the dropdown
- Now select 'Launch instance' at the bottom
- Go back to the Instances list and wait for your instance state to show 'Running'
- You can now connect to the instance
- Note: When logging into the instance, the username 'root' may need changing to the correct username