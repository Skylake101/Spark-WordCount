# Spark-WordCount

## About the author and the project
Hi, my name is Aawaj Joshi and I'm a graduate student at Northwest Missouri State University stuyding Applied Computer Science. This is project that I did for my Big Data class. In this project, I have utilized Spark to generate a word count for a raw text data. 

## Data used  
I am huge Potterhead which is why I have selected a few paragraphs from Chapter 31 of Harry Potter and the Goblet of Fire (my favorite book in the series). [Here is a link to my data](https://harrypotterbooksfree.com/harry-potter-4-chapter-31-the-third-task/). 

## Scala commands used
```
val inputFile = sc.textFile("C:/44517/Spark-WordCount/HP Third Task.txt")
val counts = inputFile.flatMap(line => line.split(" ")).map(word => (word,1)).reduceByKey(_ + _);
counts.saveAsTextFile("C:/tmp/show-spark/outputHP")
```

## Results
After running the aforementioned commands, I obtained two files with the words and their count. I aggregated the two files into one and imported it into Tableau, where I was able to filter by the top ten most frequent words. 

Here is a table showing the ten most frequent words and their count.

![wc table](https://user-images.githubusercontent.com/31771293/48317024-03c4c780-e5b1-11e8-9f68-a9ff9f10823b.PNG)


Here is a graphical representation of the result (also generated via Tableau).

![wc graph](https://user-images.githubusercontent.com/31771293/48317005-d11acf00-e5b0-11e8-954a-4f24a980fb9a.PNG)

## Author
Aawaj Raj Joshi   
