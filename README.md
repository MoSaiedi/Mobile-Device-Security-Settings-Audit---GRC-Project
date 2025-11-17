# Mobile-Device-Security-Settings-Audit---GRC-Project
Project viewable Google Sheets Link https://docs.google.com/spreadsheets/d/1mt9w0w9amc_rqPSwpNNFMV7b3ftF9Kfqg6BDlN2c1i0/edit?usp=sharing

YouTube Video walking through the project: https://youtu.be/oJ-okWl4114

This project is a security settings audit I conducted on a configuration profile used on a large group of iPads being managed via Jamf MDM. In this project I show the pre audited security settings, post audited security settings, and pre and post audited risk register. 

Note: This project is derived from an actual mobile-device security audit I performed. To protect client confidentiality, all device counts, configuration details, screenshots, risk scores, and identifiers have been altered or anonymized. The real environment and its data remain fully protected.

Device Overview: 
Project: Mobile Device Security Audit 

Objective: Assess and validate the effectiveness of security configuration profiles applied across all student iPads to ensure compliance with organizational security policies and reduce data exposure risks.

SCOPE: 
Reviewed configuration profile settings, app store access, data backup policies. 
Mapped implemented settings to CIS Apple iOS Benchmarks and NIST 800-53 mobile device management controls.
Identified deviations from baseline standards and documented risk impact levels (low/medium/high).
Provided remediation recommendations for non-compliant or weakly enforced controls.
Reduced risk of unauthorized access and data leakage on 500+ managed devices.
Established audit trail and documentation for annual compliance review.

Pre-Audit Security Posture (Baseline Findings)
Before conducting the audit, the iPads were configured with minimal security enforcement. The existing controls consisted of:
App Blocking List: Certain applications were restricted. If an end user installed a restricted app, the device would automatically lock itself.


Offline Lock Policy: Devices that remained offline for extended periods would self-lock after exceeding the defined threshold.

Beyond these two measures, no additional security or compliance restrictions were in place. Specifically:
End users could freely sign in with personal Apple IDs, enabling iMessage, FaceTime, Photos, iCloud, and Keychain synchronization.
The App Store was unrestricted, allowing the installation of any third-party applications without prior approval.


As a result, the environment faced several material risks:

Data Leakage Risk: Users could sync or transfer sensitive organizational data to personal iCloud accounts.

Compliance Gap: The lack of enforced configuration controls meant devices were not aligned with security standards such as CIS or NIST.

Accountability Risk: There was no centralized visibility or audit trail to track data movement or application usage.
In summary, the absence of baseline configuration and identity restrictions created an environment prone to unauthorized data access, loss of sensitive information, and policy non-compliance.

Post-Audit Security Posture (Remediation and Policy Implementation)

Following the audit, a new configuration profile was developed and deployed via Jamf MDM, introducing a comprehensive mobile device security policy applied to all iPads. This policy established a consistent baseline for device configuration, aligning with CIS Apple iOS Benchmarks and NIST 800-53 mobile device management controls.
Pre audit risk register score 59 VS Post audit risk register score 40

The following key controls were implemented:

Apple ID Restriction:

Apple ID login was disabled across all devices to prevent synchronization of personal data such as iMessage, FaceTime, Photos, iCloud backups, Keychain passwords, and other user-linked content.


Objective: Protect organizational and student data by eliminating data exfiltration vectors and ensuring no personal accounts are associated with managed devices.


App Store Restriction:

The App Store was disabled for end users to ensure only organization-approved applications are installed. Rather than relying on a static block list (which only restricts certain apps), this approach enforces a whitelist model—allowing only vetted, secure applications to be deployed directly through Jamf MDM.


Objective: 

Maintain control over the device software ecosystem, prevent installation of unauthorized or high-risk applications, and uphold compliance with software governance standards.

As a result of these changes:
All iPads now operate in a controlled, policy-driven environment with no personal iCloud or Apple ID data present.


Application installations are centrally managed by IT, ensuring all approved apps are deployed via Jamf MDM rather than through end-user actions.


The organization achieved full alignment with its mobile device security policy, significantly reducing risks of data leakage, unauthorized access, and non-compliance.


