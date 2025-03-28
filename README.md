# AWS CSPM with Qualys TotalCloud Integration

This repository demonstrates how to implement Cloud Security Posture Management (CSPM) for an AWS account using Qualys TotalCloud. The solution leverages Qualys' cloud-native security capabilities to continuously assess, monitor, and remediate misconfigurations and compliance violations in your AWS environment.

By connecting your AWS account to Qualys TotalCloud via a Cloud Connector, this setup enables automated scanning and visibility into your cloud infrastructure. The repository includes step-by-step instructions, sample configurations, and scripts to help you integrate Qualys TotalCloud with your AWS account, ensuring a secure and compliant cloud environment.

<h2>Key Features:</h2>
Automated CSPM Scanning: Continuously monitor your AWS resources for misconfigurations and compliance issues.

Cloud Connector Integration: Step-by-step guide to connect your AWS account to Qualys TotalCloud.

Remediation Guidance: Identify and resolve security gaps with actionable insights provided by Qualys.

Compliance Reporting: Generate compliance reports for industry standards like CIS, GDPR, and more

# Qualys Set up
<h3>create an account on Qualys</h3>
- go to <a href="https://www.qualys.com/">Qualys</a>
- click 'try now'> free trials> totalcloud 2.0 

![Image](https://github.com/user-attachments/assets/c0642f59-b9be-4229-9117-e3585b664b36)
- complete the free account form

  ![Image](https://github.com/user-attachments/assets/025e9a18-01c5-4e31-8bcf-d5dcabb2b01b)
- site requires using a work email. sign up for bugcrowdninja to receive free work email

![Image](https://github.com/user-attachments/assets/53bd6573-82b0-4b2f-a168-0fd4554b27fd)
- click bugcrowd home link on website> "hackers" under the hamburger/menu icon> 'start today' link> complete the sign up form

![Image](https://github.com/user-attachments/assets/a4354e75-0c20-4c00-9efc-d5301ab1b916)
- check your email

  ![Image](https://github.com/user-attachments/assets/86136862-9956-456f-9a96-04242b97c9d3)
  - log back into bugcrowd> to Account settings> profile, then update the username. your email address is now 'username'@bugcrowdninja.com
  - now back to Qualys and use the new email to complete the sign up form> use any dummy phone number
 
![Image](https://github.com/user-attachments/assets/08d06b5b-1732-4ded-a8ec-6682be70b554)
- check your personal email for the Qualys trial activation

![Image](https://github.com/user-attachments/assets/ab5323e1-6064-4202-a017-7af5296c04ee)
- and the second email containing your username and OTP

![Image](https://github.com/user-attachments/assets/dbcdaefd-be43-42f2-9b76-d1eb0eabe140)
- click 'activate your account' link in the email and enter the OTP

![Image](https://github.com/user-attachments/assets/cecf96ab-c6af-4ac7-a9ff-17aac59cbfc7)
- you will then be provided with a password and the login URL> copy password and click the URL> sign in and accept Service Agreement> and now create new password

![Image](https://github.com/user-attachments/assets/ba412ae2-5ed7-41d1-a2b5-e89a8afbc390)
- now log into Qualys

![Image](https://github.com/user-attachments/assets/cf819d9c-ca31-463f-9820-ea6953c28477)
- select TotalCloud from dropdown

![Image](https://github.com/user-attachments/assets/21760953-c938-4192-9771-3461ca22bb3f)

![Image](https://github.com/user-attachments/assets/9f891589-4e87-470d-b4a2-bf416a0b0d8c)

# Create an AWS profile
- log into your existing AWS account or create a <a href="https://aws.amazon.com/free/?gclid=Cj0KCQiAlbW-BhCMARIsADnwaspO8i986yG0D4XdFCOsR7gJqPp9MAmMN26Z8HKg3Kn4762WLOcp6T0aApCxEALw_wcB&trk=78b916d7-7c94-4cab-98d9-0ce5e648dd5f&sc_channel=ps&ef_id=Cj0KCQiAlbW-BhCMARIsADnwaspO8i986yG0D4XdFCOsR7gJqPp9MAmMN26Z8HKg3Kn4762WLOcp6T0aApCxEALw_wcB:G:s&s_kwcid=AL!4422!3!432339156165!e!!g!!aws%20free%20tier%20account!9572385111!102212379047&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all">free tier</a> account

![Image](https://github.com/user-attachments/assets/5cc88a93-4403-47b9-93d8-96d7aa02b2dd)
# Connect Qualys TotalCloud to your AWS account
- select 'Configure Connector Now'

![Image](https://github.com/user-attachments/assets/bb384058-7a27-4466-b2f3-ebfc6e8e0d82)
- select AWS

![Image](https://github.com/user-attachments/assets/e0538a6f-1760-4c99-affc-c1502732a84c)
- next, select 'Launch Stack'> accept the defaults and click'Create stack'

![Image](https://github.com/user-attachments/assets/0bb2ace8-f8d4-4093-896a-4e1c5898c25e)

![Image](https://github.com/user-attachments/assets/5944fc13-0570-4d23-bb0f-14d9e9c1b733)
- we will need the Role ARN from AWS

![Image](https://github.com/user-attachments/assets/1b85f10e-b964-4187-96d2-691338600f48)
- search for the stack in IAM roles. select it and copy the role ARN

![Image](https://github.com/user-attachments/assets/35d02417-f1ef-4ad0-99d6-ad5dc8083d93)

![Image](https://github.com/user-attachments/assets/90a28ca8-84aa-4391-9e39-e8f47495e25c)
- enter the Role ARN in Qualys and select next> test the connection

![Image](https://github.com/user-attachments/assets/8123cd8a-b4bd-4dd2-94b4-ed65ce20a467)
- select TotalCloud from dropdown again to get to the dashboard

![Image](https://github.com/user-attachments/assets/2cce3359-1ec8-4ca0-b874-62c25dc5a12d)
- select configure tab (on left-hand side)> check the AWS connector> Manage Connectors> select AWS connector and 'run connector' from the Actions drop-down, select yes

![Image](https://github.com/user-attachments/assets/e5e450f1-8b01-4d59-8fa5-6a22df3dd2c4)
- see the scan results> select the back arrow> TotalCloud> Posture

![Image](https://github.com/user-attachments/assets/33c6c480-55b5-4333-8f20-b9bdad1ed54f)
- 116 Controls evaluated  and 346 failures> select any failed Control Name and you will see the steps for remediation

![Image](https://github.com/user-attachments/assets/81bab2f9-7ad7-441d-a546-7db76e1c81ca)
- example on how to create a false-positive exception> select a failed Control Name> check the Actions drop-down and select Create Exception

![Image](https://github.com/user-attachments/assets/3a53d196-f674-43a3-85d4-6b7113619d22)
- this allows you to perform remediations for the items needed and to create exceptions for any false positive results based on the organization's standards
# Next steps
- complete all the needed remediations and rerun the scan. I hope these steps were useful!
