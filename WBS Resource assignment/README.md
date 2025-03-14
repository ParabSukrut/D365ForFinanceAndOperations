When you work on F&O Implementation and implementing project operations or Project management and accounting module you always come across Work breakdown structure. Once you Migrate data in Work breakdown structure you need to assign resources to the task before you publish it. I have blogged about WBS import in this blog.
 
https://elearnd365.com/2024/08/16/working-with-project-work-breakdown-structure-in-project-management-and-accounting/

To assign resources to WBS there is no standard entity exist in the system and the process is complex if you have large amount of data. You can utilize this utility to assign resources to imported WBS. This utility has staging table and classes which reads csv file and stores data in custom staging table by project Id and hierarchy Id. After that all the staging table data is pushed to projPlanVersionAssignment table and finally to method assignResourcesToDraftTask method of class ProjectTask. 

I have provided sample csv file structure which you can use to fill your data. 

Steps you must follow to import resources on WBS. 

1. WBS task level data is imported. Refer my blog post for it.
2. Download the utility and deploy it in your target enviornment. 
3. Download csv template and fill in data from your imported WBS and resource assignments. 
4. Run the utility and select template and execute.

