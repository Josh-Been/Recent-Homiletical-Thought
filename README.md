# Recent-Homiletical-Thought
An annotated dataabse of journal articles, books, and theses/dissertations around the field of homiletics. The annotations range from a sentence to a paragraph. The initial dataset contains 2,370 citations. Anticipated additions are 2,000 new records per year for the next five years.

[Themed Readme](https://josh-been.github.io/Recent-Homiletical-Thought/)

Live Power BI Database: [https://sites.baylor.edu/rht/](https://sites.baylor.edu/rht/)

Video Overview: [https://mediaspace.baylor.edu/media/Recent+Homiletical+Thought/0_zsamobf2](https://mediaspace.baylor.edu/media/Recent+Homiletical+Thought/0_zsamobf2)

Files:
* [Data Management Plan](https://josh-been.github.io/Recent-Homiletical-Thought/DMP-Recent_Homiletical_Thought_Project.docx)
* [Power BI Project File](https://josh-been.github.io/Recent-Homiletical-Thought/rht.pbix)
* [Cited Articles](https://josh-been.github.io/Recent-Homiletical-Thought/RHT-Articles.xlsx)
* [Cited Books](https://josh-been.github.io/Recent-Homiletical-Thought/RHT-Books.xlsx)
* [Cited Theses and Dissertations](https://josh-been.github.io/Recent-Homiletical-Thought/RHT-Theses-and-Dissertations.xlsx)

3rd Party Tools Used:
* [Microsoft Power BI](https://powerbi.microsoft.com/)

Custom Tools Used:
* [RHT_Processing.ipynb Jupyter Notebook](https://github.com/Josh-Been/Recent-Homiletical-Thought/blob/master/RHT_Processing.ipynb)
  * Prepares the raw data for use within Power BI
* [rht_citations.html](https://josh-been.github.io/Recent-Homiletical-Thought/rht_citations.html)
  * Assists accessing citation information

Workflow:
1. Truett Seminary researchers collect and approve new records in three separate Excel sheets. One each for books, articles, and theses/dissertations.
2. Once approved, these Excel sheets are processed using the [RHT_Processing.ipynb Jupyter Notebook](https://github.com/Josh-Been/Recent-Homiletical-Thought/blob/master/RHT_Processing.ipynb). This creates a composite Excel file, including standardized column headers, Google Scholar and Worldcat URLs, binned date categories, composite fields for all-field searching, and citation style formatting.
3. This composite Excel sheet is used by Power BI to provide online searchable access. A searchable version will be available via https://sites.baylor.edu/rht/ using Microsoft Power BI. Baylor ITS undergoes rigorous security reviewes for web applications and platforms. As Power BI previously passed such a security review, and as there are no further fees incurred, we decided to use this 3rd party software to build the searchable database.
4. [Citations via Web Page Hosted by GitHub](https://github.com/Josh-Been/Recent-Homiletical-Thought/blob/master/rht_citations.html). As it proved difficult to create a formatted list of citation styles that was both convenient and easy to copy/paste for the end-user, we created this standalone JavaScript html file. Record data is passed from Power BI to this JavaScript html file via the url string, which is then parsed and displayed. Each record contains three citation styles: Chicago, MLA, APA. All three styles are passed to the JavaScript html file delimited by the pipe character |. The first word of each citation is the style name.
