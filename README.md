# Career Outcomes for Post-Doctoral Students
## Background

According to the [National Postdoctoral Association](https://www.nationalpostdoc.org/page/What_is_a_postdoc), a "postdoc" is is an "individual holding a doctoral degree who is engaged in a temporary period of mentored research and/or scholarly training for the purpose of acquiring the professional skills needed to pursue a career path of his or her choosing." In other words, they are engaging in research and/or training at a university in order to decide what they want to pursue as a career. Thus, it would be helpful to see what career paths postdocs from different departments at Johns Hopkins University pursue. This could help the career center effectively accomodate current postdoctoral students at Hopkins. This is important as postdocs are students who are, in essence, at a university while they decide where to continue on with their career.

Looking into some of the areas that postdocs pursue, such as academia, for-profit, goverment, non-profit, teaching positions or non- science related fields could prove useful for career centers to provide adequate support.

A look into Johns Hopkins data from [Next Generation Life Science Coalition](http://nglscoalition.org/coalition-data/#close) will elucidate the different career paths that Hopkins postdocs from different departments pursue.

## Business Question

___How can Johns Hopkins University's career center provide different career opportunities and resources for post-doctoral students in different departments?___


## Open Data 

__[Next Generation Life Science Coalition](https://provost.jhu.edu/education/graduate-and-professional-education/cngls/):__ this library contains the different career outcomes for postdocs and doctorul students at Hopkins. [Career outcomes for postdocs](https://provost.jhu.edu/education/graduate-and-professional-education/cngls/postdoctoral-career-outcomes-tabular-format/) was used.

- [Postdoc Career Outcomes Data Part 1](https://github.com/skang06/Post-Doctoral_Career_Outcomes/blob/main/tabula-Postdoc-CareerOutcome-ADATables-083019-2.csv): Dataset containing original data source where the "teaching" and "non-science related" data was gleaned from.

- [Postdoc Career Outcomes Data Part 2](https://github.com/skang06/Post-Doctoral_Career_Outcomes/blob/main/tabula-Postdoc-CareerOutcome-ADATables-083019.csv): Dataset containing original data source where the "Academia," "for-profit," "goverment," "non-profit" was gleaned from.

## Data Analysis 

___How does the data group itself into separate clusters?___

K-means clustering analysis was used in Excel. The cluster analysis was initally conducted with 3 anchors. As the aim is to find the anchors that minimize the sum of the minimum squared distances between the anchors and the individual data points, a cluster analysis with 4 nodes was also conducted. The cluster analysis with 4 nodes had a lower sum of the minimum squared distances. The 5-anchor cluster analysis also had a lower sum. Nonetheless, there was only 1 department in the 5th anchor, which indicated that 5 anchors was unnecessary. Thus, the 4-anchor cluster model was the best.

A step-by-step Excel data analysis can be found [here](https://github.com/skang06/Post-Doctoral_Career_Outcomes/blob/main/Excel%20Step%20by%20Step_3.docx).

__Clusters and Their Characteristics__
![alt text](https://github.com/skang06/Post-Doctoral_Career_Outcomes/blob/main/chart1.png)
![alt text](https://github.com/skang06/Post-Doctoral_Career_Outcomes/blob/main/factors.png)

_Cluster 1_: Above average going into non-profit. Slightly above average going into for- profit. 
Significantly below average percent of postdocs going into academia/teaching/non science related fields. Below average going into government. 
- It is the only cluster that has an above average percent of postdocs going into for- profit and the only cluster with an above average percent going into non-profit institutions. Although they are both less than one standard deviation above the average. On the other hand, it has the lowest average percent of postdocs going into academia, government, and teaching among the clusters. For academia and teaching, it is more than one standard deviation below average going into those paths, which demonstrates their unpopularity with postdocs.

_Cluster 2_: Above average going into teaching. Very slightly above average going into government. 
Significantly below average percent of postdocs going into academia/for- profit/ non science related fields. Below average going into non-profit
- It is the cluster with the most above average percent of postdocs going into teaching. Although it is less than one standard deviation above the average. Interestingly, it is significantly below average percent of postdocs going into academia; it is almost one standard deviation lower. So, perhaps those going into teaching are not pursuing teaching positions in academia, unlike what one would normally expect.

_Cluster 3_: Significantly above average going into academia. Above average going into government. 
Below average going into for- profit/ non-profit. Slighty below average going into teaching.  Significantly below average going into non science related fields.
- It is the cluster with the most above average percent of postdocs going into academia, at nearly one standard deviation above the mean. The percent of postdocs going into government is also above average at .65 standard deviations above. 

_Significantly below average going into non science related fields at almost one standard deviation lower for cluster 1 - 3._

_Cluster 4_: Significantly above average going into government. Slightly above average going into academia/teaching. 
Significantly below average going into for- profit/non science related fields. Below average going into non-profit.
- This cluster has the most above average percent of postdocs going into government. It is nearly 2 standard deviations above the average. There is also an above average percent of postdocs going into academia, although it is not nearly as many as cluster 3.
- Significantly below average going into for- profit. It is tied with Cluster 4 for most below average percent of post docs going into for-profit institutions. Among the four clusters, this cluster has the smallest below average percent of postdocs go into non- science related fields.

A list of the departments and the cluster they fall in can be found in the chart below.
__List of Departments and Their Relevant Cluster__
![alt text](https://github.com/skang06/Post-Doctoral_Career_Outcomes/blob/main/list.png)


## Summary and Implementation
This analysis can help career centers figure out which resources and opportunities to provide postdoc students in different departments based on which career paths are more prevalent. It can also help employers figure out which departments to target and concentrate their efforts on for the greatest effectiveness (ie. they would be reaching out to students that are more likely to pursue those paths). This is important since there are many departments at Hopkins that house postdocs, thus figuring out an oorganized method of attack would prove fruitful. The career center could implement four different subgroups to accomodate the four different groups of departments that tend towards similar career paths. 

__Cluster 1__: For-profit and non-profit institutions were the most popular career outcomes. The career center could reach out and organize more for-profit and non-profit institutions to come to career fairs or other events for these departments. On the other hand, the for-profit and non-profit employers could send more information or reach out to these departments and hold more events and panels to educate the students.
__Cluster 2__: Teaching was the most popular path. The career center could organize more workshops developing skills such as public speaking and effective ways to teach for the postdocs, as these are skills not learned as much during studies.
__Cluster 3__: Academia and government were the most popular. The career center could make sure they send out information about universities and colleges, and reach out to them as well. Some information about governmental institutions that are hiring would also benefit these departments.
__Cluster 4__: Government was the most popular choice for those in departments in this cluster. It also had some people go into academia and teaching. The career center should make sure they reach out to governmental institutions for potential job openings.

Additional data on what specific kinds of companies within non-profits or for-profits the postdocs pursue would provide more detailed analysis. There are a lot of different kinds of nonprofits and for-profit institutions, so having a more detailed division of the percentage that go into each help career centers and employers alike. Furthermore, overall data on the specific companies that postdocs go to could help the career center find similar companies that are popular with the students

