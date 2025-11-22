
# Vision
**A Vacation Tracking System (VTS)** will provide individual employees with the capability to 
- **manage** their own: 
	- vacation time
	- sick leave
	- and personal time off
without having to be an expert in company policy or the local facility’s leave policies.

- **streamline** the functions of the human resources (HR) department, to minimize noncore, business-related activities of management, and to give a sense of empowerment to the employees.

# Functional Requirement 
-  **Employee** uses this system to manage his or her vacation time.
	- viewing
	-  creating
	-  and canceling vacation time requests.
- **Manager** can:
	-   approve vacation requests for immediate subordinates.
	-   award subordinates comp time (subject to certain limits set in the system)
	- directly award personal leave time (with system-set limits)
-  **Clerk (HR Employee)**:
	- view employees’ personal data.
	- responsible for ensuring that employees’ information in all HR systems is up to date and correct.
	-  Add nearly any record in the system. 
	- remove nearly any record in the system.
	- Interfaces with the HR department legacy systems to retrieve required employee information and changes.
	
- Provides a Web service interface for other internal systems to query any given employee’s vacation request summary

- Provides access to requests for the previous calendar year, and allows requests to be made up to a year and a half in the future.

# Non-Functional Requirement 
- The main goal of this application is to improve the internal business processes of this organization, at least with respect to the time it takes to manage vacation time *(all vacation time had to be approved by an immediate man ager and then checked by a clerk in the HR department before it was authorized. Sometimes this manual process could take days. An automated system will speed up this process and will require at most one manual approval by the immediate manager )*

- Easy to use *(High-level and potentially vague features like this sometimes need to be part of the official requirements set, not so they can be objectively verified and tracked through testing, but rather so they can be used to support and justify other, more concrete requirements or design decisions. As an example)*

- This system has the potential to save time and money mostly in the HR depart ment, which is essentially taken out of the individual time request process and replaced by a rules-based validation system.

- Keeps activity logs for all transactions.

- Enables the HR and system administration personnel to override all actions restricted by rules, (functional)
with logging of those overrides

# Constrains
-   award subordinates comp time (subject to certain limits set in the system)
-  directly award personal leave time (with system-set limits)
- Provides access to requests for the previous calendar year, and allows requests to be made up to a year and a half in the future.
- Uses existing hardware and middleware.
- Is implemented as an extension to the existing intranet portal system, and uses the portal’s single-sign-on mechanisms for all authentication.

# Use Case Model (Top Level)
- The top-level use case model contains four actors and eight use cases.
<img width="947" height="668" alt="image" src="https://github.com/user-attachments/assets/3e56d5cf-b28f-4f82-9086-35b71a8634de" />

### Manage Time Use Case

-	**Use case name**: Manage Time 
	-  **Actor**: Employee 
	- **Goal**: The employee wishes to submit a new request for vacation time. 
	- **Preconditions**: The employee is authenticated by the portal framework and identified as an employee of the company with privileges to manage his or her own vacation time


- **Alternate flow 1**: Cancel Approved Request 
	-  **Goal**: The employee wants to cancel an approved vacation time request. 
	- **Preconditions**: The employee has a vacation time request that has been approved and is scheduled for some time in the future or the recent past (previous 5 business days)

- **Alternate flow 2**: Edit Pending Request 
	- **Goal**: The employee wants to edit the description or title of a pending request.
	- **Preconditions**: An employee has made a vacation time request, and that request has yet to be approved or denied by an authorized manager.
   
![manage-time](https://github.com/user-attachments/assets/4b37be45-f092-4516-9b0b-1f059cdf4d35)


