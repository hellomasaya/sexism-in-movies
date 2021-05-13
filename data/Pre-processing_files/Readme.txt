1. ScriptId_title.txt	Extracted from movieObj.txt (movieObj.js). Contains a complete list (7571 entries) of script id to script name mapping. 

2. characters.tsv		Converted from character_list5.csv (had some encoding issues; unrecognizable characters). Contains “script_id	imdb_character_name	words	gender	age”

3. movieId_title_char.txt	Contains 2000 no. of movie ids with name mapping for which characters could be extracted by polygraph people from their movie scripts (contains only those character names for whom spoken words were > 100).  

4. Harshita_scripts.txt	Cleaned list of the scripts (Original 1170 reduced to 1133 scripts after removing redudant scripts); names converted to lowercase with single underscore for the ease of matching with Polygraph's Film Dialogue Dataset.

5. matched_scripts_polygraph_vs_harshita.txt	Names of the 761 scripts which are common in Polygraph dataset and Harshita’s scripts.

6. polygraph_matched_scriptid_title_gender.txt	This file has complete information of characters (having no. of spoken words > 100) in a movie script (Harshita Vs. Polygraph) along with the gender information. Headings: “Matched/Unmatched	script_name/title	script_id	imdb_character_name	gender”. This is the final file which can be used for true labels for a given script. "Matched" refers to the common script (761 scripts are matched out of 1137).

NOTE: The gender information for each character for a script has been picked up from the Github link: "https://github.com/matthewfdaniels/scripts" which has 9254 scripts in principle out of which Polygrpah people could scrape 7571 scripts. Out of these scripts, only 2000 script's characters could be extracted by them. We have compared those 2000 movie titles to our 1137 scraped scripts, out of which we could get 761 matching entries/scripts. The speaker names  extracted by our program are more in number that the ones extracted by Polygraph as they pick the only ones having spoken words > 100 (we haven't put any filter as of now). Also, speaker names are a bit different in some scripts; like full name mentioned in the polygraph file (eg: bianca stratfor) and only half name mentioned in our script (eg: bianca). We'll have to see if model can predict gender in sufficient no. of cases accounting for this difference.

Speaker list for script "10_things_i_hate_about_you" given by our program looks like: 
rider
kat
bianca
boy
girl
miss perky
cameron
patrick
michael
derek
joey
teacher
mandella
mandelia
cohort
sharon
walter
pepe
trevor
scurvy
bruce
skippy
lead singer
bogey
guy
clem
cowboy 

While the Polygraph character gender information looks like:
1512	bianca stratfor	3068	f	18
1512	cameron james	2022	m	18
1512	chastity	260	f	27
1512	derek	204	m	NULL
1512	joey donner	1294	m	20
1512	kat stratford	4718	f	18
1512	mandella	946	f	25
1512	michael	2312	m	21
1512	mr. chapin	122	m	49
1512	patrick verona	3346	m	20
1512	teacher	182	m	45
1512	walter stratfor	1206	m	46

And the processed extracted speaker list for the matched movie in Polygraph(1899) Vs. Our(1160) Dataset looks like:
(Un)/Mmatched	script_name	script_id	imdb_character_name	gender
Matched	10_things_i_hate_about_you	1512	bianca stratfor	f
Matched	10_things_i_hate_about_you	1512	cameron james	m
Matched	10_things_i_hate_about_you	1512	chastity	f
Matched	10_things_i_hate_about_you	1512	derek	m
Matched	10_things_i_hate_about_you	1512	joey donner	m
Matched	10_things_i_hate_about_you	1512	kat stratford	f
Matched	10_things_i_hate_about_you	1512	mandella	f
Matched	10_things_i_hate_about_you	1512	michael	m
Matched	10_things_i_hate_about_you	1512	mr. chapin	m
Matched	10_things_i_hate_about_you	1512	patrick verona	m
Matched	10_things_i_hate_about_you	1512	teacher	m
Matched	10_things_i_hate_about_you	1512	walter stratfor	m	 
