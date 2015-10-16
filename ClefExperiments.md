# CLEF Test Collections

Developers of each system were invited to create scripts that would index and search across several test collections from [TREC](http://trec.nist.gov/) and [CLEF](http://www.clef-initiative.eu). The TREC collection considered in these experiments is the GOV2 collection with three sets of TREC queries: 701--750, 751--800, and 801--850.  The table below summarizes the main details about the CLEF collections in 12 different European and non-European languages, considered in the experiments; all the data can be freely downloaded by means of the [DIRECT](http://direct.dei.unipd.it/) system.


## Test Collections

Language   	| Corpora           							  		|  Encoding   								| # docs | # topics	|
:-----------|:------------------------------------------------------|:------------------------------------------|-------:| --------:|
Bulgarian  	| SEGA2002 <br /> STANDART2002 							| UTF-8										| 69195  | 	149    	|
German     	| FRANKFURTER1994 <br /> SDA1994 <br /> SPIEGEL1994 <br /> SPIEGEL1995  	| ISO-8859-1			| 225371 |	155  	|
Spanish    	| EFE1994 <br /> EFE1995						  		| ISO-8859-1								| 454045 |	97   	|
Persian	   	| HAMSHAHRI		 								  		| UTF-8										| 166774 |	100	 	|
Finnish	   	| AAMULEHTI1994 <br /> AAMULEHTI1995			  		| ISO-8859-1								| 55344	 | 	120	 	|        
French	   	| LEMONDE1994 <br /> LEMONDE1995 <br /> ATS1994 <br /> ATS1995	| ISO-8859-1						| 177452 |	99 	 	|	
Hungarian  	| MAGYAR2002									  		| UTF-8										| 49530  |  148	 	|
Italian	   	| AGZ1994<br /> AGZ1995 <br /> LASTAMPA1994 			| ISO-8859-1(AGZ) <br /> US-ASCII(LASTAMPA)	| 157558 |  90	 	|
Dutch	   	| ALGEMEEN1994 <br /> ALGEMEEN1995 <br /> NRC1994 <br /> NRC1995	| ISO-8859-1					| 190604 |	156     |
Portuguese 	| FOLHA1994 <br /> FOLHA1995 <br /> PUBLICO1994 <br /> PUBLICO1995  | ISO-8859-1					| 210734 |	100	    |	
Russian		| IZVESTIA1995									  		| UTF-8										| 16716  |	62	    |
Swedish		| TT1994 <br /> TT1995							  		| UTF-8										| 142819 |	103	    |

### Topic Sets

Language   	| Topic Set 		| Topid IDs  												| Topic file        |  					  		
:-----------|------------------:| :---------------------------------------------------------|:-----------------|
Bulgarian  	| AH Mono BG		| 251-291	293-325;	351-375; <br /> 401-450 			| bg_topics.xml 	|
German     	| AH Mono DE		| 41-43; 45-143; 145; 147-169; <br /> 171-190; 192-200		| de_topics.xml 	|
Spanish    	| AH Mono ES		| 41-49; 60; 62-69; 80-99; <br /> 110-119; 130-149; 160-168; <br /> 170-179; 190-200 | es_topics.xml 	|
Persian	   	| AH Mono FA		| 551-650													| fa_topics.xml 	|
Finnish	   	| AH Mono FI 		| 92; 94-95; 98; 100; 102-103; <br /> 105-107; 109; 111; 114-116; <br /> 118-119; 122-126; 128; 130-132; <br /> 137-140; 142-143; 147-159; <br /> 161-166; 168; 170-174; 176-181; <br /> 183-185; 187; 190; 192-193; <br /> 196-205; 207-230; 232-239;<br /> 241-246; 248-250;   																							 | fi_topics.xml 	|
French	   	| AH Mono FR 		| 251-331; 333-350											| fr_topics.xml 	|
Hungarian  	| AH Mono HU 		| 251-325; 351-369; 371-375; <br /> 401-450					| hu_topics.xml 	|
Italian	   	| AH Mono IT 		| 41-42; 44-49; 60-63;  65-69; <br /> 80-99;  110-119; 130-145; <br /> 147-149; 161-168; 171; 173-174; <br /> 176-179; 190; 192-200 									| it_topics.xml 	|
Dutch	   	| AH Mono NL 		| 41-159; 161-165; 167-190; <br /> 192-193; 195-200															| nl_topics.xml 	|
Portuguese 	| AH Mono PT 		| 251-350													| pt_topics.xml 	|
Russian		| AH Mono RU		| 143; 147-149; 151; 153-155; 157; <br /> 163-164; 168-169; 172; 176-181; <br /> 183; 187; 192-193; 197-203; 207;  <br /> 209-216; 218; 220-221; 224-228;  <br /> 230-235; 237-239; 241-242;  <br /> 244-245; 250     | ru_topics.xml 	  |	
Swedish		| AH Mono SV 		| 91-109; 111-159; 161-166; <br /> 168-190; 192-193; 195-197; <br /> 199-200															| sv_topics.xml 	|

# Retrieval Effectiveness

For the TREC collection there were a total of 7 systems that provided such scripts: ATIRE, Galago, Indri, JASS, Lucene, MG4J, and Terrier. The scripts were free to index and search with varying parameters. As a result, a total of 13 different indexes were generated, and 17 sets of search results. For the CLEF collections there were 3 systems together with their required scripts: Indri, Lucene, Terrier; in the case of Terrier different retrieval models (BM25, Hiemstra LM, PL2, and TFIDF) were experimented in conjunction with different configurations for [stop lists](http://members.unine.ch/jacques.savoy/clef/index.html) and [stemmers](https://github.com/snowballstem). All the details about the experiments (MAP@1000 calculated by *trec_eval* are reported in the table below.


System  | Model 	   | Stop  | Stem  | bg      | de      | es      | fa      | fi      | fr      |
:-------|:-------------|:------|:------|:--------|:--------|:--------|:--------|:--------|:--------|
Terrier | BM25         |   	   |       | 0.2092  | 0.2733  | 0.3627  | 0.4033  | 0.3464	 | --	   |
Terrier | BM25		   | ✔ 	   |	   | 0.2081  | 0.2742  | 0.3656  | 0.4022  | 0.3392	 | --	   |
Terrier | BM25		   |	   | ✔	   | -- 	 | 0.3194  | 0.4347  | -- 	   | 0.4339	 | --	   |
Terrier | BM25		   | ✔	   | ✔     | --      | 0.3215  | 0.4356  | --      | 0.4278	 | --	   |
Terrier | Hiemstra LM  |       |	   | 0.1647	 | 0.2520  | 0.3016  | 0.3140  | 0.3125	 | --	   |
Terrier | Hiemstra LM  | ✔	   | 	   | 0.1640	 | 0.2561  | 0.3081  | 0.3193  | 0.3156	 | --      |
Terrier | Hiemstra LM  |       | ✔	   | -- 	 | 0.2753  | 0.3673  | -- 	   | 0.3639	 | --	   |
Terrier | Hiemstra LM  | ✔	   | ✔	   | -- 	 | 0.2801  | 0.3783  | -- 	   | 0.3636	 | --	   |
Terrier | PL2		   | 	   |	   | 0.2043	 | 0.2625  | 0.3486  | 0.4081  | 0.3316	 | --	   |
Terrier | PL2		   | ✔	   | 	   | 0.2009	 | 0.2658  | 0.3572  | 0.4061  | 0.3388	 | --      |
Terrier | PL2		   |	   | ✔	   | --      | 0.3080  | 0.4168  | -- 	   | 0.4222	 | --	   |
Terrier | PL2		   | ✔     | ✔     | --	     | 0.3102  | 0.4211  | -- 	   | 0.4152  | --	   |
Terrier | TFIDF		   | 	   |	   | 0.2071	 | 0.2709  | 0.3597  | 0.4050  | 0.3457  | --	   |
Terrier | TFIDF		   | ✔	   | 	   | 0.2083	 | 0.2723  | 0.3658  | 0.4053  | 0.3393	 | --	   |
Terrier | TFIDF		   |	   | ✔	   | -- 	 | 0.3185  | 0.4313  | -- 	   | 0.4354  | --	   |
Terrier | TFIDF		   | ✔	   | ✔	   | --		 | 0.3167  | 0.4355  | -- 	   | 0.4269	 | --	   |
Lucene	| BM25   	   | ✔     | ✔	   | --	     | 0.3126  | 0.4251	 | 0.4158  | -- 	 | 0.3865  |
Indri	| LM Dirichlet | ✔	   | ✔	   | 0.2051  | 0.1365  | 0.3334	 | 0.3735  | --		 | 0.1444  |
	


