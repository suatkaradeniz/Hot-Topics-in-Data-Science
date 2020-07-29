

# Hot Topics in Data Science

   In this project, we will be in search for an answer to the following question:
   "What is it that people want to learn about in data science?"
    
## Stack Exchange 
   Stack Exchange is a popular webpage which hosts sites on a multitude of fields 
   and subjects, including mathematics, physics, philosophy, and ***data science*** !
   The website employs a reputation award system for its questions and answers. 
   Each post — each question/answer — is a post that is subject to upvotes and 
   downvotes. This ensures that good posts are easily identifiable. 
    
   Stack Exchange provides a public data base for each of its websites. 
   Here's a [link](https://data.stackexchange.com/datascience/query/new) to query and 
   explore Data Science Stack Exchange's database.
   By writing a simple SQL query and saving it as a .csv file, data science community
   is able to derive valuable results from the obtained data. For our purpose, analyzing 
   all questions posted in 2019 seems promising. 
   
   We run the following query to extract the relevant data and then save it as a .csv file
   called **2019_questions.csv**:
   
   ```
SELECT Id, CreationDate,
       Score, ViewCount, Tags,
       AnswerCount, FavoriteCount
  FROM posts
 WHERE PostTypeId = 1 AND YEAR(CreationDate) = 2019;
```


#### Here's what the first few rows look like:

<table>
  <tr>
    <th>Id</th>
    <th>PostTypeId</th>
    <th>CreationDate</th>
    <th>Score</th>
    <th>ViewCount</th>
    <th>Tags</th>
    <th>AnswerCount</th>
    <th>FavoriteCount</th>
  </tr>
  <tr>
    <td>44419</td>
    <td>1</td>
    <td>2019-01-23 09:21:13</td>
    <td>1</td>
    <td>21</td>
    <td>&lt;machine-learning&gt;&lt;data-mining&gt;</td>
    <td>0</td>
    <td></td>
  </tr>
  <tr>
    <td>44420</td>
    <td>1</td>
    <td>2019-01-23 09:34:01</td>
    <td>0</td>
    <td>25</td>
    <td>&lt;machine-learning&gt;&lt;regression&gt;&lt;linear-regression&gt;&lt;regularization&gt;</td>
    <td>0</td>
    <td></td>
  </tr>
  <tr>
    <td>44423</td>
    <td>1</td>
    <td>2019-01-23 09:58:41</td>
    <td>2</td>
    <td>1651</td>
    <td>&lt;python&gt;&lt;time-series&gt;&lt;forecast&gt;&lt;forecasting&gt;</td>
    <td>0</td>
    <td></td>
  </tr>
</table>
