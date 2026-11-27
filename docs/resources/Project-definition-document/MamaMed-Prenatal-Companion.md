

MamaMed Prenatal Companion
## Project Document
A maternal health follow for expecting mothers and new parents,
paired with a clinic dashboard.
Presented by:
## Muliri Shebirongo Jonathan

Table of contents
1.General description.....................................................................................................................4
1.1 Initial context...............................................................................................................................4
- Problem statement..........................................................................................................................5
2.1 Research question.....................................................................................................................5
- Justification........................................................................................................................................5
3.1 Positioning....................................................................................................................................5
3.2 Acknowledged limits.................................................................................................................5
3.3 Outlook and sustainability.......................................................................................................5
- Proposed solution.............................................................................................................................6
4.1 Reminders and privacy............................................................................................................6
- Objectives..........................................................................................................................................6
5.1 General objective......................................................................................................................6
5.2 Specific objectives.....................................................................................................................7
- Project scope....................................................................................................................................7
6.1 In scope (MVP)...........................................................................................................................7
6.2 Planned for version 2.................................................................................................................7
6.3 Out of scope...............................................................................................................................8
- System actors.....................................................................................................................................8
7.1 Mother or expecting mother..................................................................................................8
7.2 Midwife or health worker.........................................................................................................8
7.3 Clinic manager...........................................................................................................................8
7.4 NGO officer (version 2).............................................................................................................9
7.5 System administrator.................................................................................................................9
7.6 Health reviewer...........................................................................................................................9
7.7 Unauthenticated visitor............................................................................................................9
7.8 External systems..........................................................................................................................9
7.9 Roles and permissions...............................................................................................................9
- Functional modules.......................................................................................................................11
8.1 Authentication and users......................................................................................................11
8.2 Patient record and consent.................................................................................................11

8.3 Visit calendar.............................................................................................................................11
8.4 Reminders...................................................................................................................................11
8.5 Danger sign checker (version 2)..........................................................................................11
8.6 Clinic follow-up.........................................................................................................................11
8.7 Educational cards (version 2)...............................................................................................12
8.8 Reports (version 2)....................................................................................................................12
8.9 Administration...........................................................................................................................12
8.10 Infrastructure and quality....................................................................................................12
- Business rules....................................................................................................................................12
9.1 Visit calendar.............................................................................................................................12
9.2 Reminders...................................................................................................................................13
9.3 Follow-up of missed visits........................................................................................................13
9.4 Consent and traceability.......................................................................................................14
9.5 Administration...........................................................................................................................14
- Initial functional requirements..................................................................................................15
- Initial non-functional requirements.........................................................................................17
- Risks and pending decisions.....................................................................................................18
- User stories......................................................................................................................................19
13.1 Authentication and users....................................................................................................19
13.2 Patient record and consent...............................................................................................20
13.3 Visit calendar..........................................................................................................................21
13.4 Reminders................................................................................................................................21
13.5 Danger sign checker............................................................................................................22
13.6 Clinic follow-up.......................................................................................................................22
13.7 Educational cards (version 2)............................................................................................23
13.8 Reports (version 2).................................................................................................................24
13.9 Administration.........................................................................................................................24

1.General description
MamaMed is a maternal and child health follow-up web application that helps mothers
avoid missing visits and helps clinics know whom to contact. It accompanies the mother
from early pregnancy through the first two years of the child's life, and comes with a
dashboard for the clinic.
The first version (MVP) generates a visit calendar (antenatal, postnatal, and
immunization), schedules reminders before each visit, and gives clinics a daily list of
mothers who missed a visit. A system administrator manages clinics, accounts, and
settings. The educational cards, the clinic and NGO reports, and the danger sign
checker come in version 2.
The project is not intended to diagnose or to replace a health professional. It always
recommends consulting a qualified professional. Its goal is to make it easier to follow up
on mothers and to help clinics know whom to contact, based on explicit business rules.
1.1 Initial context
MamaMed will first operate in the Democratic Republic of the Congo (DRC), in one or
two urban or peri-urban partner clinics. The project is no longer presented as pan-
African: any extension to another country will require a new review of healthcare
guidelines, languages, and regulations.
ItemInitial choice
CountryDemocratic Republic of the Congo (DRC)
AudienceMothers in urban and peri-urban areas, followed by a
partner clinic
LanguagesEnglish and French for the interface and messages;
educational cards in French and English, then in local
languages (for example Lingala, Swahili) in version 2 once
a validated translation is available
Reminder channelSMS, then WhatsApp; sending simulated in the MVP
Visit calendar rulesBased on WHO recommendations (eight antenatal
contacts, postnatal care, and the childhood
immunization schedule) and adjusted to national
protocols with a health professional before real use
Data protectionPersonal data is handled according to the data
protection regulations applicable in the DRC, with data
minimization and explicit consent from the first version
Field constraintsPhones sometimes shared, limited connectivity, and
paper registers still in use, so data entry must stay light

- Problem statement
In the DRC, as in many African countries, maternal and newborn mortality remains high.
Among the causes, mothers miss antenatal visits, forget key danger signs, and lose
contact with their health worker after delivery.
Clinics often work from a paper register and only call a mother when it is already too
late. Public campaigns reach millions of people but cannot personalize the message.
Mothers and clinics may therefore have difficulty:
•Remembering the dates of antenatal, postnatal, and immunization visits.
•Recognizing danger signs and knowing when to go to the clinic.
•Staying in contact with a health worker after delivery.
•Quickly identifying which mothers missed a visit.
•Measuring visit attendance and the effectiveness of follow-up, by clinic or by
program.
The reminders and content of a digital tool do not replace care: their effect depends
on actual use by mothers and on the follow-up work of clinics.
2.1 Research question
How can the follow-up of mothers and young children be made easier through
personalized reminders and a follow-up list for clinics, while protecting the privacy of
health data?
## 3. Justification
The project proposes to personalize the follow-up that public campaigns cannot offer,
and to give clinics a simple way to know who to contact. It centralizes the visit
calendar, reminders, educational content, and attendance indicators.
## 3.1 Positioning
Mobile health programs already exist, such as MomConnect in South Africa, which
serves as an inspiration. MamaMed differs through its local focus (languages, partner
clinics in the DRC) and through a follow-up dashboard for the clinic, in addition to the
messages sent to mothers.
3.2 Acknowledged limits
The scope is that of a functional product for academic purposes. Reminders are
simulated in the first version, no medical content is published without review by a health
professional, and the project makes no diagnosis.
3.3 Outlook and sustainability
Mothers use the application for free. Future revenue would come from the
organizations that fund or run follow-up programs: NGOs and maternal health programs

(licensing with reporting), donors (start-up funding), and clinics (subscription). A pilot
with one or two clinics will measure the effect on visit attendance before any
commercialization.
- Proposed solution
Develop a web application, delivered in two stages (an MVP focused on follow-up,
then a version 2), that integrates the following capabilities:
1.Patient record with consent (MVP): registration of the mother by the midwife or
health worker (name, phone, estimated due date or child's date of birth, clinic)
with her explicit agreement.
2.Visit calendar (MVP): automatic generation of antenatal, postnatal, and
immunization visits from configurable rules.
3.Reminders (MVP): messages sent 48 hours and 24 hours before each visit, by SMS
and WhatsApp (simulated in the first version).
4.Clinic follow-up list (MVP): a daily list of mothers who missed a visit, with contact
details ready to use and recording of the call outcome.
5.Administration (MVP): a system administrator who manages clinics, manager
accounts, calendar rules, and system settings.
6.Educational cards (version 2): short, reviewed, sourced content on nutrition,
danger signs, and infant care.
7.Clinic reports (version 2): simple indicators on enrollment, attendance, and
follow-up.
8.Danger sign checker (version 2): a short questionnaire that directs the user to the
clinic, without diagnosing.
9.NGO reports (version 2): aggregate indicators without personal data.
The first version uses explicit business rules, without artificial intelligence. Actual SMS and
WhatsApp sending goes through an external provider, which will be connected in a
later version.
4.1 Reminders and privacy
Reminder messages are written discreetly, without medical detail, to protect a mother
whose phone is shared. No message is sent without consent, and a mother can
unsubscribe at any time. Each reminder is recorded in a sending log with its status
(scheduled, sent, failed, and cancelled).
## 5. Objectives
5.1 General objective
Develop a maternal and child health follow-up web application that helps mothers
avoid missing their visits and helps clinics follow up with those who did, while protecting
data privacy.

5.2 Specific objectives
•Analyze the problem, identify the actors, and establish the functional and non-
functional requirements.
•Model the system's domain and its main interactions.
•Design a normalized relational database representing users, clinics, mothers,
children, visits, reminders, follow-ups, educational cards, and logs.
•Implement a REST API organized by responsibilities, with input validation,
consistent error handling, and access control.
•Build a simple web interface, usable on a phone, for clinic staff and
administrators.
•Provide an administration space to manage clinics, accounts, and system
settings.
•Automatically generate a visit calendar based on configurable rules.
•Schedule reminders 48 and 24 hours before each visit, with a sending log.
•Produce the daily follow-up list of mothers who missed a visit and record the
outcome of each contact.
•Produce aggregate reports for the clinic and for NGOs (version 2).
•Protect health data and respect users' consent.
•Verify the main flows through tests and technical documentation.
- Project scope
The MVP is limited to follow-up: register a mother, generate her calendar, remind her,
and help the clinic follow up with those who missed a visit, under the control of a system
administrator. Everything else moves to version 2 or out of scope.
6.1 In scope (MVP)
•Web application with several profiles: midwife or health worker, clinic manager,
and system administrator. The mother has no account.
•Registration of a mother with consent (name, phone, estimated due date or
child's date of birth, clinic) and withdrawal of consent.
•Automatic generation of the antenatal, postnatal, and immunization visit
calendar.
•Recording of attendance, absence, or postponement of a visit.
•Reminders 48 and 24 hours before each visit, simulated, with a sending log.
•Daily follow-up list of mothers who missed a visit, with recording of the contact
outcome.
•Administration of clinics, accounts, calendar rules, and system settings.
•Tests, API documentation, and a reproducible development environment setup.
6.2 Planned for version 2
•Danger sign checker, after review and validation by a health professional.
•Aggregate reports for the clinic, and the NGO officer profile with multi-clinic
reports without personal data.

•Actual SMS and WhatsApp sending through an external provider, with a STOP
reply to unsubscribe.
•Educational cards in French and English, reviewed by a health professional and
published by the clinic manager, then in a local language once a validated
translation is available.
•Direct access for the mother to her calendar (account with phone and code).
6.3 Out of scope
•Diagnosis or personalized medical advice.
•Growth tracking, telemedicine, a community health worker app, voice notes,
and offline mode.
•Integration with the national maternal and child health register.
•Payment, billing, and subscriptions.
•Sponsored content.
•Native mobile application.
•Production deployment and availability commitments.
•Any guarantee of the accuracy of the information entered by clinics.
- System actors
Each role has precise rights, limited to its clinic of assignment, except the system
administrator. The server checks these rights on every request, including a direct API
call.
7.1 Mother or expecting mother
Primary beneficiary, in urban and peri-urban areas. In the MVP she has no account.
•Be registered by the clinic with her consent.
•Receive reminders before each visit.
•Be contacted by the clinic's midwife when she misses a visit.
•Ask the clinic to withdraw her consent at any time.
•In version 2: read the educational cards, use the danger sign checker, and view
her own calendar.
7.2 Midwife or health worker
Main user of the MVP, who follows the mothers of a clinic.
•Log in to the system.
•Register a mother with her consent, and view and edit her record.
•Record attendance, absence, or postponement of a visit.
•View each day the list of mothers who missed a visit.
•Record the outcome of a follow-up contact.
7.3 Clinic manager
Responsible for the staff accounts and data of their clinic.

•Manage the accounts of their clinic's staff.
•View their clinic's sending log, access history, and records (read-only).
•In version 2: view the clinic reports, and manage and publish educational cards
after review by a health professional.
7.4 NGO officer (version 2)
Tertiary user, who follows a program across several clinics.
•View aggregate reports for their clinics (for example, the percentage of mothers
who attended their third antenatal visit).
•No access to mothers' personal data.
7.5 System administrator
Responsible for the platform as a whole, not for patient care. The first administrator
account is created when the system is installed.
•Create and deactivate clinics.
•Create and deactivate clinic manager and NGO officer accounts.
•Configure the visit calendar rules and the system settings (reminder times, retries,
follow-up attempts).
•View the system-wide history of accesses and modifications.
•No access to mothers' records or contact details.
7.6 Health reviewer
Health professional outside the system, who will review the educational cards and the
danger sign questionnaire in version 2. The reviewer has no account: the clinic manager
records the reviewer's name and the review date.
7.7 Unauthenticated visitor
Can view the public pages (presentation and, in version 2, the published educational
cards and the danger sign checker), without access to records.
7.8 External systems
SMS and WhatsApp providers are external systems. No actual integration is planned in
the first version: sending is simulated and recorded in a log.
7.9 Roles and permissions
ActionMidwifeClinic
manager
## NGO
officer (V2)
AdministratorMotherVisitor
Log in
## ✓✓✓✓
## ——
Create and deactivate
clinics
## ———
## ✓
## ——

ActionMidwifeClinic
manager
## NGO
officer (V2)
AdministratorMotherVisitor
Create and deactivate
clinic manager and NGO
officer accounts
## ———
## ✓
## ——
Create and deactivate staff
accounts of a clinic
## —
## ✓
## —
## ✓
## ——
Configure calendar rules
and system settings
## ———
## ✓
## ——
Register a mother with her
consent
## ✓
## —————
View a record
## ✓
## Read-
only
## ————
Edit a record (due date,
phone)
## ✓
## —————
Record attendance,
absence, or postponement
## ✓
## —————
Record the withdrawal of
consent
## ✓
———Reque
st
## —
View the follow-up list and
note an outcome
## ✓
## Read-
only
## ————
View the reminder sending
log
## ✓✓
## ————
Create and edit
educational cards (V2)
## —
## ✓
## ————
Publish a reviewed card
## (V2)
## —
## ✓
## ————
Read published cards (V2)
## ✓✓✓✓✓✓
Clinic report (V2)—
## ✓
## ————
NGO aggregate report——
## ✓
## ———
View the access and
modification history
## —
## ✓ (own
clinic)
## —
## ✓ (system-
wide, no
health
content)
## ——

ActionMidwifeClinic
manager
## NGO
officer (V2)
AdministratorMotherVisitor
Use the danger sign
checker (V2)
## ————
## ✓✓
Three decisions answer the main questions about roles:
•Who can modify patient records? Only the midwife or health worker of the clinic.
The clinic manager has read-only access for supervision, and every change is
logged.
•Who approves educational content? From version 2, a health reviewer reviews it
and the clinic manager then publishes it. A card without a source, reviewer, and
review date cannot be published.
•Can mothers access their own accounts? Not in the MVP: the clinic registers
them and manages their consent on request. Direct access with phone and
code comes in version 2.
- Functional modules
8.1 Authentication and users
Manages staff and administrator login, accounts, profiles, and access rights according
to the role and the clinic of assignment.
8.2 Patient record and consent
Registers a mother with her name, phone, estimated due date or child's date of birth,
and clinic. Stores her consent and allows it to be withdrawn.
8.3 Visit calendar
Generates antenatal, postnatal, and immunization visits from configurable rules, records
the attendance, absence, or postponement of each visit, and recalculates the
calendar when the due date changes.
## 8.4 Reminders
Schedules reminders 48 and 24 hours before each visit, sends them through a simulated
channel (SMS or WhatsApp), and keeps a sending log.
8.5 Danger sign checker (version 2)
Offers a short self-check questionnaire. It always directs the user to a clinic visit and
never makes a diagnosis.
8.6 Clinic follow-up
Produces each day the list of mothers who missed a visit, with their contact details, and
records the outcome of each contact attempt.

8.7 Educational cards (version 2)
Manages short cards on nutrition, danger signs, and infant care, with their language,
source, reviewer, and review status.
## 8.8 Reports (version 2)
Produces aggregate reports for the clinic (enrolled mothers, visit attendance, reminders
sent, and follow-ups completed) and for the NGO.
## 8.9 Administration
Lets the system administrator create and deactivate clinics and manager accounts,
configure the calendar rules and system settings, and view the system-wide history of
accesses and modifications, without access to mothers' personal data.
8.10 Infrastructure and quality
Covers the setup of the development environment, database migrations, environment
variables, tests, API documentation, and instructions for running the project.
- Business rules
These rules specify the behavior of the calendar, reminders, follow-up, consent, and
administration. Values marked "configurable" are settings that the administrator can
change, not code. Each rule is covered by a test.
9.1 Visit calendar
CodeRule
BR-01Antenatal visits are calculated from the estimated due date (EDD);
postnatal and immunization visits, from the child's date of birth.
BR-02When a mother is registered late, only upcoming visits are created: a
visit whose date has already passed is neither created nor counted as
missed.
BR-03If the EDD changes, antenatal visits not yet recorded are recalculated;
those already recorded (attended, absent) stay unchanged; reminders
for the old dates are cancelled and rescheduled; the change is logged
(author, date, old and new value).
BR-04When the date of birth is entered, the remaining antenatal visits are
closed and the postnatal and immunization calendars are generated.
BR-05A visit has one of these statuses: planned, attended, absent, postponed,
closed. Only the midwife or health worker changes the status, and an
upcoming visit cannot be marked attended or absent.
BR-06To postpone a visit, the midwife enters a new future date; the old date is

CodeRule
kept; the visit is not counted as missed until the new date has passed;
reminders are recalculated on the new date.
BR-07If no status is entered the day after a visit, it appears in the "Status to
confirm" section of the follow-up list and is not counted as missed until it
is marked absent.
Initial calendar values (configurable, based on WHO recommendations):
TypeVisits
Antenatal8 contacts at 12, 20, 26, 30, 34, 36, 38, and 40 weeks of
gestation (date = EDD − (40 − week) × 7 days)
PostnatalAt day 3, day 10, and day 42 after birth
ImmunizationAt birth, at 6, 10, and 14 weeks, then at 9 months
## 9.2 Reminders
CodeRule
BR-08Each visit has two reminders, at D-2 and D-1, at a configurable sending
time (09:00 by default). If the visit is less than 48 hours away at creation,
only the reminder still possible is scheduled; no reminder for a past visit.
BR-09A scheduled reminder becomes "cancelled" if the visit is attended,
postponed, or closed, or if consent is withdrawn.
BR-10The sending log uses four statuses: scheduled, sent, failed, cancelled. A
failed sending is retried once (configurable).
BR-11Reminder text is discreet: clinic name, date, and time, without the word
"pregnancy" or any medical term.
BR-12No message is scheduled or sent without recorded consent.
9.3 Follow-up of missed visits
CodeRule
BR-13The follow-up list is generated each morning (configurable time) for the
user's clinic. It contains mothers with at least one unresolved absent visit
who have not withdrawn consent, sorted from the oldest absence to the
newest, with name, phone, missed visit, days elapsed, and number of
attempts.
BR-14After three unsuccessful attempts (configurable), the case becomes

CodeRule
"not reached", leaves the daily list, and stays visible to the clinic
manager.
BR-15A contact outcome records its date, its author, and an optional note
without medical detail.
A contact outcome distinguishes three levels: unsuccessful attempt, successful contact,
and completed follow-up.
Outcome enteredLevelEffect
## Unreachable (no
answer)
## Unsuccessful
attempt
The mother stays on the list; new attempt
the next day
Wrong or out-of-
service number
## Unsuccessful
attempt
Record flagged "number to correct"; the
mother stays on the list until corrected
## Reached,
appointment
rescheduled
## Successful
contact, follow-
up completed
New date entered, visit postponed,
reminders rescheduled; the mother leaves
the list
Reached, no
longer wants
follow-up
## Successful
contact, follow-
up completed
Follow-up ends for this absence; if she asks
to stop messages, her withdrawal of
consent is recorded
9.4 Consent and traceability
CodeRule
BR-16Withdrawal of consent is immediate: scheduled reminders are
cancelled, the mother leaves the follow-up list, and the record is
archived. Complete deletion is available on request.
BR-17Every modification of a record (EDD, phone, statuses, consent) logs the
author, the date, and the old and new value.
## 9.5 Administration
CodeRule
BR-18The first administrator account is created at installation. The administrator
creates clinics and their manager accounts; each clinic manager
creates the staff accounts of their own clinic.
BR-19A new account receives a temporary password that must be changed
at the first login.
BR-20Deactivating a clinic blocks the login of all its users and keeps its data

CodeRule
and history.
BR-21Only the administrator can change calendar rules and system settings. A
change applies to visits created afterwards, and each change is logged
(author, date, old and new value).
BR-22The administrator never has access to mothers' records or contact
details.
- Initial functional requirements
These requirements are preliminary and will be refined through use cases and
acceptance criteria. Seventeen of the twenty-two requirements are in the MVP; FR-09,
FR-12, FR-13, FR-14, and FR-15 are planned for version 2.
CodeRequirementVersion
FR-01The system will allow a mother to be registered with her
explicit consent (name, phone, estimated due date or child's
date of birth, clinic).
## MVP
FR-02The system will allow staff and administrators to authenticate
and will manage accounts.
## MVP
FR-03The system will distinguish the rights of each role and limit
each user, except the administrator, to their clinic.
## MVP
FR-04The system will generate the antenatal, postnatal, and
immunization visit calendar based on configurable rules.
## MVP
FR-05The midwife or health worker will be able to record the
attendance, absence, or postponement of a visit.
## MVP
FR-06The system will schedule reminders 48 and 24 hours before
each visit.
## MVP
FR-07The system will send reminders through a simulated channel
and keep a sending log.
## MVP
FR-08The system will stop all sending when a mother withdraws her
consent.
## MVP
FR-09The system will offer a danger sign checker that directs the
user to the clinic, without diagnosing.
## V2
FR-10The system will produce each day the list of mothers who
missed a visit, with their contact details.
## MVP

CodeRequirementVersion
FR-11The midwife or health worker will be able to record the
outcome of a follow-up contact among predefined
outcomes.
## MVP
FR-12The system will display educational cards in several
languages, with their review status.
## V2
FR-13The clinic manager will be able to manage educational
cards and will only publish a reviewed, sourced card.
## V2
FR-14The system will produce an aggregate report for the clinic.V2
FR-15The system will produce an aggregate report for the NGO,
without personal data.
## V2
FR-16The system will protect health data and prevent access to
records outside the authorized scope.
## MVP
FR-17The system will keep a history of access and important
modifications.
## MVP
FR-18The system will recalculate the calendar and reminders when
the due date changes, a visit is postponed, or the birth is
recorded.
## MVP
FR-19The system will distinguish an unsuccessful contact attempt, a
successful contact, and a completed follow-up.
## MVP
FR-20The system administrator will be able to create and
deactivate clinics and the accounts of clinic managers and
NGO officers.
## MVP
FR-21The system administrator will be able to configure the
calendar rules and the system settings.
## MVP
FR-22The system administrator will be able to view the system-wide
history of accesses and modifications, without access to
health data.
## MVP
- Initial non-functional requirements
The privacy of health data takes priority over any other criterion; the requirements
below follow from it.

•Security and privacy: encrypt health data in transit and, where possible, at rest;
hash passwords; verify authorizations on the server side; temporarily lock an
account after five failed logins; end the session after a period of inactivity.
•Data minimization: collect only what is needed for follow-up (name, phone, due
date or date of birth, clinic); no medical information in follow-up notes.
•Consent: send no message without explicit agreement, and respect the
withdrawal of consent.
•Discreet messages: write reminders without medical detail.
•Clinical content: display only content reviewed by a health professional and
drawn from recognized sources (WHO, DRC Ministry of Health, recognized NGO).
Never diagnose, and always recommend a visit to a qualified professional.
•Tone and language: avoid shaming wording and assumptions about users'
identity.
•Usability: simple interface suited to phones and limited connections, in several
languages.
•Maintainability: organize the code into modules, with a sending channel that
can be replaced by a real provider.
•Integrity: define primary keys, foreign keys, constraints, and consistency rules in
the database.
•Validation: validate input data in both the interface and the server.
•Error consistency: use appropriate HTTP responses and a uniform structure for
error messages.
•Traceability: keep a history of access and important modifications, including
administrator actions (FR-17, FR-22).
•Administration security: require a new password at first login and limit
administrator rights to platform management, with no access to health data.
•Report confidentiality: in version 2, hide any NGO indicator computed on fewer
than five mothers.
•Data retention: set the retention period with the partner clinic, in line with DRC
regulations.
•Testing: verify calendar generation, due date change and postponement,
reminders, the follow-up list, contact outcomes, permissions (including the
administrator role), and consent withdrawal.
•Documentation and reproducibility: describe the installation, configuration,
endpoints, and main decisions, in a documented environment.
No quantitative performance or availability targets typical of a production system are
set, since they are not part of the scope of the training.
- Risks and pending decisions
Three risks determine the project's success: access to a partner clinic, the medical
review of content, and compliance with data regulations.

TopicRisk or pending decision
Health dataRecords contain sensitive information; protecting it
is a priority. Minimization, access control, and a
history of accesses apply from the MVP.
Data protection regulationThe data protection regulations applicable in the
DRC will be reviewed with a legal advisor before
the pilot.
Message confidentialityA reminder received on a shared phone may
reveal a pregnancy; messages stay discreet and
consent explicit.
Medical contentCards and the questionnaire must be reviewed by
a health professional before any real use; both are
planned for version 2.
Calendar rulesThe visit rules (antenatal, postnatal, immunization)
start from WHO recommendations and are
adjusted to national protocols with a health
professional.
SMS and WhatsApp providerActual sending has a cost, and WhatsApp requires
approval; it is postponed until after the first version.
Access to clinicsObtaining one or two partner clinics for a pilot is a
challenge, and it determines the real value of the
project.
Local languageThe language must be chosen and a validated
translation obtained before adding it; it is planned
for version 2.
Data entry by clinicsThe follow-up list is only reliable if clinics record visits
correctly; the "Status to confirm" section and light
data entry reduce this risk.
Administrator accountA single powerful account is a security risk; it is
limited to platform management, protected by a
strong password, and all its actions are logged.
Retention and deletionThe retention period is set with the partner clinic,
and complete deletion is available on request.
Revenue modelRevenue depends on NGOs, donors, and clinics,
and will come late; sponsored content is ruled out.
Academic timeThe number of features must be adjusted to the

TopicRisk or pending decision
training schedule; the MVP is limited to follow-up
and the rest moves to version 2.
- User stories
The user stories follow the modules described in section 8. The priority indicates the
importance of each story and its version, the Requirement column relates it to the
functional requirements in section 10, and the BR-xx codes refer to the business rules in
section 9.
13.1 Authentication and users
IDUser storyAcceptance criteriaPriorityRequirement
US-01Login. As a
staff member
or
administrator,
I want to log
in so that I
can access
the functions
of my role.
Credentials are verified; an
error shows a generic
message that does not
reveal which field is wrong;
without login, protected
pages and API routes return
401; passwords are hashed;
the account is locked for 15
minutes after five failures.
High (MVP)FR-02
US-02Staff account
management.
As a clinic
manager, I
want to
create and
deactivate
my staff's
accounts so
that I control
access.
An account has a
mandatory role and clinic;
the email address is unique;
a new account receives a
temporary password to
change at first login; a
deactivated account can
no longer log in but its
history is kept; the manager
only manages their own
clinic's staff.
Medium (MVP)FR-02
US-03Access
separation. As
the system
owner, I want
each user to
access only
the data
allowed by
The midwife and the
manager only see their
clinic; the NGO officer and
the administrator see no
personal data; the server
returns 403 to any out-of-
scope request, including a
direct API call; each row of
High (MVP)FR-03, FR-16

IDUser storyAcceptance criteriaPriorityRequirement
their role so
that mothers'
privacy is
protected.
the matrix in section 7.9 is
covered by a test.
13.2 Patient record and consent
IDUser storyAcceptance criteriaPriorityRequirement
US-04Registration
with consent.
As a
midwife, I
want to
register a
mother with
her
agreement
so that she
receives
reminders.
Name, phone, estimated due
date (EDD) or child's date of birth,
and clinic are required; the
phone has a valid format; the
EDD falls within the next 42 weeks
and the date of birth within the
last 24 months; consent is
recorded with its date, channel
(SMS or WhatsApp), and author;
without consent, no record is
created and no message is sent.
High (MVP)FR-01
US-05View and
edit the
record. As a
midwife, I
want to view
and edit a
mother's
record so
that I keep it
up to date.
Information and calendar are
visible; changes are validated
and logged (author, date, old
and new value); an EDD change
recalculates visits and reminders
(BR-03); a wrong number can be
corrected.
High (MVP)FR-01, FR-17,
## FR-18
US-06Withdraw
consent. As
a mother, I
want to
unsubscribe
so that I no
longer
receive
messages.
In the MVP, the midwife records
the withdrawal at the mother's
request; it takes effect
immediately: no message is
scheduled or sent and scheduled
reminders become "cancelled";
the mother leaves the follow-up
list; the withdrawal is logged; in
version 2, a STOP reply will have
the same effect.
High (MVP)FR-08

13.3 Visit calendar
IDUser storyAcceptance criteriaPriorityRequirement
US-07Generate the
calendar. As a
midwife, I want
the visit
calendar to be
generated
automatically
so that I can
tell the mother
her upcoming
appointments.
Antenatal, postnatal, and
immunization visits are created
from the EDD or date of birth
(BR-01); rules are configurable;
visits already in the past are
not created (BR-02); the
calendar is shown in date
order with type and status;
when the birth is entered,
remaining antenatal visits are
closed (BR-04).
High (MVP)FR-04, FR-18
US-08Record
attendance. As
a midwife, I
want to note
that a mother
came, was
absent, or
postponed so
that I can track
her
attendance.
The statuses are planned,
attended, absent, postponed;
an upcoming visit cannot be
marked attended or absent; a
postponement requires a new
future date and keeps the old
one (BR-06); each update
records its date and author;
an absence feeds the follow-
up list.
High (MVP)FR-05, FR-18
## 13.4 Reminders
IDUser storyAcceptance criteriaPriorityRequirement
US-09Receive
reminders. As
a mother, I
want a
reminder 48
and 24 hours
before each
visit so that I
never miss
one.
Two reminders are scheduled
per visit, at D-2 and D-1
(BR-08); none for a past visit;
the message is discreet, with
no medical detail (BR-11); if
the visit is attended or
postponed, unsent reminders
are cancelled and, for a
postponement, rescheduled
on the new date; nothing is
sent without consent.
High (MVP)FR-06, FR-08,
## FR-18
US-10Sending log.
As a clinic
manager, I
Each reminder has a status
(scheduled, sent, failed,
cancelled); sending is
Medium (MVP)FR-07

IDUser storyAcceptance criteriaPriorityRequirement
want to see
the status of
reminders so
that I know
which ones
were sent.
simulated in the MVP; a failed
sending is retried once; the
log can be filtered by date
and by status.
13.5 Danger sign checker
IDUser storyAcceptance criteriaPriorityRequirement
US-11Check
danger
signs. As a
mother, I
want to
answer a
short
questionnair
e so that I
know
whether I
should go to
the clinic.
The questionnaire is based on
recognized sources (WHO, Ministry
of Health) and reviewed by a
health professional before any use;
if at least one sign is ticked, the
result asks to go to the clinic or
emergency services immediately;
otherwise, it recommends discussing
it with a professional at the next visit;
no diagnosis or treatment advice;
no answer is stored with the person's
identity.
High (V2)FR-09
13.6 Clinic follow-up
IDUser storyAcceptance criteriaPriorityRequirement
US-12Daily
follow-up
list. As a
midwife, I
want the
list of
mothers
with an
unresolve
d
absence
so that I
can call
them.
The list is generated each morning
(BR-13); it shows name, phone,
missed visit (type and date), days
elapsed, and number of attempts;
it contains only the clinic's mothers;
a "Status to confirm" section groups
visits with no status (BR-07); mothers
who withdrew consent do not
appear.
High (MVP)FR-10

IDUser storyAcceptance criteriaPriorityRequirement
US-13Record
the follow-
up. As a
midwife, I
want to
note the
outcome
of my call
so that I
can track
the
contacts
made.
Outcomes are predefined:
unreachable, wrong number,
reached with appointment
rescheduled, reached and no
longer wants follow-up; each
attempt is dated and attributed;
the system distinguishes
unsuccessful attempt, successful
contact, and completed follow-up
(section 9.3); "rescheduled" requires
a new date and completes the
follow-up; after three unsuccessful
attempts, the case becomes "not
reached" (BR-14); the mother
leaves the list only when the follow-
up is completed or the case is not
reached.
High (MVP)FR-11, FR-19
13.7 Educational cards (version 2)
IDUser storyAcceptance criteriaPriorityRequirement
US-14View the
cards. As a
mother, I
want to read
short cards
on nutrition,
danger signs,
and infant
care so that I
stay
informed.
Cards are available in French
and English; only published
(therefore reviewed) cards are
visible, without login; they can
be filtered by theme and
language; each card shows its
source; the content avoids
shaming wording.
## Medium
## (V2)
## FR-12
US-15Manage the
cards. As a
clinic
manager, I
want to
create and
edit cards so
that content
stays up to
Each card has a language, a
theme, a source, the reviewer's
name, and the review date;
statuses are draft, reviewed,
published, archived; publishing
is impossible if the source,
reviewer, or date is missing; a
published card that is edited
goes back to "needs review"
and is unpublished until
## Medium
## (V2)
## FR-13

IDUser storyAcceptance criteriaPriorityRequirement
date.reviewed again.
## 13.8 Reports (version 2)
IDUser storyAcceptance criteriaPriorityRequirement
US-16Clinic report.
As a clinic
manager, I
want to see
enrolled
mothers, visit
attendance,
and
completed
follow-ups so
that I can
track activity.
Indicators are enrolled
mothers (active and
withdrawn), attendance rate
(attended ÷ attended +
absent), absences,
unsuccessful attempts,
successful contacts,
completed follow-ups, and
reminders sent or failed; they
are calculated from recorded
data, can be filtered by
period, and show no names; a
message is shown when there
is no data.
## Medium
## (V2)
## FR-14
US-17NGO report. As
an NGO
officer, I want
to know the
percentage of
mothers who
attended their
third antenatal
visit so that I
can assess my
program.
The percentage covers
mothers whose visit was due
during the period; the report
aggregates several clinics; it
contains no personal data; it
can be filtered by clinic and
period; an indicator
computed on fewer than five
mothers is hidden.
## Medium
## (V2)
## FR-15
## 13.9 Administration
IDUser storyAcceptance criteriaPriorityRequirement
US-18Manage clinics
and manager
accounts. As
the system
administrator, I
want to create
and deactivate
A clinic has a unique
name and a city; a
manager account is linked
to exactly one clinic; the
email address is unique; a
new account receives a
temporary password to
High (MVP)FR-20, FR-03

IDUser storyAcceptance criteriaPriorityRequirement
clinics and their
manager
accounts so
that each clinic
can start using
the system.
change at first login;
deactivating a clinic
blocks the login of all its
users and keeps its data
(BR-20); the administrator
sees no mother's record
## (BR-22).
US-19Configure rules
and settings. As
the system
administrator, I
want to adjust
the calendar
rules and the
system settings
so that the
system follows
the protocols of
the clinics.
Visit types, timing,
reminder time, retry count,
and follow-up attempt
limit can be edited; values
are validated (for
example, gestational
weeks between 1 and 42);
a change applies to visits
created afterwards
(BR-21); each change is
logged with author, date,
and old and new value;
only the administrator can
change them.
Medium (MVP)FR-21, FR-04
US-20View the
access history.
As the system
administrator or
a clinic
manager, I
want to view
the history of
accesses and
modifications
so that I can
detect misuse.
Each entry shows the
author, the action, the
date, and the record
reference, without health
details; the history can be
filtered by user, action,
and date; the manager
only sees their own clinic;
the administrator sees the
whole system.
Medium (MVP)FR-17, FR-22