# 28 Software Development Lifecycle Policy

## 28.1. Purpose 
The purpose of the Software Development Life Cycle (SDLC) Policy is to describe the requirements for developing and/or implementing new software and systems and to ensure that all development work results in software that is secure, protects patient privacy, and complies with all regulatory requirements.

## 28.2. Scope
This policy applies to all Quantel AI employees responsible for software development.

## 28.3. Policy
Quantel AI follows an agile model for software development, including design reviews of new software and features as well as continuous integration of code. New software, features, and customizations are reviewed by relevant stakeholders, relevant stakeholders listed, as well as the CEO as needed. 
All new code is reviewed by another developer, and all code must pass required tests before a change can be merged to the master branch.  Code is managed through GitHub and restricted to authorized personnel in the Development team. Sprints are performed on a regular basis.

Development, testing, and production environments are all separate. This separation permits better management and security for the production system, while facilitating greater flexibility in the development environment.

## 28.4. Software Development Phases
Quantel AI’s software development process is composed of the following phases. 

Software Concept Proposal and Review: This phase transforms the identified use case into an approved design document.
 * Definition of product
 * Definition of security and privacy requirements
 * Technical specifications document

Software Development and Testing
 * Code development for new software (see Change Management Procedure)
 * Manual and automated testing, including QA and security tests, conducted and documented
 * Resolution/remediation of any problems identified during testing
 * Final security assessment by CISO or designated authority

Software Release and Maintenance
 * Software moved from development environment to production environment
 * Customer support and operational support structure established
 * Continuous security testing conducted at regular intervals
 * Security or functionality issues identified, resolved, and documented (see Change Management Procedure)

## 28.5. Change Management
Application and infrastructure related changes follow an established change management process for the Quantel AI environment. When service teams or customer representatives enter a request for a change, the request is assigned to one of three severity levels based on the nature and impact of the change:
 * Standard – A normal change
 * Normal (Low Impact or High Impact) – A non-emergency or non-routine change with either low or high impact on the system
 * Emergency – A risk that must be remediated as quickly as possible.
Changes to software, service infrastructure, or internal systems must adhere to Quantel AI’s change management procedure.

See Change Management Procedure for additional details.

## 28.6. Testing
Testing is performed through automated and manual processes, and includes:
a. Unit testing
b. Functional testing
c. Security testing
Unit tests, functional tests, and security tests (including static code analysis) are automated and no change can be committed to the Github repository until all of those are passing.  Additional testing is conducted following manual processes prior to delivery to customer.

## 28.7. Deployment
Code is moved from pre-production environments to production through the use of the Deployment/Continuous Integration Tools. These tools are restricted to the Engineering team.

## 28.8. Exceptions
Exceptions to this policy shall be permitted only if approved by CISO or other designated authority, including Executive Management and should be reported according to the Exceptions Management Policy
