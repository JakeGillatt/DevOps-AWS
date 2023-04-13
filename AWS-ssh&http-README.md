# Setting up a virtual Linux environment in AWS and connecting with SSH
#
# Once you are logged into the AWS platform:
#
- In the top search bar, search 'EC2' and select EC2 - Virtual Servers in the Cloud
#
- Under 'Launch instance' select Launch instance
#
- Enter a name for the instance and in the 'Application and OS Images' section
locate and select Ubuntu Server 22.04 LTS(HMV) 64-bit(x86)
#
- Select the Key pair name from the dropdown 'tech221.pem'
#
- Select 'Create security group' and allow SSH traffic from 'My IP'
#
- Check the box to 'Allow HTTP traffic'
#
- View the summary and 'Launch instance' once all steps are complete
#
- Head to 'Instances' and click on the Instance ID code
#
- Select the 'Instance state' box and start the instance
#
- Wait for the 'Instance state' to confirm that it's Running
#
- Now tick the box to select the instance and select the 'Connect' box. Then select the 'SSH client' section
#
- Now in git bash, within the .ssh directory where the key file is located, 
connect to the instance using its public DNS - Example: `ssh -i "tech221.pem" ubuntu@ec2-34-245-60-35.eu-west-1.compute.amazonaws.com`
#
- Enter 'yes' if prompted
#
- You are now connected to the Linux Instance.
#
# If you need to edit the security groups rules or add new rules:
#
- On your Instance summary window, scroll down and select the 'Security' tab next to Details.
#
- Click the 'Security groups' code link
#
- Now select 'Actions' drop down tab and select 'Edit inbound rules'
#
- You can now 'Add rule' and Delete rules. Select Add rule to add a new rule, 
choose the rule type you want and then under 'Source type' select 'My IP' and save the changes
