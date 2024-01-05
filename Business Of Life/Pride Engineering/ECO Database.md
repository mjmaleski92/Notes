This is meant to be a collection of all the details needed to understand the structure and setup for the ECO Database.

---
#Hardware
The database is currently comprised of a Postgresql database which is hosted locally on a computer [[dave-holmespc]] ip address:192.168.0.161

![[Diagram.svg]]

---

#PostgreSQL
Here is a relational diagram of the database:
![[ECO Database Relational Diagram.png]]

The database also has several triggers and functions that reside in the main table_startup.psql file.

---
#Python #Backend #Flask

All modules utilized should be included in the requirements.txt file inside the project folder.
A #virtualenvironment is being used (.venv) so that all the python modules and dependencies won't conflict with globally installed variables.
**Key Files**
- **main.py** -this is the file which houses all the flask endpoints and controls all the flow of the program
- **database_interface.py** -handles all the transactions with the database as well as handling all the creation of new folders to place attachments onto the [[Sharepoint]] site

---
#Frontend #Bootstrap #Javascript #HTML
- **templates folder** - this houses all the html files required for flask render_templates method
- **static folder** -houses all the javascript and logo/picture files
	- **filter.js** - this applies the filtering to the main database view so that a drop down appears and allows the user to select what type of ECO status they want to see (Default is everything except for "Closed")
	- **script.js** - this grabs all the information from the database to store into the headers and the table dynamically
	- **style.css** - main stylesheet for everything, most everything else is utilizing bootstrap which brought in via CDN in the header of html files
