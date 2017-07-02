# Product Plan - Tehut Getahun

## Learning Goals
- Use the opportunity of working on the Transparent Classroom API to navigate and contribute to an existing codebase. 
- Learn to generate and manage PDFs from the browser
- Learn to use Google Container Engine to containerize my final product
- Learn to deploy to the cloud--either with Heptio AWS Kubernetes quickstart or Google Computer Engine

## Problem Statement

Wedgwood Montessori (WMS) parents enter student data into our Transparent Classroom student management system and every session WMS adminmistrators spend time formatting and manipulating that data to generate registration invoices and classroom documents as a part of repetitive workflows that are prime candidtates for automation.



## Market Research

- Competitor apps
The primary competition for my app is not another app but the existing manual workflows for generating registration invoices and classroom documents. The current workflow for sending registration inbvoices requires administrators to download a list of new registrants each day, manually log into our Quickbooks online website, manually create a new customer and manually generate and send an invoice.

WMS recieves between 80-120 applications per enrollment session. 

Similarly, the process for generating classroom documents from data entered by parents is also manual. WMS uses Transparent Classroom data to generate the following documents for every term:
- Class List :A numbered and alphabetized list of students 
- Daily Roster: A numbered and alphabetixed list of students that lists only the students registered to attend school on  a given day of the week.
- Birthday List: A chronological list, sorted by Academic Year, of the students in a given classroom and their names and birthdays.
- Allergy List: An alphabetized list of the students in a given classroom with allergies listed on their registration form. The list must contain the student's name and a list of the items to which they are allergic.
- Parent Email List: An alphabetized list of the students in a given classroom, their names, their parents names and their parents email addresses.
- Parent Phone List:  An alphabetized list of the students in a given classroom, their names, their parents names and their parents phone numbers.

Data is downloaded from Transparent Classroom in CSV format and then manully entered into either a new file or an existing document template. A second shortcoming of this existing approach is the introduction of an additional layer of human error.

- Shortcomings of the competition
The primary shortcoming of the current system is the time it takes and the fact that the highly manual processes introduces additional human error.

- My product is different because...
It does not ask WMS administrators to learn new systems but works on top of systmes they already use, takes the familiar inputs and produces the same outputs (forms and invoices) as an administrator would but instead of doing the work, adminstrators only have to begin the process and inspect the results.
## Target Audience

My app targets school adminstrators who are familiar with basic consumer facing technology (email, quickbooks, etc) but do not have an interest in thinking about their technology at all.

## Trello Board
https://trello.com/b/F1TxZlXU/wmsapp  (there isn't really anything up here but my wireframes)

## Technologies

- Back-end Technology
   - Rails Server
	   - Given the small size of my PDF files I am considering moving away from maintaining my own server side code. The primary use that comes to mind is storing previously generated pdfs and given the nature of our data that is a risk that doesn't seem wise.
   - Quickbooks API
   - Transparent Classroom API
   -
- Front-end Technology

    - Backbone for API managment
    - PDFmake Javascript Library
    - Node Quickbooks library to allow for faster development with quickboos
    - React for front end display
- Infrastructure
	-Google Container Engine
	- Either Google Compute Engine or AWS using the Kubernetes Quickstart for AWS by Heptio
<<<<<<< HEAD

=======


## Wireframes
https://trello.com/b/F1TxZlXU/wmsapp
in Trello Board

## MVP Feature Set

1.  WMS Admin can log into TC via WMSApp and generate PDFS of classroom data
- Class List :A numbered and alphabetized list of students 
- Daily Roster: A numbered and alphabetixed list of students that lists only the students registered to attend school on  a given day of the week.
- Birthday List: A chronological list, sorted by Academic Year, of the students in a given classroom and their names and birthdays.
- Allergy List: An alphabetized list of the students in a given classroom with allergies listed on their registration form. The list must contain the student's name and a list of the items to which they are allergic.
- Parent Email List: An alphabetized list of the students in a given classroom, their names, their parents names and their parents email addresses.
- Parent Phone List:  An alphabetized list of the students in a given classroom, their names, their parents names and their parents phone numbers.

2. WMSApp will run a nightly job that downloads all the registrations on a given day and posts invoices to Quickbooks 

3. WMS Admin can log into WMS App and see list of invoices sent to parents who submitted registration forms
	
<<<<<<< HEAD

=======
>>>>>>> upstream/master
