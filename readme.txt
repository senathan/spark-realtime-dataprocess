spark streaming、spark连接mysql、gp的相关技术。
Category


Summary,Description,Label,Issue Type,Story Points
"Update Schema with Email Field","Story:  
As a system admin  
I need to add an email field to the SPDW table  
So that batch jobs can send notifications.  

Acceptance Criteria:  
Scenario 1: Schema Change  
Given: The SPDW table exists  
When: I run the migration script  
Then: The email column (VARCHAR(255), nullable) is added.  

Scenario 2: Backward Compatibility  
Given: Existing batch jobs  
When: The schema is updated  
Then: Jobs should run without errors.","Cloud-WAF-Automation-Batch",Story,1
"Load Akamai Templates via API","Story:  
As a batch operator  
I want to fetch Akamai templates from their API  
So that templates are available for onboarding.  

Acceptance Criteria:  
Scenario 1: API Connection  
Given: Valid API credentials  
When: The job runs  
Then: Data is saved to Akamai_Templates table.  

Scenario 2: Data Validation  
Given: 10 templates exist in Akamai  
When: The job completes  
Then: All 10 are stored with IDs and names.","Cloud-WAF-Automation-Batch",Story,2
"Load Akamai Property Configs","Story:  
As an operator  
I need to load property configurations  
So that teams can map services to Akamai.  

Acceptance Criteria:  
Scenario 1: Config Mapping  
Given: A property config ID  
When: Data is loaded  
Then: It links to the correct service in SPDW.  

Scenario 2: Error Handling  
Given: An invalid config ID  
When: The job runs  
Then: It logs the error and skips the record.","Cloud-WAF-Automation-Batch",Story,2
"Load Akamai Security Policies","Story:  
As a security engineer  
I want security policies loaded automatically  
So that I don’t have to manually enter them.  

Acceptance Criteria:  
Scenario 1: Policy Sync  
Given: New policies in Akamai  
When: The batch job runs  
Then: Policies appear in the Security_Policies table.  

Scenario 2: Field Completeness  
Given: A policy has 5 fields  
When: Data is loaded  
Then: All 5 are stored (no NULLs).","Cloud-WAF-Automation-Batch",Story,2
"Load Akamai Host Information","Story:  
As a network admin  
I need host details (DNS, TTL, HTTP methods)  
So that I can troubleshoot issues faster.  

Acceptance Criteria:  
Scenario 1: Host Data Load  
Given: 100 hosts in Akamai  
When: The job runs  
Then: All appear in the Host_Info table.  

Scenario 2: Critical Fields  
Given: A host record  
When: Data is loaded  
Then: DNS type and TTL are mandatory.","Cloud-WAF-Automation-Batch",Story,2
"Load Akamai Certificate Data","Story:  
As a security team member  
I want certificate expiry dates tracked  
So that we avoid outages.  

Acceptance Criteria:  
Scenario 1: Certificate Sync  
Given: Certificates in Akamai CPS  
When: The job runs  
Then: Expiry dates are stored in Certificates table.  

Scenario 2: Alert Threshold  
Given: A cert expires in 30 days  
When: Data is loaded  
Then: It’s flagged in the UI.","Cloud-WAF-Automation-Batch",Story,2
"Map Hostnames to Configs","Story:  
As an onboarding specialist  
I need hostnames linked to configs/policies  
So that services are protected correctly.  

Acceptance Criteria:  
Scenario 1: Mapping Accuracy  
Given: HostA belongs to ConfigX  
When: Data is loaded  
Then: The mapping is stored in Host_Config_Mappings.  

Scenario 2: Conflict Handling  
Given: HostA mapped to ConfigX and ConfigY  
When: The job runs  
Then: It logs a warning.","Cloud-WAF-Automation-Batch",Story,2
"Setup MDC Logging for Batch","Story:  
As a DevOps engineer  
I want logs with trace/correlation IDs  
So that I can debug batch jobs easily.  

Acceptance Criteria:  
Scenario 1: Log Format  
Given: A batch job runs  
When: It logs an event  
Then: The trace ID is included.  

Scenario 2: Error Tracking  
Given: A job fails  
When: I check logs  
Then: I see the error and correlation ID.","Cloud-WAF-Automation-Batch",Story,1
"Validate UAT Data Load","Story:  
As a tester  
I want to verify UAT data loads correctly  
So that we can proceed to production.  

Acceptance Criteria:  
Scenario 1: Data Completeness  
Given: UAT batch jobs run  
When: I check tables  
Then: All expected records exist.  

Scenario 2: Cron Job Test  
Given: A scheduled job  
When: It triggers at 2 AM  
Then: It completes successfully.","Cloud-WAF-Automation-Batch",Story,1
"Design Menu/Landing Page","Story:  
As a user  
I want a clean menu and landing page  
So that I can navigate easily.  

Acceptance Criteria:  
Scenario 1: Menu Items  
Given: I open the UI  
When: The page loads  
Then: I see links to Onboarding, Reports, Settings.  

Scenario 2: Responsiveness  
Given: I’m on a mobile device  
When: I open the menu  
Then: It collapses into a hamburger icon.","Cloud-WAF-Automation-UI",Story,2
"Display Onboarding Grid","Story:  
As an onboarding manager  
I want a grid of requests  
So that I can track progress.  

Acceptance Criteria:  
Scenario 1: Column Visibility  
Given: 10+ requests exist  
When: I load the grid  
Then: I see ID, Service Name, Status, Owner.  

Scenario 2: Sorting  
Given: The grid is open  
When: I click the "Status" column  
Then: Requests sort by status (ASC/DESC).","Cloud-WAF-Automation-UI",Story,3
"Show Service Info on Selection","Story:  
As a user  
I want details when I click a grid row  
So that I don’t have to open a new page.  

Acceptance Criteria:  
Scenario 1: Data Display  
Given: I select a service  
When: The section expands  
Then: I see DNS, IP, and owner info.  

Scenario 2: Empty State  
Given: No service is selected  
When: I view the section  
Then: It shows 'Select a row to see details'.","Cloud-WAF-Automation-UI",Story,2
"Add Search/Filter to Grid","Story:  
As a user  
I want to filter the grid  
So that I can find requests faster.  

Acceptance Criteria:  
Scenario 1: Text Search  
Given: I type 'API' in search  
When: I press Enter  
Then: Only services with 'API' in the name appear.  

Scenario 2: Status Filter  
Given: I select 'Pending'  
When: I apply the filter  
Then: Only pending requests display.","Cloud-WAF-Automation-UI",Story,3
"Display Host Info Section","Story:  
As a network engineer  
I need host-specific data (TTL, DNS)  
So that I can debug issues.  

Acceptance Criteria:  
Scenario 1: Host Data Load  
Given: A host is selected  
When: The section loads  
Then: I see TTL, DNS record type, and HTTP methods.  

Scenario 2: Error State  
Given: Invalid host data  
When: The section loads  
Then: It shows 'Data unavailable'.","Cloud-WAF-Automation-UI",Story,2
"New Onboarding Modal (Stepper)","Story:  
As a user  
I want a step-by-step modal  
So that I can onboard services easily.  

Acceptance Criteria:  
Scenario 1: Step Navigation  
Given: I’m on Step 1  
When: I fill required fields  
Then: I can click 'Next' to Step 2.  

Scenario 2: Validation  
Given: I skip a required field  
When: I click 'Next'  
Then: The button is disabled, and I see an error.","Cloud-WAF-Automation-UI",Story,5
"Show User Inputs in Grid","Story:  
As a user  
I want to review my inputs before submitting  
So that I can catch mistakes.  

Acceptance Criteria:  
Scenario 1: Input Summary  
Given: I filled 5 fields  
When: I reach the review step  
Then: I see all 5 values in a grid.  

Scenario 2: Edit Option  
Given: I spot an error  
When: I click 'Edit'  
Then: It takes me back to the relevant step.","Cloud-WAF-Automation-UI",Story,3
"Display Configuration Mappings","Story:  
As an engineer  
I want to see Akamai config mappings  
So that I can verify correctness.  

Acceptance Criteria:  
Scenario 1: Config Display  
Given: A service is selected  
When: I open the Config tab  
Then: I see linked Akamai property/security configs.  

Scenario 2: No Mappings State  
Given: No configs are mapped  
When: I open the tab  
Then: It shows 'No configurations found'.","Cloud-WAF-Automation-UI",Story,2
"Handle Onboarding Errors","Story:  
As a user  
I want clear error messages  
So that I can fix issues quickly.  

Acceptance Criteria:  
Scenario 1: API Failure  
Given: The backend API is down  
When: I submit the form  
Then: I see 'Server error. Try again later.'  

Scenario 2: Validation Error  
Given: I enter an invalid hostname  
When: I click Submit  
Then: I see 'Hostname must be alphanumeric'.","Cloud-WAF-Automation-UI",Story,2
"Review Page Before Submit","Story:  
As a user  
I want a final summary before submitting  
So that I can confirm accuracy.  

Acceptance Criteria:  
Scenario 1: Summary Layout  
Given: I complete all steps  
When: I reach the review page  
Then: I see sections for Service, Host, Config.  

Scenario 2: Edit Option  
Given: I need to change a value  
When: I click 'Edit'  
Then: It takes me to the correct step.","Cloud-WAF-Automation-UI",Story,3
"Setup UI Logging","Story:  
As a developer  
I want UI logs with MDC context  
So that I can track user actions.  

Acceptance Criteria:  
Scenario 1: Log Events  
Given: A user clicks 'Submit'  
When: The action completes  
Then: The log includes user ID and timestamp.  

Scenario 2: Error Logging  
Given: An API call fails  
When: The error is caught  
Then: The log includes the HTTP status code.","Cloud-WAF-Automation-UI",Story,1
