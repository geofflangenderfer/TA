# Question:

sarahk asks:

Hello Coding Help! While going through the weekly coding exercises, I have had some thoughts that I would like to get clarified.  
1) Where exactly is the data we are pulling for each week? Are the weekly exercises part of a huge folder that relies on the 'running' the previous examples to get the data? 
2) In all of the exercises, it would have been helpful to have an exercise in architecting how develop a solution. It seems like all the sample modules of code have been a) Load libraries b) define functions c)import data d)run functions e)plot functions 
3) Is there is Github repo that I can pull from? Thank you!

Please also note that for the Week 5 coding exercise, the link to the Andrew Ng k-mean video gives no video.

I also though of something else (I know I have a lot of questions :/)

I see how we are pulling 'data' from spreadsheets. I would like to learn how to pull 'data' from prose. i.e Reading scientific papers and generating conclusions. 




To achieve this, would it require some supervised learning, such as 'training' the system on certain sentences such "This conclusion supports" or "The results are" and then working from there with test data? I would like to know.


# Answer:
- Data Sources: We have various sources for the data.
    - train.csv originally comes from the NYC Taxi & Limousine Commission, which
    open sources this data.
    - the stack overflow links data comes from stack overflow
    - whenever we load a dataset from sklearn (i.e. load_boston()), we're pulling 
    small datasets that are part of that software package. They have various 
    original sources including the UCI Machine Learning Repository.

- Exercises: While there is somewhat of a routine involved in finding a
  solution-exploratory data analysis, feature engineering, model fitting,
  repeat-a lot of it is also experimentation. You get a hunch about the data
  after visualizing it, then test out your theory, and iterate. 
    - for further practice with this type of experimentation, check out the [titanic kaggle competition](https://www.kaggle.com/c/titanic/overview)
- Github: Unfortunately, there isn't a public copy of the assignments right now. 

- [Andrew Ng k-means](https://www.youtube.com/watch?v=hDmNF9JG3lo): Here's a link
  on youtube.

- Pulling data: Say you wanted to pull a specific term or data from a research
  paper. This can be done with [regular expressions](https://www.datacamp.com/community/tutorials/python-regular-expression-tutorial).
