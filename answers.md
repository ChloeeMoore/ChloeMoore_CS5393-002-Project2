Answers:

How do you train the model and how do you classify a new tweet? Give a short description of the main steps.

Training: The model is trained by processing each tweet in the training dataset, breaking it into words, and 
storing these in a frequency table for positive and negative classifications. This involves parsing each tweet,
tokenizing it into individual words, and counting their occurrences in both sentiment categories. Optional 
enhancements, such as removing stop words or stemming, could improve performance by reducing noise. 

Classification: For each new tweet, the classifier tokenizes the tweet’s text and checks the frequency of each 
word in both sentiment categories. Based on this comparison, it assigns a sentiment by calculating the likelihood 
of the tweet being positive or negative using these word counts.

How long did your code take for training and what is the time complexity of your training implementation 
(Big-Oh notation)? Remember that training includes reading the tweets, breaking it into words, counting, ... 
Explain why you get this complexity (e.g., what does N stand for and how do your data structures/algorithms affect
the complexity).

The code took 0.353488 seconds long to train. The time complexity is O(N * M). The m and n stand for the average
number of words per tweet and the total number of tweets.

How long did your code take for classification and what is the time complexity of your classification implementation 
(Big-Oh notation)? Explain why.

The testing time is about 5.189 which prints to console. The complexity is O(N^2). The first loop is O(MN) because 
each line is tokenized. But there is another loop that goes through IDs N times and also iterates through each line 
also N times. The complexity for this is O(N^2) which overrules O(MN).

What accuracy did your algorithm achieve on the provides training and test data?

Accuracy: 67.2%

The TA will run your code on Linux and that accuracy value will be used to determine your grade.

What were the changes that you made that improved the accuracy the most?

A change that was made to improve accuracy was switching the stemming library midway through the project.

How do you know that you use proper memory management? I.e., how do you know that you do not have a memory leak?

Proper memory management was ensured by following the Rule of Three in the DSString class to correctly manage dynamic 
memory. I used memory profiling tools like valgrind to confirm no memory leaks and validated proper deallocation of any 
dynamic structures. The code also follows RAII principles, ensuring that memory is automatically released at the end of 
each scope

What was the most challenging part of the assignment?

The most challenging part of the assignment was getting started. This project was much harder than any other assignment 
we have had, so talking with people and collaborating took a big effort to fully get this project rolling. Additionally, 
figuring out which stemming library to use.

UML Analyzer:

![UML_analyzer (1)](https://github.com/user-attachments/assets/ef3599e7-ae9d-4886-8ff3-f9d2ba3b9419)
