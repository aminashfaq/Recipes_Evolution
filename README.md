# Recipes_Evolution

## Contents
1. About Recipes Evolution
2. Getting Started
3. Installing Visual Web Ripper
4. Recipes Script
5. Recipe Constituents
6. Recipe Models
7. Extraction Challenges
8. Solutions to extraction challenges
9. Link to our Extracted Websites



# About Recipes Evolution:
Culinary art is not just about providing food but is a whole complex task involving multiple ingredients, best-spotted spices, and delivering a mixture of appetizing flavors. Every culture has a unique recipe, and each individual has a distinct preference for taste and flavor. Recipes available on the internet nowadays are so vast, introducing an unlimited number of feasible combinations of ingredients just for a single recipe.
By introducing evolutionary computing to the recipes we can create a recipe that is the best among the bests. This computing uses evolutionary algorithms, the science of which is similar to the biological theory of evolution. The algorithm is applied to parent recipes, these recipes will evolve and reproduce a child recipe that is in fact the best combination of its parents.

# Getting Started:
To evolve various recipes over the internet we need some way to collect all the recipe data. The technique we imply to gather all the recipe relevant data is data extraction and the tool we use for this purpose is Visual Web Ripper.

## Installing Visual Web Ripper:
Visual Web Ripper is a powerful web page scraper used to easily extract website data, such as product catalogs, classifieds, financial web sites or any other web site that contains information you may be interested in.

Download Link: http://visualwebripper.com/download/professional

Version: 3

We generate a script with a specific recipe schema and then extract that data with specific attributes. Visual Web Ripper helps us to extract data in various formats like xml, excel, mysql db file, sqlite db file.


## Recipes Script:
Recipes Script generates out .rip file. In the script, we define the recipe model if present for the website. First, we give it a template **Page Area**  and save it, next we give it a **Link** that would help us continue to the next page and name them as **“recipe categories”** and **“recipe category”** respectively. 

For the next step, we take in a list of recipes in the template of **Page Area** and select all our recipes. After saving it as **“recipes”** we make a link of those selected items and give them the template of **Link**. This list will help us open each recipe and is named as **“recipe”**. Once we have provided all the present content of the recipe constituents, we save the script. 
### Extraction:
Next comes the **extraction**. We will extract the website by running our project. It will take some time to get done. The time for extraction varies depending upon the size of the website.
### Generating SQL file
Extracting the website successfully isn’t the end of our work. We will use the extracted file in **SQLite studio** to export a **.sql** file of our data.  After some syntax changes to this .sql file, we upload it to our PHP server.

## Recipe Constituents:
Throughout our journey of exploring recipes, we have come across various constituents of recipes, each of them enhancing their outlook and essence. The elements a recipe comprises, bestow a sense of soul to it. The core recipe constituents we have gathered so far are mentioned as follows:

| **Recipe Property** |	**Description** |
| --- | --- |
| url	| a recipe url that tells the address of the page where the recipe lies |
| name | a recipe’s name identifies it |
| image |	a url that links us to the image showing what’s its final outlook like |
| author |	a person or organization, who produces the content of the recipe |
| cookTime |	Cook Time is the one that tells the duration it takes to cook a recipe |
| prepTime	| Prep Time would be the time to do all the initial preparations as per directions |
| totalTime	| Total Time is the time it took to perform all the instructions and complete the recipe |
| marinateTime |	Marinate time, is used in the recipes where meat takes time to get marinated |
| recipeCuisine	| Recipe Cuisine is the cuisine of the recipe, for example, Italian pasta |
| recipeYield	| Recipe Yield denotes how many people does a recipe serve |
| yield	| Yield to indicate the quantity it will produce |
| cookingMethod |	Cooking Method tells the procedure we undertake to cook the recipe i.e frying, steaming, baking, grilling, etc. |
| commentCount	| There is a Comment Count indicating the number of comments the recipe has received so far |
| dateCreated	| Date Created is the date on which recipe was created |
| datePublished	| Date Published is the date when the recipe was published and introduced to the public |
| dateModified	| Date Modified is the recent date when the recipe was edited |
| keywords	| Keywords are the tags that are used to search |
| aggregateRating |	Aggregate Rating represents the overall ratings of a recipe, it is calculated in the backend by taking an average of the ratings collected so far |
| contentRating |	Content rating, the official rating the recipe has gotten |
| nutrition	| Nutrition indicates the nutrient content a recipe consists of like calories, fat content, protein content, fiber content, and vitamins |
| estimatedCost |	Estimated cost shows the cost of raw materials or supplies |
| recipeIngredients |	Recipe Ingredients is the one representing a list of all the ingredients used to make the recipe |
| recipeIngredient |	Recipe Ingredient is the content showing a single ingredient from the ingredient list |
| recipeInstructions | 	Recipe Instructions  are all the steps that make up the “how-to” part of the recipe, mainly the directions to follow |
| step	| step is a single direction from the recipe instructions list |

![image](https://user-images.githubusercontent.com/75631472/108617460-6a93e500-7438-11eb-920f-f15a0953ceed.png)

## Recipe Models:
While exploring recipes, the models of recipes we see never remain consistent. Studying a wide range of models and inspecting those models side by side, I would like to mention the commonly occurring models below:
-	Recipes by Category
-	Recipes by Ingredients
-	Recipes by Regions
-	Recipes by Diet
-	Recipes by Courses
-	Recipes by Occasions
-	Recipes by Drinks
- Recipe Desserts
- Street food

# Extraction Challenges:
The extraction process isn’t quite easy as it seems and we face several challenges throughout our journey. Some of these challenges are:
-	The recipe content in our browser doesn’t appear in ripper. 
-	An image has a different path than the others.
-	Even if the script is generated right, sometimes it may not appear in extraction.
-	Ingredients or Instructions appear in subheadings and those subheadings can only be selected as a single div.
-	An ad appears in the ripper and we can’t casually treat web pages on ripper like we do in the browser.

# Solutions to extraction challenges:
Let’s discuss solutions to the challenges we have been facing:
-	If the content of the web page doesn’t appear in the ripper, we review the “tree view” of the page and compare it with its insect mode.
-	If an image has a different path, we inspect it in the browser and set its XPath manually.
-	If images can’t be picked on during extraction, we either select “link” from the list or select src in the “attributes” or do the content transformation.
-	To overcome the challenge of ingredients and instructions subheadings being in a single div we select list type “text”, add line breaks, and content transform it.
-	If we want to use ripper as we do in the browser, we select the option “navigate in the browser” option.

# Link to our Extracted Websites:

- AmericanRecipes.xml,
AmericanRecipes.sql	https://www.thespruceeats.com/

- AsianRecipes.xml,
AsianRecipes.sql	https://www.thespruceeats.com/

- Australian&AfricanRecipes.xml,
Australian&AfricanRecipes.sql	https://www.thespruceeats.com/

- SeafoodRecipes.sql,
SeafoodRecipes.xml	https://www.thespruceeats.com/

- Recipesbying.xml,
Recipesbying.sql	https://www.thespruceeats.com/

- RecipesbyDrinks.xml,
RecipesbyDrinks.sql	https://www.thespruceeats.com/

- RecipesbyDiet.xml,
RecipesbyDiet.sql	https://www.thespruceeats.com/

- RecipesbyCourse.xml,
Recipesbycourse.sql	https://www.thespruceeats.com/

- MiddleEasternRecipes.xml, 
MiddleEasternRecipes.sql	https://www.thespruceeats.com/

- Europeanrecipes.xml,
Europeanrecipes.sql	https://www.thespruceeats.com/

- FruitsRecipes.xml,
FruitsRecipes.sql	https://www.thespruceeats.com/

- LatinAmericanrecipes.xml
LatinAmericanrecipes	https://www.thespruceeats.com/

- MeatandSausages.xml
MeatandSausages.sql	https://www.meatsandsausages.com/

- Macheesmo.xml,
Macheesmo.sql	http://macheesmo.com/

- Kitchenbellious.xml,
Kitchenbellious.sql	http://kitchenbelleicious.com/recipe-index/

- Drinksecrets.xml,
DrinkSecrets.sql	http://www.drinksecrets.com/

- Honeysucklewhite.xml,
Honeysucklewhite.sql	https://www.honeysucklewhite.com/

- Cnz.sql,
Cnz.xml	https://cnz.to/recipes-by-category/

- Aol.xml,
Aol.sql	https://www.aol.com/food/recipes/

- Casavenaracion.xml,
Casavenaracion.sql	https://casaveneracion.com/

- Cookwithcampbells.xml,
Cookwithcampbells.sql	https://www.cookwithcampbells.ca/

- Lemonandolives.xml,
Lemonandolives.sql	https://www.lemonandolives.com/greek-recipes/

- Twopeasandtheirpods.xml,
Twopeasandtheirpods.sql	https://www.twopeasandtheirpod.com/

- Latartinegourmande.xml,
Latartinegourmande.sql	https://www.latartinegourmande.com/

- Fleischmannsyeast.xml,
Fleischmannsyeast.sql	https://www.fleischmannsyeast.com/

- Goodcocktails.xml,
Goodcocktails.sql	https://www.goodcocktails.com/recipes/browse_drinks.php?letter=ALL

- Flavorandfortune.sql,
Flavorandfortune.xml	http://www.flavorandfortune.com/dataaccess/recipes.php


