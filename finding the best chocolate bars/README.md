# Finding the best chocolate bars

## Overview
The goal of this project is to find the best chocolate bars by analyzing the data given by [flavors of cacao](https://flavorsofcacao.com/). The analysis presented here will answer specific questions such as:
- What is the average rating by country of origin?
- How many bars were reviewed for each of those countries?
- Is the cacao bean's origin an indicator of quality?

## Technical Aspect
This project is mainly done using dataframe manipulation and seaborn plots for visualization.

## Installation
The code is written in Python 3.8. If you don't have Python installed, you can find it here(https://www.python.org/downloads/).

## Run
Windows
https://docs.python.org/3/using/windows.html

Mac
https://docs.python.org/3/using/mac.html

Unix (Linux, FreeBSD and OpenBS, OpenSolaris)
https://docs.python.org/3/using/unix.html

## To do
There are many questions left to explore and analyze to further strengthens my claim that bean of origin is an indicator of quality.

## Technologies used
<p align="left"> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://jupyter.org/" target="_blank" rel="noreferrer"> <img src="https://github.com/devicons/devicon/blob/master/icons/jupyter/jupyter-original.svg" alt="jupyter" width="40" height="40"/> </a>

## Team
Branislav Galović

# Analysis

## Average Rating
![image](https://user-images.githubusercontent.com/102976455/217013060-6960fc76-bcfc-4fd0-914e-7415515fdbe0.png)
There are a lot of **single rows or at least a couple of rows**, for example, Tobago for the column bean_origin with a rating of **3.25 and 4.00, averaging 3.75**. For that reason, there are a lot of outliers which might throw off the correct average rating and some other things, which I will adress later. I figured I would first count the **top couple most frequent values**, and get the average rating that way, dodging the outliers. **Outliers might be occuring due to lack of data, so keep that in mind.**

### **Average Rating by Country of Origin**
I calculated the average rating by country of origin. We can see that **Venezuela, Peru, Dominican Republic, Ecuador, Madagascar and Blend** are all somewhere between **3.00 and 3.30**. With **highest** being Madagascar with 3.669, and **lowest** Blend with 3.0385.

### **Average Rating by Company Location**
U.S.A. had the highest counting number of 1136, while all the other company locations being below 200. Top 10 company locations are averaging between **3.0 and 3.40**. With **highest** being Australia with 3.3585, and **lowest** Ecuador with 3.0388. Venezuelan chocolate's company locations are from U.S.A, Canada, France, U.K, Italy, Spain and Venezuela. They are all from the top 5 most frequent company locations!

### **Average Rating by Year Reviewed**
**I did not count the top 5 most frequent values**, since the column year_reviewed is normally distributed. The highest average rating year is 2017, with 3.3619, and lowest being 2020 with 3.2562.

### **Cocoa Percent by Country of Origin**
Histogram is normally distributed, however there's a **single** and **highest** row being with the rating 3.75, which is 50%. Therefore, I will count most frequent number of cocoa_percent in the top 6 country of origins. We see that for all the 6 countries, the most frequent percent of cocoa is **70%**, with Peru being the one with the most chocolate with 70%.

### **Average rating by Ingredients.**
- B = Beans,
- S = Sugar,
- S* = Sweetener other than white cane or beet sugar,
- C = Cocoa Butter,
- V = Vanilla,
- L = Lecithin,
- Sa = Salt

We can see that the highest average rating for the number of ingredients is a chocolate with only **3 ingredients**. **Beans, Sugar and Cocoa Butter**. While the lowest average rating has 4 ingredients. **Beans, Sugar, Cocoa Butter, and Salt**. We can see that each of those 5 bars has both Beans and Sugar, which the 2nd highest average rating exactly has.

### **Average Rating by Bar Name**
Other name for this column is specific bean origin. For example, there's a chocolate from Venezuela called **Sur del Lago**, **Anamalai** from India, **Semuliki Forest** from Uganda, **Crillo** from Madagascar, etc. We can see that the specific bean origin matches the the country of origin from our first plot. Both **Chuao**, and **Venezuela** chocolate is exactly from Venezuela! The lowest average rating is 2.9207, Peru.

![image](https://user-images.githubusercontent.com/102976455/217015011-165c485b-1171-4f60-ac71-282f0768cdcd.png)
We can see that four countries of origin (Venezuela, Peru, Ecuador and Madagascar) have the **highest average rating of ingredients**, which is Beans, Sugar and Cocoa. Meanwhile Dominican Republic only has Beans and Sugar, and Blend has Beans, Sugar, Cocoa Butter, Vanilla and Lecithin. And the second highest on the plot, every country except Dominican Republic only has **Beans and Sugar**.

## Reviews
![image](https://user-images.githubusercontent.com/102976455/217013776-5f4a7b79-a141-4047-997a-9cb785a58065.png)
### **Number of Reviews by Country**
We can see that the most number of reviews is Venezuela, which is expected, since a lot of beans come from Venezuela. I counted all reviews separated with a comma.

### **Number of Reviews by Bar Name**
Madagascar has the most number of reviews, which is again, expected. A lot of chocolates are coming from Madagascar with its name.

### **Number of Reviews by Company Location**
As I've said before, U.S.A. is a location of over dozens of bean origins! Therefore it's expected that U.S.A has the most amount of reviews.

### **Number of Reviews by Cocoa Percent**
Same with cocoa percent, most of the chocolate has 70% of cocoa. Seems like that's a perfect amount of cocoa.

### **Number of Reviews by Number of Ingredients**
The most chocolate with reviews has 3 ingredients.

### **Number of Reviews by Ingredients**
The most popular ingredients, Beans, Sugar and Cocoa. With Beans and Sugar following right after it.

### **Number of Reviews by Rating**
Rates between 3.0 and 3.5 is the perfect spot for a chocolate.

### **Most Frequent Reviews**
'Cocoa' is the word that most people use when reviewing chocolate! Following it is sweet, and nutty. Which is most likely connected to the 2 most used ingredients, Sugar and Cocoa.

## **Is the cacao bean's origin an indicator of quality?**
![image](https://user-images.githubusercontent.com/102976455/217014056-376c6588-53ce-4679-af0f-a740228f1b8c.png)

Let's first summarize what each **quality** of the best chocolate is, based on visualizations above. First, let's list the best top five countries. **Venezuela, Peru, Dominican Republic, Ecuador, and Madagascar.** What do all of these countries have in common?

- For starters, they are all grouped in between 3.00 and 3.30 of average rating, pretty close to each other. Venezuela has the country the highest number of 4.00 ratings, which is 20. And Peru, with 19. The only one without a single 4.00 rating is Dominican Republic. Venezuela also has the highest number of of chocolates made in this dataset.

- Each of those countries have a company located in U.S.A.

- In each of those top five countries, the most used percent for a chocolate is 70%.

- The highest average rating for ingredients is Beans, Sugar and Cocoa. Also the most used combination.

- Only Venezuela has two chocolates listed in the highest average rating, out of 6.

- Most frequent reviews are: cocoa, sweet, nutty, creamy.

The best qualities a chocolate have is:
- **Beans, Sugar, and Cocoa**
- **70% of cocoa**
- **Sweet, nutty, and creamy**
- **From Venezuela**

To answer the question, cacao bean's origin indeed is an indicator of quality.
