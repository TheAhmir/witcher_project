# witcher_project

This project analyzes the 2nd book in The Witcher series, The Sword of Destiny, and visualizes character importance in the second book of the series and the importance of characters throughout the entire series. I used Selenium to scrape the witcher wiki page. After cleaning it, I used Spacy to analyze the data and Networkx and Pyvis to visualize the data in a meaningful way.

## Extraction Strategy
There are several methods to extract relationships from text. However, currently available deep learning models are often trained on a specific dataset and would not be suited for fantasy novels. I decided to go with a simple Named Entity Recognition model with a few rules

1. Every book is tokenized into a large list of sentences
2. I label every sentence by the name of the character(s) that appear in them
3. I define a window size of how far 2 sentences are apart from eachother and assume that if 2 characters are mentions in 2 sentences within this window then their is a relationship between them

## Overview
Through my analysis, I learned that the 2nd book in The Witcher series, The Sword of Destiny, contains a varying level of importance of character throughout the book with the most important characters being Geralt, Yennefer, and Ciri. Geralt had a much larger importance, indicating that he is the main character with Ciri and Yennefer being close to him. I addition, I can conclude from my data that he had the most relationships with "side characters" throughout the book.

![2ndBookCharImportance](https://github.com/TheAhmir/witcher_project/assets/100968856/265f58ab-fc84-40c9-851f-6709404b21a4)

Next, I took the top 5 characters based on importance from my analysis of the 2nd book in the series and visualized their importance throughout the first 8 books in the series. As expected, the level of importance of the character remained similar to the importance in the second book. However, the their is no data for Ciri for the 1st book. This is because she is born in the second book. She then rises to the most important character for books 5 and 6 before Geralt becomes the most important character once again for book 8. This was an interesting discovery and I enjoyed being able to visualize how the events throughout each book affected each characters importance over the course of the series.
