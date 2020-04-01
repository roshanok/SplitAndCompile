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
