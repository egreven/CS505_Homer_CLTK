# CS505_Homer_CLTK

**Results:**


**Graph 1: Speakers and Graph 2: Without Outliers**

The embeddings seem to just show the speakers who have the most frequent speeches that they are outliers and then each layer or section of outliers towards the main left cluster, the number of speeches per speaker decreases. This seems to lead to the conclusion that the word embeddings are only predicting similarity based on the number of speeches made. Maybe this is because there is not enough data to differentiate between speakers when several speakers only make one speech, whereas speakers who have multiple speeches the word embedding is more effective in predicting the similarity between speakers. 

The purpose of graph 2 without the outliers, is to better see the cluster of speakers on the left. 

Most outliers to Least outlying (number of speeches they speak)
- Achilles spoke 87 speeches - most outlier
- Agamemnon (47), Hector(49)
- Zeus (39), Nestor(33)
- Diomedes(26), Priamus(25), Odysseus(27), Menelaos(22), Athena(20), Apollo(18)
- Aias (son of Telamon)(19), Poseidon(16), Patroclus(12), Iris(12), Idomeneus(12)



**Graph 3: Mortal, god, or animal**

The speeches made by mortals, gods, and animals seem to have no similarity between each other and are all distinct ways of speaking since their points are far apart on the graph of the PCA


**Graph 4: Books**

Books 23, 24 are fairly separated/removed from the main middle cluster of books and this seems to reflect the shift in the Iliad during the last two books where funeral games and processions are carried out and much more grief and sadness is mentioned and referenced in these books. Hector is disgraced in his death, and only towards the end of the Iliad does Achilles give Hector’s body back for a proper Hero’s burial. An additional book close to the outliers of Book 23, 24 is Book 10. This is important because Book 10 talks about an Achaean victory and although it is not as big as winning the war, it is a significant win because the Achaeans Odysseus and Diomedes successfully gather information about the Trojans and are able to take some horses and escape with their lives. 

Victory or at least success happens for Hector in Book 12 when he successfully broken the Achaean wall and is able to enter. This book seems to be characterized by success of Hector and is on the opposite end (farthest as possible) of similarity from Books 23, 24 where Hector is dead and his memory is being disgraced. 

The embeddings done on the books seem to show that there is similarity amongst books where the Achaeans are winning and significant difference from these winning books and the books where the Achaeans are losing i.e. Book 12.


**Graph 5: Addressee and Graph 6: No outliers Addressee**
Similar to the case of Graph 1 and 2 of the speakers, Graphs 5 and 6 seem to rate similarity based on the number of times a character is addressed. Therefore, PCA analysis with this particular model for Word2Vec (and corpus of a variety of ancient Greek words) does not give valuable information on the similarity of how characters are referenced but rather just on the amount of times the character is addressed.

Most outlying to least outlying/closer to main left most cluster (number of times addressed)
- Greeks(59)
- Hector(44), Achilles(43)
- Agamemnon(37)
- Trojans(29)
- Hera(24), Priamus(21), Diomedes(22), Zeus(21)
- Athena(17)
- Patroclus(16), Nestor(16), Menelaos(14), Odysseus(16), Zeus (prayer)(16), himself(12), Thetis(12)

**Future Work**
Further analysis could be done to compare how Homer portrays the speech of characters with similar counts of speeches and being addressed then by accounting for the similarity in frequency the PCA analysis should accurately show if the character (like Odysseus) speaks and is spoken to similarly in both the Iliad and the Odyssey. Originally I thought it would be interesting to compare how certain characters (mostly gods) are spoken to in the Iliad and Odyssey compared with the Hymns Homer wrote to them. However, unless the number of times a god is addressed is similar to the number of hymns Homer has to that god, the PCA analysis might still be skewed based on frequency and not similarity of words in the speeches. Another idea was to make a corpus based solely on Homeric greek and use this to train a Word2Vec model on but there is concern that the number of lemmas in all of Homer’s works is not a sufficient number to create a corpus on and then train a model. But this could be interesting to do just to see if this suspicion is confirmed. Additionally, Homer characterizes each character by a phrase such as “Most cunning Odysseus” in the Odyssey or “wise Telemachus” in the Iliad, it would be interesting to graph and see if there is similarity in sentiment or connotation between the phrase and the following person’s speech. 


Resources:
- Talks about characterization in Homer: https://chs.harvard.edu/chapter/2-characterization-in-homer-and-agamemnons-appeal-in-iliad-4/
- Very helpful for reading Greek: https://geoffreysteadman.com/
- Character level BERThttps://github.com/brennannicholson/ancient-greek-char-bert
- Paper on extending character BERT to a more functional BERT: https://aclanthology.org/2021.latechclfl-1.15.pdf
- Export whole passages without lines as txt: https://scaife.perseus.org/reader/urn:cts:greekLit:tlg0012.tlg001.perseus-grc2:1/


Coding Sources:

Help with coding:
- https://www.geeksforgeeks.org/python-get-unique-values-list/
- https://stackoverflow.com/questions/2249036/grouping-python-tuple-list

Help with CLTK and using CLTK:
- https://github.com/cltk/enm_models_cltk
- https://github.com/cltk/cltk
- https://github.com/cltk/cltk/issues/1193#issue-1492399885


Content Sources:
- https://github.com/cltk/grc_text_perseus/tree/master/cltk_json --edited some files that were missing lines
- https://www.dsgep.ugent.be/iliad/  used for speech indices. Files "speech indices" came directly from this website

Summaries of Iliad used:
- https://www.litcharts.com/lit/the-iliad/book-10
- https://www.litcharts.com/lit/the-iliad/book-12
- https://www.litcharts.com/lit/the-iliad/book-23
- https://www.litcharts.com/lit/the-iliad/book-24
