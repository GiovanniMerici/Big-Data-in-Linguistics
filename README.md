# Big-Data-in-Linguistics
Supporting code for big-data analysis applied to linguistics.

Analysis of the apparition and evolution of french connective phrases, from ancien french (starting in the 9th century) to classical french (ending at the end of the 18th century) from the databases Base de Français Médiéval (BFM) http://bfm.ens-lyon.fr/ and Frantext https://www.frantext.fr. The BFM's corpus extends from the 10th century to the 15th century. Frantext contains more corpora but does not date as back as the BFM, and as a result the corpus used for this research extends from the 12th century to the 18th century. The precision will explain in the future possible gaps in results in between both bases. Also, the choice to use these two databases at once is self-explained by the apparent complementarity. The scope of the analysis is using basic tools offered by Pandas, Scipy and Matplotlib to analyse the vast quantity of data offered by the database. 
Pandas allows to handle dataframe in the simplest possible manner.
Matplotlib offers the possiblity of plotting graphs, fucnctional to the rapresentation of a vast range of data. 

Given the possibility of exporting data from the website directly in an excel file it's possible to import it into the script and quickly sort the data to obtain the desidered graphs. 

After few changes to the exported data it's possible for any users to exploit this simple script to visualise data in a ordered fashion.

This code was written by Giovanni Merici, gradstudend in biology and master student in "Scienze Biomolecolari, Genomiche e Cellulari" at the Università degli Studi di Parma (Parma, Italy). It serves as a support to the Mémoire of Axelle Domingues, gradstudent in modern letters and master student in "Sciences du langages : linguistique française et générale" at Sorbonne Université (Paris, France). This work conducts the diachronic study of the apparition of connective phrases in french, from latin to classical french, particularly focusing on the grammaticalization stage occuring in middle french (1300-1549). 

The data's organization allowed by Giovanni Merici's participation offers graphs that reveal without data loss the many tendancies in the evolution of several connecting phrases over centuries. 

The first part of the work is about the variation que/ce que in the evolution of two different connective phrases known in contemporary french as "pour que" and "parce que".
For that first phrase "pour que", formulas in CQL (Corpus Query Langages) were first developped in order to extract data from both databases that would include the many possible ortographic variations, very common in ancient and middle french. The BFM was given ([word="P[OU].*[^IYS]"%c & cattex-pos="PRE"] [word="[^IEA].*E"%c & cattex-pos="PROdem"]? [word="(QU|K).*[^T] ?"%c & cattex-pos="CONsub"])|([word="P[OU][^IV]*"%c & cattex-pos="CONsub"])and Frantext was given ([word="P[OU].*[^IY]"%cd & pos="P"] [word="[^IEA].*E"%cd & pos="PRO"]? [word="(QU|K).*"%cd & pos="CS"])|([word="P[OU][^IV]*"%cd & pos="CS"]).
For the second phrase "parce que, the same process applies. BFM was given ([word="PA.*[^IYS]"%c & cattex-pos="PRE"] [word="[^IEA].*E"%c & cattex-pos="PROdem"]? [word="(QU|K).*[^T] ?"%c & cattex-pos="CONsub"])|([word="PA[^IV]*"%c & cattex-pos="CONsub"])and Frantext was given ([word="PA.*[^IY]"%cd & pos="P"] [word="[^IEA].*E"%cd & pos="PRO"]? [word="(QU|K).*"%cd & pos="CS"])|([word="PA[^IV]*"%cd & pos="CS"]).
The search for "pour que" yielded 3489 results on the BFM and 8638 results on Frantext. The search for "parce que" yielded ? results in the BFM and 35742 results in Frantext.
