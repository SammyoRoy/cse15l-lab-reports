# Lab Report 3

**Exploring the ```grep``` command**

(Note: The codeblock formatting disappears when I use the print --> save to pdf option on Chrome)
1) ```grep -v```

[Source](https://en.wikibooks.org/wiki/Grep)

The `grep -v` command filters a list by excluding the search term. This could be useful if you're
trying to exclude a certain type of file, works by a certain author, topic, etc.

In this example, I'm filtering out all the files that have History in the title. This could be useful if I'm not interested in reading any history articles when planning my trip. 

```
$ cd written_2/travel_guides/berlitz2
$ ls | grep -v History
Algarve-Intro.txt
Algarve-WhatToDo.txt
Algarve-WhereToGo.txt
Amsterdam-I
Amsterdam-WhatToDo.txt
Amsterdam-WhereToGo.txt
Athens-Intro.txt
Athens-WhatToDo.txt
Athens-WhereToGo.txt
Bahamas-Intro.txt
Bahamas-WhatToDo.txt
Bahamas-WhereToGo.txt
Bali-WhatToDo.txt
Bali-WhereToGo.txt
Barcelona-WhatToDo.txt
Barcelona-WhereToGo.txt
Beijing-WhatToDo.txt
Beijing-WhereToGo.txt
Berlin-WhatToDo.txt
Berlin-WhereToGo.txt
Bermuda-history.txt
Bermuda-WhatToDo.txt
Bermuda-WhereToGo.txt
Boston-WhereToGo.txt
Budapest-WhatToDo.txt
Budapest-WhereoGo.txt
California-WhatToDo.txt
California-WhereToGo.txt
Canada-WhereToGo.txt
CanaryIslands-WhatToDo.txt
CanaryIslands-WhereToGo.txt
Cancun-WhatToDo.txt
Cancun-WhereToGo.txt
China-WhatToDo.txt
China-WhereToGo.txt
CostaBlanca-WhatToDo.txt
Costa-WhatToDo.txt
Costa-WhereToGo.txt
Crete-WhatToDo.txt
Crete-WhereToGo.txt
CstaBlanca-WhereToGo.txt
Cuba-WhatToDo.txt
Cuba-WhereToGo.txt
Nepal-WhatToDo.txt
Nepal-WhereToGo.txt
Paris-WhatToDo.txt
Paris-WhereToGo.txt
Poland-WhatToDo.txt
Portugal-WhatToDo.txt
Portugal-WhereToGo.txt
PuertoRico-WhatToDo.txt
PuertoRico-WhereToGo.txt
Vallarta-WhatToDo.txt
Vallarta-WhereToGo.txt
```

In this example, I'm filtering out all the files that contain Intro in the title. This could be useful if I'm already familiar with the locations and thus am not interested in reading the intro articles.
```
$ cd ../berlitz1
$ ls | grep -v Intro
HandRHawaii.txt
HandRHongKong.txt
HandRIbiza.txt
HandRIsrael.txt
HandRIstanbul.txt
HandRJamaica.txt
HandRJerusalem.txt
HandRLakeDistrict.txt
HandRLasVegas.txt
HandRLisbon.txt
HandRLosAngeles.txt
HandRMadeira.txt
HandRMadrid.txt
HandRMallorca.txt
HistoryDublin.txt
HistoryEdinburgh.txt
HistoryEgypt.txt
HistoryFrance.txt
HistoryFWI.txt
HistoryGreek.txt
HistoryHawaii.txt
HistoryHongKong.txt
HistoryIbiza.txt
HistoryIndia.txt
HistoryIsrael.txt
HistoryIstanbul.txt
HistoryItaly.txt
HistoryJamaica.txt
HistoryJapan.txt
HistoryJerusalem.txt
HistoryLakeDistrict.txt
HistoryLasVegas.txt
HistoryMadeira.txt
HistoryMadrid.txt
HistoryMalaysia.txt
HistoryMallorca.txt
JungleMalaysia.txt
WhatToDublin.txt
WhatToEdinburgh.txt
WhatToEgypt.txt
WhatToFrance.txt
WhatToFWI.txt
WhatToGreek.txt
WhatToHawaii.txt
WhatToHongKong.txt
WhatToIbiza.txt
WhatToIndia.txt
WhatToIsrael.txt
WhatToIstanbul.txt
WhatToItaly.txt
WhatToJamaica.txt
WhatToJapan.txt
WhatToLakeDistrict.txt
WhatToLasVegas.txt
WhatToLosAngeles.txt
WhatToMadeira.txt
WhatToMalaysia.txt
WhatToMallorca.txt
WhereToDublin.txt
WhereToEdinburgh.txt
WhereToEgypt.txt
WhereToFrance.txt
WhereToFWI.txt
WhereToGreek.txt
WhereToHawaii.txt
WhereToHongKong.txt
WhereToIbiza.txt
WhereToIndia.txt
WhereToIsrael.txt
WhereToIstanbul.txt
WhereToItaly.txt
WhereToJapan.txt
WhereToJerusalem.txt
WhereToLakeDistrict.txt
WhereToLosAngeles.txt
WhereToMadeira.txt
WhereToMadrid.txt
WhereToMalaysia.txt
WhereToMallorca.txt
```

2) `grep -r`

[Source](https://man7.org/linux/man-pages/man1/grep.1.html)
The `grep -r` command recursively searches through *all* the files in a directory. This is really useful if you want to look through every subdirectory at once.

In this example, I'm searching through all the files for the word "Lucayans". This could be useful if I want to find more information specifically on the Lucayans.
```
$ grep -r "Lucayans"
written_2/travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
written_2/travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
In this example, I'm searching through all the files for the word "Vista". This could be useful if I'm interested in scenic viewpoints.
```
$ grep -r "Vista"
written_2/non-fiction/OUP/Castro/chB.txt:Buena Vista, Mateo, La Seis, Chiquis, El Sur and all
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:        Greystone Mansion (905 Loma Vista Dr.), the spectacular neo-Gothic
written_2/travel_guides/berlitz1/WhereToMadeira.txt:        by car is Quinta da Boa Vista (Rua Luis Figueiroa de Albuquerque). The
written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt:Just 3 km (2 miles) down river from Portimão is Praia da Rocha, which became a holiday village for wealthy Portuguese families back at the end of the 19th century. It was “discovered” by the British in the 1930s, when this “beach of rocks,” strewn with extravagantly shaped eroded stacks, provided an inspirational refuge for writers and intellectuals. The belle époque Hotel Bela Vista is a living monument from those days.
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt:If you want a view of the whole city and the North Saskatchewan River on your way home, stop off at Vista 33, the observation level of the telephone building.
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:High in the hills behind Ponce is Hacienda Buena Vista. To get there, take Route 10, a major north-south artery. The road climbs steeply into dense vegetation and cooler air before you see signs for the hacienda; the climate and environmental conditions here were ideal for the coffee that the plantation began to grow more than 150 years ago. The plantation fell into neglect in the 20th century, but since 1984 it has been returned to its original state by The Conservation Trust of Puerto Rico. Agricultural machinery such as coffee bean huskers can be seen in the original buildings, and the water mill and canals, which harnessed the power of the Canas River, are now in working order. The facility shows how plantations used to operate and offer a fascinating insight into agricultural life in Puerto Rico all those years ago. Advance reservations are required for the tours (see page 64).
```

3) `grep -c`
[Source](https://man7.org/linux/man-pages/man1/grep.1.html)
Prints a count of matching lines for each input file. Could be useful for finding frequencies of words and other clustering techniques.

In this example, the output shows how many times "Egypt" is mentioned in the HistoryEgypt.txt file. This could be useful if I want to see what words are mentioned the most in the file.
```
$ grep -c Egypt HistoryEgypt.txt
55
```
In this example, the output shows how many times "Mediterranean" is mentioned in the HistoryGreek.txt file. This could be useful if I want to see what words are mentioned the most in the file.
```
$ grep -c Mediterranean HistoryGreek.txt
5
```

4) `grep -n`
[Source](https://man7.org/linux/man-pages/man1/grep.1.html)

The `grep -n` command prints the line number of where the match is located. This could be useful if you want to see how the term is distributed along a file, eg more frequent in the top, middle, or bottom.

In this example, the command output shows where "Clovis" is located in HistoryFrance.txt. This could be useful because it shows Clovis is mentioned near the middle of the file which immediately gives some context to France's historical timeline.
```
$ ls | grep -n Clovis HistoryFrance.txt
49:        Clovis, the leader of the Franks, defeated the Roman armies at
```

In this example, the command output shows where "Ireland" is located HistoryDublin.txt. It seems to be distributed pretty consistently throughout the entirety of the article. 
```
$ ls | grep -n Ireland HistoryDublin.txt
7:        Celtic Ireland
8:        Ireland has been inhabited since very ancient times, but
10:        6th century b.c. , Ireland’s first documented invasion. They brought
16:        system, and Celtic Ireland became a series of independent kingdoms.
26:        St. Patrick first came to Ireland as a prisoner, captured in
28:        and returned to Ireland as a missionary in a.d. 432. By the time of
35:        and the plant has been a symbol of Ireland ever since.
37:        successfully fused, Ireland entered its “Golden Age” (a.d. 500 until
40:        Ireland became “the light of the known world,” sending its saints and
48:        Throughout this period, Ireland’s political organization
53:        Ireland was subject to repeated Viking raids. The Vikings sacked the
55:        they built a fort on the Liffey and founded Ireland’s first town — Dubh
64:        Ireland Under the Normans
66:        struggle between England and Ireland that was to dominate Irish history
69:        “Strongbow,” to come to Ireland to help him reclaim his kingdom
77:        center of English administrative power in Ireland. The city elected its
88:        I were determined to subdue Ireland, and sent in massive military
101:        In 1649, Ireland’s most hated conqueror, Oliver Cromwell,
118:        anxious to achieve at least a measure of self-government for Ireland.
135:        life in Ireland. Great public buildings like the Customs House and the
141:        1801, when the Act of Union brought Ireland under direct rule from
173:        Ireland. For a time, it looked as if the campaign was going to succeed,
205:        partial victory for Ireland, and in 1921 the Partition Act enabled the
206:        six counties of Northern Ireland to remain in the union with Britain,
213:        In 1937 De Valera’s republican constitution took Ireland
219:        toll, and at first independent Ireland was characterized by a parochial
222:        erected in their place that are not admired today. However, Ireland has
230:        woman as mayor, and in 1990 Ireland chose the dynamic Mary Robinson as
```
