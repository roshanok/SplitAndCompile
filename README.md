# SplitAndCompile

This script is to split or combine or merge the files
```
--------------------------------------------------------------
Usage: SplitAndCombine.py [-h] [-i INPUT] [-s] [-n CHUNK] [-m]\n
optional arguments:
-h, --help            show this help message and exit
-i INPUT, --input INPUT
                    Provide the File that needs to be Split
-s, --split           To Split the File
-n CHUNK, --chunk CHUNK
                    [n]: No. of files to be created
                    [n]kb : Split the file in nKB size
                    [n]b : Split the file in nb size
                    [n]mb : Split the file in nmb size
                    [n]gb : Split the file in ngb size

-m, --merge           Merge the Files


examples :
SplitAndCombine.py -s -i first_project.zip -n 5
SplitAndCombine.py -s -i first_project.zip -n 5kb
SplitAndCombine.py -s -i first_project.zip -n 2gb
SplitAndCombine.py -s -i "c:\temp\first_project.zip" -n 5
SplitAndCombine.py -m -i first_project.zip
SplitAndCombine.py -m -i "c:\temp\\first_project.zip"
----------------------------------------------------------------
```

The split also creates an additional file as .CRC. and then is compared while merging to check if merging is successful
Note : This is not a CRC check, but does good to ensure file is merged properly

            # create the content for the file copy check
            data_length = len(data)
            self.check_list += str(data[:5]) + str(
                data[int(data_length / 2) - 1:
                     int(data_length / 2) + 1]) + str(data[-5:])


```
Examples :

python SplitAndCombine.py -s -i "New folder\first_project.zip" -n 700kb

output
Splitting the File Now
Total file Size : 8162474
Splitting into 12 files of 700kb size
Creating New folder\first_project.zip-1.ros
Creating New folder\first_project.zip-2.ros
Creating New folder\first_project.zip-3.ros
Creating New folder\first_project.zip-4.ros
Creating New folder\first_project.zip-5.ros
Creating New folder\first_project.zip-6.ros
Creating New folder\first_project.zip-7.ros
Creating New folder\first_project.zip-8.ros
Creating New folder\first_project.zip-9.ros
Creating New folder\first_project.zip-10.ros
Creating New folder\first_project.zip-11.ros
Creating New folder\first_project.zip-12.ros
Creating the check file : New folder\first_project.zip-CRC.ros
File split successfully
```

```

python SplitAndCombine.py -m -i "New folder\first_project.zip"
Merging the file to New folder\first_project.zip
File Already Exist. Please remove the C:\Roshan\ZIP\New folder\first_project.zip and then re-run.

Do you want to remove the file [Y/N] : y
Merging the file first_project.zip-1.ros
Merging the file first_project.zip-2.ros
Merging the file first_project.zip-3.ros
Merging the file first_project.zip-4.ros
Merging the file first_project.zip-5.ros
Merging the file first_project.zip-6.ros
Merging the file first_project.zip-7.ros
Merging the file first_project.zip-8.ros
Merging the file first_project.zip-9.ros
Merging the file first_project.zip-10.ros
Merging the file first_project.zip-11.ros
Merging the file first_project.zip-12.ros
Checking if the files are merged properly
File check : Passed
File Merged successfully
```
