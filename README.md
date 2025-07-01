Garage Management System Using Salesforce
This project involves building a comprehensive Garage Management System using Salesforce's powerful capabilities, including sharing settings, flows, Apex triggers, reports, dashboards, and subscription features. Below is a combined and detailed overview of the project's features and implementation.

1. Profiles and Permission Sets
Profiles and permission sets control object-level and field-level permissions for users.
Profiles grant general access, while permission sets extend specific permissions to select users.
2. Sharing Settings
Configured Organization-Wide Defaults (OWD) to set the Service Records Object to "Private."
Created Sharing Rules to share specific records between roles:
Records of “Salesperson” role shared with “Manager” role.
Access level: Read/Write.
3. Flows
Developed a Record-Triggered Flow for the "Billing Details and Feedback" object:
Trigger: Executes when a record is created or updated.
Automation: Updates payment-related fields based on payment status and sends email notifications.
Custom Email Template: Sends a personalized email to customers thanking them for payments.
Flow Elements:
Update Record: Updates the "Payment Paid" field dynamically.
Send Email: Sends an email alert using a custom text template.
4. Apex Trigger and Handler
Apex Triggers:
Used to perform custom actions before/after database operations like insert, update, or delete.
Created a trigger for the "Appointment" object to handle service amount calculations.
Apex Handler Class:
Logic: Determines service amount based on selected options like Maintenance, Repairs, and Replacement Parts.
Implements a clean structure by separating business logic into a dedicated handler class.
5. Reports
Salesforce Reports enable detailed data visualization and sharing.
Report Types:
Tabular, Summary, Matrix, and Joined Reports.
Custom Report Creation:
Built a custom report type named "Service Information" using related objects: Customer Details, Appointment, Service Records, and Billing Details.
Designed a report that includes fields like Customer Name, Appointment Date, Payment Paid, and Service Rating.
Grouped rows by fields such as Payment Status and Service Rating.
Added a Line Chart for visual data representation.
6. Dashboards
Dashboards provide a real-time visual overview of business operations.
Features:
Created a dashboard folder labeled “Service Rating Dashboard.”
Built a dashboard using the reports created, including charts like Line Charts.
Theme Customization: Enhanced aesthetics and data clarity.
Subscription Feature:
Scheduled the dashboard to send weekly updates every Monday to stakeholders.
7. Apex Trigger for Amount Distribution
Trigger Name: AmountDistribution
Object: Appointment
Events Handled: Before Insert and Before Update
Purpose:
Dynamically calculate and assign service amounts based on the services selected.
Handler Logic:
Ensures clean separation of trigger logic from business logic.
Sets predefined service amounts based on selected combinations.
8. Subscription Management
Automated Notifications:
Subscribed the dashboard for weekly notifications.
Set notification frequency to send updates on Mondays.
9. End-to-End Data Visualization
Linked the system's objects for streamlined reporting and dashboard creation.
Reports and dashboards empower stakeholders to track and improve service performance metrics.
Project Impact
This Garage Management System demonstrates how Salesforce tools like flows, sharing settings, Apex triggers, reports, and dashboards can be leveraged to automate processes, enhance data insights, and improve customer relationships. The system ensures scalability, efficient data management, and optimized operational workflows, making it a valuable solution for garage services.
