--> all_scripts_harshita.txt:		Cleaned list of unique names of 1133 scripts. This is different from Harshita_scripts.txt which has all names converted to lowercase and having single underscore.

--> The above file is split into a batch of 100 scripts resulting into 12 sub_files namely all_scripts_harshita_aa, all_scripts_harshita_ab, ..., all_scripts_harshita_al.

--> Following 4 files are created for each batch of files, i.e each following file has information about 100 files, last file being 33 scripts only.

1. dialogues.txt:		Contains dialogue to speaker mapping for all the dialogues that could be extracted from a set of 100 scripts. Look for the pattern "****Dialogues from script :" to get block of each script.

2. speakers_list.txt:		Contains a list of speakers for a set of 100 scripts. Look for the pattern "****Speakers from script :" to get block of speakers for each script.

3. blocks.txt:		Contains extracted blocks for the set of scripts.
4. Candidate_scripts.txt:		This has the percentage dialogue extraction information about a set of scripts.


--> failed.txt:		Contains the list of 127 scripts for which no speakers/dialogues were extracted, or extraction % was > 100 (dividing the script into blocks failed).

--> gdrive link to all files:		https://drive.google.com/file/d/1Lilxm825bO21qQEtzT0BKvGgp0PkMn3m/view?usp=sharing 
