## Preprocessing Instructions

### Starting the app

- In PyCharm: First make sure you pulled the most recent version of the Github repository
- Select correct branch - “main_edit_config_file_as_txt”
- Open “main_app.py”, then run it (green “play” button at the top of the window) 
- Choose the first option: “Processing and oranization”
- Now a window called “Alice Data Processing App” should open. This is where we’ll do the preprocessing.

### Reorganizing the folders

- For the app to work, we need the subject data folders to only have one level of subfolders.
- Initially, subject folders (ex. "Sub151") will be have 4 or 5 folders depending on the project. Usually named "Part1", "Part2", "Part3", "Training", and in some projects you may have other folders such as "WBT" or others.
- Inside these folders, you will find the actual data subfolders (eg. "Sub-151_Plan-Part1_UI_RunID-20230522-145026")
- Take these subfolders and move them to the main subject folder (in this case, from "Part 1" folder, to "Sub151" folder), and delete the empty "Part 1" etc. folders.
- According to the processing being made, you may not need to do this for folders such as "Training". 
- Now the folder should be ready for preprocessing.

### Preprocessing

- First, at the top left of the “Alice Data Processing App” window, choose “file” and then “browse”. 
- Select the subject data folder you wish to preprocess (for example “Sub151”) and press the “Select Folder” button.
- Now, in  the app window, press the small button in the middle, just above all the other buttons. It usually says “WTB” when you just open it. Select SOA.
- This will open a text file. In it, make sure that under “directory:” and “base_directory_for_run_all:” you see the path of the folder you just selected (eg. C:\user\...).
- Still in the text file, make sure that under “sub_dirs:” you see the subfolders of the different parts of the experiment. These are the folders that will be preprocessed.
- Note: the app will only process the folders under "sub_dirs:". This is useful because you can choose to process only some of the folders or all of them.
- Once you’re done, save and exit the text file.
- In the data processing app window, select “Run All”.
- The app will freeze for about 2 minutes, while it processes the data.
- New CSV files will appear in the main folder of the repository. Usually it’s C:\Users\(your username)\Documents\GitHub\alice_data_analyze-main
- There should be 5 new CSV files for each subfolder you ran through the app, so usually 15.
- Now you can move these CSV files to a folder of your choosing. 
- You’re now ready to process the next subject. You will only need to choose “file”>”Browse”>Select folder>”Run All”, no need to open the text file if it selected the folders properly the first time.
        

### Troubleshooting
- Sometimes the app returns “DEBUG: invalid literal for int() with base 10: 'n'” and doesn’t finish processing all the files. In this case, open the text file by pressing the small middle button in the app, and selecting SOA. Then manually erase some of the subfolders you’re running under “sub_dirs:”. Running only one subfolder at a time should work, and not create more errors.
