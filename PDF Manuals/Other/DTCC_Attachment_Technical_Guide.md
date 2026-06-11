---
title: "IAT - Attachments Implementation Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/DTCC_Attachment_Technical_Guide.pdf"
pages: 6
size: "278.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# IAT - Attachments Implementation Guide

**Original File:** [DTCC_Attachment_Technical_Guide.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/DTCC_Attachment_Technical_Guide.pdf)  
**Category:** Other  
**Total Pages:** 6  
**File Size:** 278.1 KB  

---

## Page 1

6/01/2018   [[DTCC]] Confidential (Yellow)  Page 1 of 6 
[[DTCC]] Internal (Green) 
                       
 
 
 
 
IPS Web Services Technical Reference Guide 
Attachments Process 
[[participant]] Checklist 
  
 
 
The following information will provide [[DTCC]] Participants an overview of the requirements for 
establishing connectivity for processing Insurance Processing Service (IPS) Attachments. 
 
Test Set-up: 
 
1. [[participant]] submits the IPS Product Update Form (PUF). The IPS PUF is located in the 
[[participant]]’s Section of the IPS Web Site: http://www.[[DTCC]].com/forms/product-
request-form, under the Product & Trading Relationships Section, indicating the product 
set-up in Test for Attachments.  (See Exhibit 1.) 
 
2. Implementation Representative initiates a conference call with the [[participant]] within 24 
hours of receipt of the IPS PUF to discuss connectivity requirements that include Web 
set-up for Day One. 
 
3. Implementation Representative emails the Router Exchange Form (REF)* to the 
designated technical contact at the [[participant]] within 24 hours of receipt of the IPS PUF. 
The technical contact then completes the following sections of the form:   
 
• A through D (See Exhibit 2.) 
• I - Attachments Information for Participants (See Exhibit 3.) 
 
* The REF is the [[DTCC]] form that is used to set up connectivity via the [[DTCC]] SMART 
Network.  Participants are required to complete this form prior to the actual connectivity set-up.  
The REF refers to all of the necessary information required for router and firewall configuration 
set-ups. 
 


---

## Page 2

6/01/2018   [[DTCC]] Confidential (Yellow)  Page 2 of 6 
[[DTCC]] Internal (Green) 
• The REF provides the application URLs and IP Address in order to send inbound and 
outbound transactions.  Participants will need to provide the IP Addresses that the 
transmission will be sent from so [[DTCC]] can configure accordingly.  In addition, 
Participants will need to provide [[DTCC]] with one or two URLs: 
 
• Test URL – Message Level Security (MLS) – if required 
• Test URL – Non-Message Level Security 
  
For assistance in completing the REF, please email nsccconnectivity@[[DTCC]].com 
     
4. Once completed, [[participant]] emails the REF to nsccconnectivity@[[DTCC]].com and cc’s 
(copies) the Implementation Representative and Relationship Manager.  If the [[participant]] 
does not return the REF within three (3) business days to [[DTCC]], Implementation will 
follow-up with the [[participant]]. When [[NSCC]] Connectivity opens a ticket to request the 
set-up, the [[participant]] will receive an email from [[NSCC]] Connectivity with a ticket 
number, which will be the reference number for this request for the life cycle of the 
implementation process. 
 
5. [[NSCC]] Connectivity then forwards the REF to Network Engineering & Operations (NEO) 
to complete the Router and Firewall requirements. 
 
6. NEO will contact the [[participant]] once the Router and Firewall set-ups have been 
completed to test that connectivity has been established.  The estimated turnaround time 
is one (1) week.   
 
7. Implementation Representative confirms that the connectivity set-up with the [[participant]] 
has been completed. 
 
8.   Once completed, Implementation Representative will complete a request on your behalf 
for a [[DTCC]] Digital Certificate to our Registration Support Group (RSG).  This is 
required for two purposes: 
 
a. For firms sending messages to [[DTCC]], a digital certificate must be installed in 
your system as part of the B2B messaging process. 
b. For firms receiving messages from [[DTCC]], a digital certificate must be installed to 
gain access to the [[DTCC]] Portal web screens.  This will allow an operator at your 
firm to update your own Attachment Receiver Control Table.  The table will 
provide you capability to control what firms send you messages and the type of  
business transaction that will allow. 
 
9.  RSG contacts the [[participant]] to walk through the  registration process to download the 
Digital Certificate. 
 
10. [[participant]] is ready to submit/receive test files. 
 
 

---

## Page 3

6/01/2018   [[DTCC]] Confidential (Yellow)  Page 3 of 6 
[[DTCC]] Internal (Green) 
Production Set-up: 
 
1. For migration to the Production environment, the [[participant]] is required to submit a 
new IPS Product Update Form indicating the product set-up in Production for 
Attachments.  (See Exhibit 4.) 
 
2. [[participant]] will include the Production URL on the IPS Product Update Form. 
 
3. Implementation Representative will contact the [[participant]] to confirm that 
connectivity set-up in Production has been completed. 
 
 
*Note:  Any changes to the Test and/or Production IP Addresses require the submission of 
a new REF to: nsccconnectivity@[[DTCC]].com and cc’s (copies) the Implementation 
Representative and Relationship Manager.  
 
 
**Any questions regarding the Digital Certificate, please contact RSG at 888-382-2721, 
[[Option]] 5, then 2 or webrsg@[[DTCC]].com. 
 
 
***GEOTRUST is one of two types of Digital Certificates used by [[DTCC]] systems for 
authentication purposes: 
• GEOTRUST Certificates are currently used on all applications that require a 
Digital Certificate; 
• GEOTRUST Certificates expire after one (1) year, but the system has logic to 
automatically re-issue before the expiration; 
• GEOTRUST Certificates can be issued by the Registration Support Group (RSG) at 
this time with appropriate authentication and approval; 
• GEOTRUST Certificates will be able to be reissued by Access Coordinators at the 
end of July due to system enhancements; 
• GEOTRUST Certificates are installed locally; meaning when a customer moves to 
another computer, the Digital Certificate is not necessarily available on the new 
machine unless there is a network provision. 
 

---

## Page 4

6/01/2018   [[DTCC]] Confidential (Yellow)  Page 4 of 6 
[[DTCC]] Internal (Green) 
 
Exhibit 1: 
 
 

---

## Page 5

6/01/2018   [[DTCC]] Confidential (Yellow)  Page 5 of 6 
[[DTCC]] Internal (Green) 
 
Exhibit 2: 
 
Participants - Complete Client Host Sections: 
 
[[DTCC]] Host Client Host 
APPL. System IP Address 
TCP 
Port 
 
Subnet 
Mask IP Address Subnet 
Mask 
TCP 
Port 
Attachments 
 
Sender (inbound): 
 
DNS URLs  
  
 
 
 
 
 
 
PROD 
 
PSE 
(TEST) 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
    
 
 
[[DTCC]] Host Client Host 
APPL. System IP Address 
TCP 
Port 
 
Subnet 
Mask IP Address Subnet 
Mask 
TCP 
Port 
 
Attachments 
 
Recipient (outbound): 
 
URL Information (Carrier must provide URR 
– [[DTCC]] will initiate an outbound connection 
to the URL provided)  
 
 
PSE (Test) URL: 
 
________________________________ 
 
 
Note: Production URL’s will be provided to 
Implementation in a separate request at the time 
you are ready to go into production. 
 
 
 
 
 
PROD 
 
PSE 
(TEST) 
 
 
 
 
 
 
 
 
 
 
 
 
    

---

## Page 6

6/01/2018   [[DTCC]] Confidential (Yellow)  Page 6 of 6 
[[DTCC]] Internal (Green) 
FAQs 
 
 
1. Why [[DO]] I need to complete a Router Exchange Form (REF)?  I believe that I 
already completed one. 
Answer – You are correct. When connectivity to your circuit was originally set up, you 
needed to complete an REF. At that time, Fund Transfers was not an application that was 
being implemented for your connectivity profile.  You and [[DTCC]] need to exchange IP 
Addresses for this new host application (Attachments).  This way the IP Addresses can be 
configured properly and enabled to our routers and firewalls. You will also need to 
enable [[DTCC]] IP Addresses through your firewalls. 
2. Is there a fee for adding Attachments to my circuit? 
Answer – [[DTCC]] does not charge additional connectivity fees for additional applications 
to an existing circuit.   
3. [[DO]] we need to update our membership to start utilizing Attachments? 
Answer – No.  If you are approved for IPS Membership, no additional documentation is 
required for Attachments. 
4.   [[DO]] I need to have the Attachments product set up in the Test region prior to  going l
 live in Production?  
Answer – No.  You can go directly into Production. 
 
5.   What is the implementation timeframe for the Attachments product?  
Answer – The estimated timeframe for Attachments is ten (10) business days from 
 receipt of the REF through implementation. 
6.   What is the difference between a DNS URL and a non-DNS URL?  
Answer – A DNS URL contains a name whereas a non-DNS URL contains an IP 
Address. 
 
 
 
 
 
 
 
 
 
        
 