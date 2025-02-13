# founding-fathers-corpus-dataset
 A corpus of correspondences & other writings of US Founding Fathers, credit to Founders Online.

Founding Fathers Corpus Dataset
----------------------
**A ~180k documents, 66 million-word corpus**.

[Founders Online](https://founders.archives.gov/) is a [National
Archives](https://www.archives.gov/) resource that makes available
\~180K writings/letters of the Founders of the United States of America.

Originally extracted by GitHub user [jaytimm](https://github.com/jaytimm) using the Founders Online [API](https://founders.archives.gov/API/docdata/) and made available at his [founders-online-corpus](https://github.com/jaytimm/founders-online-corpus/tree/master) repository as R Data Serialization (RDS) format.

My contribution was converting the compressed RDS files into their respective CSV files.

These CSV files range in (uncompressed) sizes from 52 MB to 203 MB, totaling 795 MB (155 MB compressed).

Since these were mostly text and compress very well, it was silly to leave them uncompressed, so they appear here as compressed files. I went with .ZIP format instead of 7Zip format to make them as accessable as possible.





### Files, Names, Counts

| file name                   | years    | doc count | word count  |
|:----------------------------|:-------- |:----------|:------------|
| Adams_Presidency.csv        | 1706-1775| 16,111    | 5,569,488   | 
| Colonial.csv                | 1775-1783| 48,502    | 16,255,296  | 
| Confederation_Period.csv    | 1783-1789| 17,024    | 7,184,958   | 
| Jefferson_Presidency.csv    | 1789-1797| 27,531    | 10,435,172  | 
| Madison_Presidency.csv      | 1797-1801| 13,743    | 4,351,329   | 
| post-Madison_Presidency.csv | 1801-1809| 28,854    | 10,883,697  | 
| Revolutionary_War.csv       | 1809-1817| 15,094    | 6,468,738   | 
| Washington_Presidency.csv   | 1817+    | 14,618    | 5,026,013   |
|                             |          |           |             |  
| Total                       |          | 181,477   | 66,174,691  |

Note: The word counts are very rough, and a
single document may be double counted. (See Founders Online for an
explanation).



### Data Sample

```
"title","permalink","project","authors","recipients","date_from","date_to","api","og_text","text","period"
"To James Madison from George Graham, 15 September 1817","https://founders.archives.gov/documents/Madison/04-01-02-0115","Madison Papers","Graham, George","Madison, James",1817-09-15,1817-09-15,"https://founders.archives.gov/API/docdata/Madison/04-01-02-0115","
Dear SirDept. of War Sepr. 15th. 1817
Yours of the 10th Inst. covering a Letter to you from Mr. French was duly received. On examining the files of this Dept. it appears that his recommendations for a Commission in the Army were placed on file, but burnt with all the other papers of that description when the enemy were at this place. I return you Mr. French’s letter, And am with great respect & esteem—yours &c
Geo Graham
","Dear SirDept. of War Sepr. 15th. 1817 Yours of the 10th Inst. covering a Letter to you from Mr. French was duly received. On examining the files of this Dept. it appears that his recommendations for a Commission in the Army were placed on file, but burnt with all the other papers of that description when the enemy were at this place. I return you Mr. French’s letter, And am with great respect & esteem—yours &c Geo Graham","post-Madison Presidency"
```

### Descriptions of the Columms

The `title`:`date_to` columns have been extracted directly from [document
metadata](https://founders.archives.gov/Metadata/) made available by
Founders Online as XML. The `api` column was derived from the
`permalink` and `project` columns, and used to access/scrape document
text. The `og_text` column contains document text as presented on
Founders Online, which includes quite a bit of line breaks and odd
spacing. The `text` column is a stripped version of `og_test`, with
whitespace and line breaks removed. These data are not perfect.
The `period` column categorizes each document in corpus historically.
Categories/dates are based on Founders Online.



### Caveats

With the exception of the `text` column, the data presented here have
been extracted without modification from the Founders Online website.
Any data weirdness (of which there is some) lives in the original data
source. This is only to say that the user can make their own decisions
on how to address some of these issues as all original data exist in the
files made available here. 




### Acknowlegments

Thanks to the Founding Fathers, for their actions and words, without which, the creation of this dataset would not be possible.

Thanks to the folks at [Founders Online](https://founders.archives.gov/about), who did the hard work of digitizing and aggregating the data.

Thanks to the GitHub user [jaytimm](https://github.com/jaytimm), who gathered the data from Founders Online and made it available at their [founders-online-corpus](https://github.com/jaytimm/founders-online-corpus/tree/master) repository.

