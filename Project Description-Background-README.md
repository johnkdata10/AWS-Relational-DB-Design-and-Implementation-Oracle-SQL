# Project Description/Background
## Client:
Hospital
## Client project statement: 
The purpose of the client Hospital database application is to maintain the data that we generate and to provide an efficient, effective, and friendly health care provision service for our elderly patients.

## Project objectives:
To maintain data on wards.
To maintain data on staff.
To maintain data on patients and their immediate family contacts.
To maintain data on local doctors.
To maintain data on patient appointments.
To maintain data on out-patients.
To maintain data on in-patients.
To maintain data on both surgical and non-surgical supplies, and their suppliers.
To maintain data on ward requisitions.

## 1. Provide a user’s requirements specification for the global views:
Examine the following in detail and identify and compile a user specification for the Medical Director’s and the Charge Nurse’s views.  Create one conceptual data model (EER) for both of the user views. State any assumptions necessary to support your design. Of course, to complete this exercise will require that you may make some assertions about the precise requirements of each user view. Any assumption should be documented along with the view.

### 1a. Medical Director:
The Director is responsible for the overall management of the hospital and must maintain control over the use of resources (including staff, beds, and supplies) in the provision of cost-effective treatment for all patients.
1.	The hospital is composed of many wards. Each ward is managed by a Charge Nurse. The information to be held on each ward includes the ward name, number (e.g. W1), phone number, location (e.g. Block E), number of beds, and the name of the Charge Nurse.
2.	Each ward is allocated staff including (e.g. Charge nurse, senior and junior nurses, doctors, consultants, auxiliaries).
3.	The hospital maintains stock of general supplies. These supplies include both surgical (e.g. syringe, bandages) and non-surgical (e.g. plastic bags, aprons). The details of the general supplies includes item number and name, item description, quantity in stock, re-order level, cost per unit. The hospital also maintains a stock of pharmaceutical supplies (e.g. antibiotics, pain killers). The details of pharmaceutical supplies includes drug number and name, description, dosage, quantity in stock, re-order level, cost per unit.
4.	The details of the suppliers of the surgical, non-surgical and pharmaceutical items are stored. The information stored includes the supplier name and number, address, phone and fax number. Assume that each supplier provides a unique subset of supplies (i.e. no two suppliers provide the same item).
5.	Patients are normally referred to the hospital for treatment by their local doctor. The details of local doctors are stored including their name, clinic number, address, and phone number. Some local doctors are also on staff at the hospital, but many maintain only their private practice.
6.	The details of patients referred to the hospital includes the patient number, name (first and last name), address, phone number, date of birth, marital status, and immediate family contacts (name, relationship, address, and phone number).
7.	When a patient is referred by his/her doctor to attend the hospital, the patient is given an appointment and is examined by a consultant. The details of the appointment are stored including the consultant’s name and number, appointment number, date and time, and examination room (e.g. Room E112). As a result of the examination, the patient is either recommended to attend the outpatient clinic or placed on a waiting list until a bed can be found in a particular ward.
8.	The details of outpatients are stored. The information stored includes the patient details as stated earlier (see 6) and the date and time of the appointment at the outpatient clinic.
9.	The details of patients currently placed in a ward and those on the waiting list for a place on a ward are stored. The information stored includes the patient details as stated earlier (see 6) and the date placed on waiting list, ward required, expected duration of stay, date placed in the ward, and date left the ward.

### 1b. Charge Nurse:
The Charge Nurse has overall responsibility for the management of a single ward. The Charge Nurse is allocated a budget to run the ward and must ensure that all resources (staff, beds, and supplies) are used effectively in the care of patients. The Charge Nurse and other senior medical staff are responsible for the allocation of beds to patients on the waiting list.

1.	The information to be held on each ward includes the details of staff allocated to each ward including the staff number, name, address, phone number, position, and number of hours worked per week and shift (e.g. early, late).
2.	The information stored on each patient on the waiting list includes the patient number, name (first and last name), address, phone number, date of birth, marital status, immediate family contacts, date placed on waiting list, required ward, date placed in ward, expected duration of stay, and date left ward.
3.	When a patient enters the ward they are allocated a bed with a unique bed number. Each patient is prescribed medication and the details of this medication includes the patient number, staff number (of the prescribing staff doctor), drug number and name, units per day, start and finish date. The medication (pharmaceutical supplies) given to each patient is monitored.
4.	Staff are allocated to work in wards, as required. The Charge Nurse of each ward is responsible for allocating nursing staff to each ward. This ensures that the correct complement of staff are on duty for each shift. It is the responsibility of the Charge Nurse to create a staff schedule on a monthly basis. This schedule includes the date, shift (early, late, night), and the staff on duty for that date.
In addition, a patient requiring specialist care can be assigned a specific nurse during a particular shift. This requires the Charge Nurse to maintain a list of specialties for her staff.
5.	When required the Charge Nurse may obtain surgical, non-surgical and pharmaceutical supplies from the central stock of supplies held by the hospital. The information to be stored includes the requisition number, staff name and number, ward number, item number (or drug number), quantity required, date ordered and date received.

## 2. Data Queries
### 2a. Medical Director View
1.	List the details of a specific ward.
2.	List each ward number and a count of the number of beds for each ward.
3.	List each surgical supply and the total quantity in stock, ordered by total quantity in stock descending.
4.	List each surgical supply and a sum of the quantity in stock for each item that has a re-order level greater than 10. 
5.	List the details for each surgical supply item that has a cost per unit greater than $9.00.
6.	List all the suppliers that do not have a phone number on file.
7.	List each supplier and a count of the different products that they currently supply.
8.	List the details for each local clinic and the number of patients that they have referred over the past year. 
9.	List the number of patients treated at the outpatient clinic each day ordered by date.
10.	List all of the patients currently on the waiting list for In Patient services.
### 2b. Charge Nurse View
1.	List the staff number and name of staff in a given ward, ordered by staff name.
2.	List the name of each Charge Nurse on each ward, ordered by ward number.
3.	List the name of each patient that has stayed in a specific bed.
4.	List all of the supplies ordered on a specific day.
5.	List each ward and shift (early, late, etc.) and a count of staff on duty.
6.	List the immediate family contact details for all patients.
7.	List every staff person who provides specialist care on each ward.
8.	List the patient ID and the maximum dosage of the patient taking he highest dosage of a
### 2c. Pharmaceutical View.
9.	List the details for the pharmaceutical supply that is most frequently ordered.
10.	List a count of patient appointments per week.

## 3. Project Logic
I broke this project up into two phases:
1. The design phase, which is the EER.
2. The implementation phase.

I completed the conceptual model of my database in 2 forms: an Entity–Relationship (ER) diagram and a logical model (relational schema). The ER diagram shows all of my entities, relationships and multiplicity. The relational schema lists each entity with all of its attributes as well as all of the primary and foreign keys.

### 3a. Created entity relationship model:
Created a conceptual schema for the view of client Hospital (Medical Director and Charge Nurse) using the concepts of the ER model. To simplify the diagram, only entities, relationships, and the multiplicity are shown. The cardinality ratio and participation constraint of each relationship type are specified. Considering the subjective interpretation of client requirements, all assumptions I made when creating the ER model are provided.

### 3b. Created relational schema
Mapped my high-level conceptual schema logical models. Created the relational schema and identified all attributes as well as my primary and foreign keys.

### 3c. Implementation/Build
After I completed my ER models and relational schema. I used Oracle SQL Developer and AWS RDS to build (implement) the database that I designed. My project implementation includes the following:

### 3d. Tables:
All of the tables specified in my logical model. Following are some additional specifications for table creation:
• Primary keys are assigned in each table.
• All fields are assigned an appropriate data type.
• All fields are assigned an appropriate field length.
