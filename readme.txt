I started my project with scraping problems from codechef using beautiful soup and selenium. The code for the same has been mentioned in a ‘WebScraping Code.txt’ file in the github repository.  Using this code, I extracted 1894 problems and named them as ‘problemCNT.txt’, where CNT=1,2,3… 1894. I also saved the problem names and urls as ‘problem_titles.txt’ and ‘problem_urls.txt’ respectively. Next, I used Python to generate ‘idf.txt’, ‘keywords.txt’, ‘Magnitude.txt’ and ‘TFIDF.txt’ using the taught algorithm, the codes for which have been mentioned in the github repository with appropriate names. Using these text files, I was able to run my app locally. However, after deploying my app on heroku I faced an error: ‘SyntaxError: Unexpected token < in JSON at position 0’, the reason for which was found to be  the large size of ‘TFIDF.txt’. So, I generated a ‘length.txt’ and ‘tf.txt’; here the former file contains 1894 rows, where each row represents the number of keywords in each problem document and later one represents the non-zero values of the TF array. I used these these two files along with ‘idf.txt’ to generate TFIDF array in Javascript. From here on, all the code was written in javascript where we implemented cosine similarity by inputting a string from the search bar to get top five results.

Some points worth mentioning:
I imported the NLTK library into python to filter stopwords and then tokenize our strings into a list from our input string and dataset.
For reading txt files in python, I imported os module to read through all the files in the folder.
For reading txt files in javascript, I used fs.readFileSunc() .
Node js was used to run my app on local server.

https://dsa-algo-search.herokuapp.com/
