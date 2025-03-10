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
- check your personal emai for the Qualys trial activation

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
