# Provenance timestamp usecase
In this use case, we take zip files from local, append provenance timestamp to all the file names and check (count) whether particular zip file contains all the files, if then pass those files to the destination folder.


UnpackContent processor is used to unzip the files.

ListFile processor gives provenance timestamp as an attribute. This attribute can be used in UpdateAttribute processor to append this provenance timestamp to the filenames.

By using RouteOnAttribute and ExecuteScript processors we can filter files and check the count of the files. In ExecuteScript we write python script to check the count. 
