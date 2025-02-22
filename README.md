## Blood Bank Management System (BBMS)

The Blood Bank Management System (BBMS) is designed to store, process, retrieve, and analyze information related to the administration and inventory management of a blood bank. This system assists blood bank administrators in meeting blood demands by efficiently handling requests from hospitals and managing donor information.

Project Overview

The BBMS aims to bridge the gap between blood donors, recipients, and blood banks through an organized procedural approach. This system is implemented using the Python programming language, leveraging its simplicity and ease of use.

### Features

1. Hospital Panel

Register:

Allows hospitals to create an account by providing their name and password.

Ensures password confirmation before account creation.

Generates a unique hospital ID upon successful registration.

Login:

Requires the hospital to log in using the generated hospital ID and registered password.

Upon successful login, hospital administrators can:

Insert recipient data into the hospital database.

View the list of recipients.

Find a suitable donor for a recipient.

2. Blood Bank Panel

Login:

Requires the admin to log in using the default password ('peopleservice').

Provides access to the blood bank database.

Allows the blood bank admin to:

Insert donor data into the database.

View the list of donors.

Modules

I. Blood_group_selector.py

split(s):

Splits and categorizes blood groups by their Rh factor.

b_match():

Determines blood compatibility using conditional statements.

II. Donor_code.py

Bloodbank_login():

Handles blood bank admin login with a maximum of three trials.

Provides access to update the donor database or view donor records.

TIME Module:

Introduces time delays within the system.

bloodbank_input():

Accepts donor information (name, age, blood group) for entry into the database.

show_don_list():

Displays the list of donors stored in the blood bank database.

III. Hospital_Login.py

input_into_hospital():

Authenticates hospital login using hospital ID and password.

check():

Validates hospital credentials against the database.

register():

Allows new hospitals to register and generates a unique hospital ID.

Supports up to five password attempts before exiting.

Creates a hospital record in the MySQL database.

check_patient():

Searches for patient records and retrieves donor matches if available.

Eject():

Deletes patient requests and updates blood inventory after successful donations.

Match():

Displays compatible donors for a specified blood group.

Login():

Handles hospital login with three attempts before lockout.

Provides access to insert recipient data, view recipients, and match blood groups.

insert_rec_data():

Collects and inserts recipient details into the database.

IV. Recipient_code.py

show_rec_list():

Displays a list of registered recipients.

V. Sql_functions.py

fetch():

Retrieves required data from specified tables.

### Limitations

Despite the system's capabilities, it has a few limitations:

Character User Interface (CUI): Requires manual text input, reducing interactivity.

Duplicate Names: The system cannot handle multiple recipients/donors with the same name.

Date Input: Incorrect date formats cause errors that are not handled by exception blocks.

Unmasked Passwords: Password input is not hidden, reducing security.

Prerequisites

Python 3.x

MySQL Database
