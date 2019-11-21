# Unzipping files and attaching provenance timestamps

By using ListFile processor, we can track provenance timestamp (in our case file.creation time). Unpack content processor is used to unzip the file. For attaching provenance time stamp which we’ve taken from ListFile processor, we’re using updateAttribute processor. In updateAttribute processor we create a property called filename (variable) and provide a value in an expression language.

	${filename:substringBeforeLast('.')}_${file.creationTime}.${filename:substringAfter('.')}
By using this we can update file name with the timestamp. RoutOnAttribute is used to check for the specific files. And in ExecuteScript we checked whether zip files contains the required count and sent to the respective locations.
