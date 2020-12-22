![visitors](https://visitor-badge.glitch.me/badge?page_id=Soham-coder-search_engine)

# Title

##### Text Search Engine (a prototype)

```diff
@@ Aim—@@

The aim of this project is to build a prototype of a search engine which will work on millions of wikipedia pages (which are in xml format) and retrieve the top 10 relevant Wikipedia documents that matches the input query of user. This takes Wikipedia corpus in XML format which is available at Wikipedia.org as input. Then it indices millions of Wikipedia pages involving a comparable number of distinct terms. Given a query, it retrieves relevant ranked documents and their titles using index. This project uses OOPs concepts.
```
###### Future Possible Goals

    - Information about index files and the final treemap data structure is ready. 
    - We can rank the documents based on this parameter when user types a query i.e., the backend part is implemented.
    - Next, one can go for implementing the GUI for this search engine i.e., the frontend part.



##### Directory structure

<details><summary><tt> Directory structure </tt></summary>
<p>

- .
   - [README.md](README.md)
   - __SearchEngine__
     - [SpamServerMinimal.iml](SearchEngine/SpamServerMinimal.iml)
     - [pom.xml](SearchEngine/pom.xml)
     - __src__
       - __main__
         - __input__
           - [2000pages.dat](SearchEngine/src/main/input/2000pages.dat)
           - [newfile.dat](SearchEngine/src/main/input/newfile.dat)
           - [sample.xml](SearchEngine/src/main/input/sample.xml)
         - __java__
           - __com__
             - __soham__
               - __searchengine__
                 - __config__
                   - [StopWordsConfig.java](SearchEngine/src/main/java/com/soham/searchengine/config/StopWordsConfig.java)
                   - [WikiPageParsingConstants.java](SearchEngine/src/main/java/com/soham/searchengine/config/WikiPageParsingConstants.java)
                   - [XMLPageConfig.java](SearchEngine/src/main/java/com/soham/searchengine/config/XMLPageConfig.java)
                 - __model__
                   - [KeyWord.java](SearchEngine/src/main/java/com/soham/searchengine/model/KeyWord.java)
                   - [MergeLine.java](SearchEngine/src/main/java/com/soham/searchengine/model/MergeLine.java)
                   - [WikiPage.java](SearchEngine/src/main/java/com/soham/searchengine/model/WikiPage.java)
                 - __search__
                   - [DocDetails.java](SearchEngine/src/main/java/com/soham/searchengine/search/DocDetails.java)
                   - [PostingList.java](SearchEngine/src/main/java/com/soham/searchengine/search/PostingList.java)
                   - [QueryWord.java](SearchEngine/src/main/java/com/soham/searchengine/search/QueryWord.java)
                   - [SearchMain.java](SearchEngine/src/main/java/com/soham/searchengine/search/SearchMain.java)
                 - __services__
                   - [ExternalSort.java](SearchEngine/src/main/java/com/soham/searchengine/services/ExternalSort.java)
                   - [Main.java](SearchEngine/src/main/java/com/soham/searchengine/services/Main.java)
                   - [PageParser.java](SearchEngine/src/main/java/com/soham/searchengine/services/PageParser.java)
                   - [Stemmer.java](SearchEngine/src/main/java/com/soham/searchengine/services/Stemmer.java)
                   - [WikiSAXHandler.java](SearchEngine/src/main/java/com/soham/searchengine/services/WikiSAXHandler.java)
                 - __util__
                   - [TimeUtil.java](SearchEngine/src/main/java/com/soham/searchengine/util/TimeUtil.java)
         - __output__
           - [0\_index.txt](SearchEngine/src/main/output/0_index.txt)
           - [0\_offsets.txt](SearchEngine/src/main/output/0_offsets.txt)
           - [0\_secondry.txt](SearchEngine/src/main/output/0_secondry.txt)
           - [10\_index.txt](SearchEngine/src/main/output/10_index.txt)
           - [10\_offsets.txt](SearchEngine/src/main/output/10_offsets.txt)
           - [10\_secondry.txt](SearchEngine/src/main/output/10_secondry.txt)
           - [11\_index.txt](SearchEngine/src/main/output/11_index.txt)
           - [11\_offsets.txt](SearchEngine/src/main/output/11_offsets.txt)
           - [11\_secondry.txt](SearchEngine/src/main/output/11_secondry.txt)
           - [12\_index.txt](SearchEngine/src/main/output/12_index.txt)
           - [12\_offsets.txt](SearchEngine/src/main/output/12_offsets.txt)
           - [12\_secondry.txt](SearchEngine/src/main/output/12_secondry.txt)
           - [13\_index.txt](SearchEngine/src/main/output/13_index.txt)
           - [13\_offsets.txt](SearchEngine/src/main/output/13_offsets.txt)
           - [13\_secondry.txt](SearchEngine/src/main/output/13_secondry.txt)
           - [14\_index.txt](SearchEngine/src/main/output/14_index.txt)
           - [14\_offsets.txt](SearchEngine/src/main/output/14_offsets.txt)
           - [14\_secondry.txt](SearchEngine/src/main/output/14_secondry.txt)
           - [15\_index.txt](SearchEngine/src/main/output/15_index.txt)
           - [15\_offsets.txt](SearchEngine/src/main/output/15_offsets.txt)
           - [15\_secondry.txt](SearchEngine/src/main/output/15_secondry.txt)
           - [16\_index.txt](SearchEngine/src/main/output/16_index.txt)
           - [16\_offsets.txt](SearchEngine/src/main/output/16_offsets.txt)
           - [16\_secondry.txt](SearchEngine/src/main/output/16_secondry.txt)
           - [17\_index.txt](SearchEngine/src/main/output/17_index.txt)
           - [17\_offsets.txt](SearchEngine/src/main/output/17_offsets.txt)
           - [17\_secondry.txt](SearchEngine/src/main/output/17_secondry.txt)
           - [18\_index.txt](SearchEngine/src/main/output/18_index.txt)
           - [18\_offsets.txt](SearchEngine/src/main/output/18_offsets.txt)
           - [18\_secondry.txt](SearchEngine/src/main/output/18_secondry.txt)
           - [19\_index.txt](SearchEngine/src/main/output/19_index.txt)
           - [19\_offsets.txt](SearchEngine/src/main/output/19_offsets.txt)
           - [19\_secondry.txt](SearchEngine/src/main/output/19_secondry.txt)
           - [1\_index.txt](SearchEngine/src/main/output/1_index.txt)
           - [1\_offsets.txt](SearchEngine/src/main/output/1_offsets.txt)
           - [1\_secondry.txt](SearchEngine/src/main/output/1_secondry.txt)
           - [20\_index.txt](SearchEngine/src/main/output/20_index.txt)
           - [20\_offsets.txt](SearchEngine/src/main/output/20_offsets.txt)
           - [20\_secondry.txt](SearchEngine/src/main/output/20_secondry.txt)
           - [21\_index.txt](SearchEngine/src/main/output/21_index.txt)
           - [21\_offsets.txt](SearchEngine/src/main/output/21_offsets.txt)
           - [21\_secondry.txt](SearchEngine/src/main/output/21_secondry.txt)
           - [22\_index.txt](SearchEngine/src/main/output/22_index.txt)
           - [22\_offsets.txt](SearchEngine/src/main/output/22_offsets.txt)
           - [22\_secondry.txt](SearchEngine/src/main/output/22_secondry.txt)
           - [23\_index.txt](SearchEngine/src/main/output/23_index.txt)
           - [23\_offsets.txt](SearchEngine/src/main/output/23_offsets.txt)
           - [23\_secondry.txt](SearchEngine/src/main/output/23_secondry.txt)
           - [24\_index.txt](SearchEngine/src/main/output/24_index.txt)
           - [24\_offsets.txt](SearchEngine/src/main/output/24_offsets.txt)
           - [24\_secondry.txt](SearchEngine/src/main/output/24_secondry.txt)
           - [25\_index.txt](SearchEngine/src/main/output/25_index.txt)
           - [25\_offsets.txt](SearchEngine/src/main/output/25_offsets.txt)
           - [25\_secondry.txt](SearchEngine/src/main/output/25_secondry.txt)
           - [26\_index.txt](SearchEngine/src/main/output/26_index.txt)
           - [26\_offsets.txt](SearchEngine/src/main/output/26_offsets.txt)
           - [26\_secondry.txt](SearchEngine/src/main/output/26_secondry.txt)
           - [2\_index.txt](SearchEngine/src/main/output/2_index.txt)
           - [2\_offsets.txt](SearchEngine/src/main/output/2_offsets.txt)
           - [2\_secondry.txt](SearchEngine/src/main/output/2_secondry.txt)
           - [3\_index.txt](SearchEngine/src/main/output/3_index.txt)
           - [3\_offsets.txt](SearchEngine/src/main/output/3_offsets.txt)
           - [3\_secondry.txt](SearchEngine/src/main/output/3_secondry.txt)
           - [4\_index.txt](SearchEngine/src/main/output/4_index.txt)
           - [4\_offsets.txt](SearchEngine/src/main/output/4_offsets.txt)
           - [4\_secondry.txt](SearchEngine/src/main/output/4_secondry.txt)
           - [5\_index.txt](SearchEngine/src/main/output/5_index.txt)
           - [5\_offsets.txt](SearchEngine/src/main/output/5_offsets.txt)
           - [5\_secondry.txt](SearchEngine/src/main/output/5_secondry.txt)
           - [6\_index.txt](SearchEngine/src/main/output/6_index.txt)
           - [6\_offsets.txt](SearchEngine/src/main/output/6_offsets.txt)
           - [6\_secondry.txt](SearchEngine/src/main/output/6_secondry.txt)
           - [7\_index.txt](SearchEngine/src/main/output/7_index.txt)
           - [7\_offsets.txt](SearchEngine/src/main/output/7_offsets.txt)
           - [7\_secondry.txt](SearchEngine/src/main/output/7_secondry.txt)
           - [8\_index.txt](SearchEngine/src/main/output/8_index.txt)
           - [8\_offsets.txt](SearchEngine/src/main/output/8_offsets.txt)
           - [8\_secondry.txt](SearchEngine/src/main/output/8_secondry.txt)
           - [9\_index.txt](SearchEngine/src/main/output/9_index.txt)
           - [9\_offsets.txt](SearchEngine/src/main/output/9_offsets.txt)
           - [9\_secondry.txt](SearchEngine/src/main/output/9_secondry.txt)
           - [allWords.txt](SearchEngine/src/main/output/allWords.txt)
         - __resources__
           - [stopwords.txt](SearchEngine/src/main/resources/stopwords.txt)
   - [SeminarPresentation6920.pptx](SeminarPresentation6920.pptx)


</p>
</details>


##### Seminar presentation
[Ppt](SeminarPresentation6920.pptx)