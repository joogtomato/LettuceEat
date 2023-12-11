# LettuceEat
[Link to our product](https://joogtomato.github.io/LettuceEat/).

# Introduction

Our team aims to build a web application that provides information on restaurants’ dietary restrictions to support individuals with specific dietary requirements, such as vegan, vegetarian, and those with celiac disease. Additionally, we plan to implement other helpful features, including a form that users can fill out to submit data of specific restaurants not in our database and a feature that enables users to specify ingredients they want to avoid. Due to time constraints, we may begin with a small number of restaurants in our database, hoping this project would serve as a foundational step toward exploring efficient ways to parse menu information from the internet and organize dietary data.

In our research, we found several first-hand accounts from individuals with food restrictions, including those who have celiac disease, that demonstrate the obstacles they encounter when searching for restaurants that cater to their dietary needs. We believe that creating technologies or providing resources, like our project, that share organized data on restaurant menus will help make the process of finding suitable dining options easier.

# Related Work

[HappyCow is a website for finding vegan restaurant options](https://www.happycow.net/), which enables users to locate vegan restaurants near them and read reviews of those restaurants. There is also an [app that was made by the “Celiac Disease Foundation”](https://celiac.org/about-the-foundation/featured-news/2015/06/celiac-disease-foundation-launches-gluten-free-allergy-free-marketplace-app/) that allows for easier ingredient shopping and provides gluten-free recipes for people with celiac disease. Such platforms provide valuable insights into each restaurant’s offering and share additional helpful resources to support communities with specific dietary restrictions. 

Our project aims to draw inspiration from these examples in supporting the community through providing well-organized restaurant data. Notably, we learned that existing resources tend to focus on particular dietary preferences, rather than considering the intersectionality among dietary needs by combining multiple options. Acknowledging the intersectionality of dietary and accessibility needs, we intend to explore this idea further by allowing users to select multiple dietary options (vegan, vegetarian, and celiac) as well as specify ingredients they prefer to avoid. This customization feature will embrace intersectionality and help users to address their specific requirements.

# Methodology

## Parser that extracts menu data into a CSV file 

Our parser works on restaurants that have the menu along with the ingredients for each menu item on a webpage. To implement the parse, we used the Python libraries BeautifulSoup and Selenium. First, we use Selenium to parse the website into html, and print out the html. Then, we manually look in the html for the tags where the menu items and menu descriptions are stored. Next, BeautifulSoup is used to search the website for those menu items and descriptions and store the results in an array. This is used to create a csv using the pandas package. For each restaurant, we created a csv file with a column for the menu item names, a column for the corresponding menu description, and an optional column for the dietary information (like gluten free or vegan) if that information is on the website. 

# Disability Justice Perspective

## Intersectionality

**Intersectionality** is the idea that people have many different identities that impact them in many ways. Our project will address this principle by supporting a plethora of different dietary restrictions that people could have on top of their disability dietary restrictions. Initially, we just focused on have broad filters such as for vegan, vegetarian, and gluten-free. However, this design excludes people who have more niche food restrictions. For example, people with certain chronic illnesses, such as IBS (irritable bowel syndrome), may not eat a unique set of food items. Or someone might be allergic to a single food item such as carrots. Thus, in our revised design, we include a build-your-own filter that allow people to enter in the specific food items that they can’t eat. This supports the intersectionality principle by allowing people with a wide variety of food restrictions to still use the website. 

## Collective Access

**Collective Access** is the idea that access needs are shared, encouraged, and supported by the community. It is everyone’s responsibility to support others' needs when they are communicated. Our project addresses this principle by including a feature where individuals can request for new restaurants to be added to our database. Our website also includes a feature where people can report accessibility concerns about the website. Listening to the users of the website is critical to centering collective access in our project so that we can address any access needs as necessary.

# Learnings and Future Work

There are several avenues that future work that we considered when initially designing our project. First, we would like to incorporate Yelp reviews to allow our website to also display accessibility reviews for the restaurant. This would include searching for reviews that indicate whether the place is wheelchair accessible inside and outside the establishment and whether the menu is accessible. A feature could also be included to allow people to filter restaurants on accessible features of the restaurant. 

Additionally, currently, our website only includes about 15 restaurants in the U-District. However, this is not a comprehensive list, and it would be great to include more restaurants in our website, in and outside the U-District. One step for this is to fully automate the process for parsing menus. Currently, our workflow includes a manual step for finding the menu html tags,  so fully automating this would allow to more quickly process more restaurants. 

Lastly, we could improve the accuracy of our ingredient filtering. For example, if there is a synonym of an ingredient or an ingredient not explicitly mentioned in the menu description, our algorithm can be improved so those would still be filtered out. 
