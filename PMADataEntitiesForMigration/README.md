Project management and accounting module has some gaps when it comes to migrating data in to the D365 for finace and Supply chain. This project has multiple entities with staging tables and security privilages,which can be utlized to fill in those gaps. If you want to utilize these entities,download this project and import it using visual studio.Once imported perform following steps
	- Build the solution
	- Synchronize the database.
	- Once DB sync is successful, Open F&O UI andnavigate to, Data Management > Framework Parameters > Entity setting > Refresh entity list
	- Entities are ready for migration using data management import projects.
