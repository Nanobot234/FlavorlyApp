

# Flavorly

An iOS app that showcases a collection of recipes with a user-friendly interface, dynamically fetching and displaying content. Requires IOS 16 or later 

### Steps to Run the App

1. Clone or download the project from the repository.  
2. Open the `Flavorly.xcodeproj` file in Xcode. Ensure you are using Xcode 14 or later versions
3. Select the "Flavorly" scheme. It likely will be preselected.
4. Click the "Run" button (or press `Cmd + R`).


### Configuration
- The app fetches recipe data from an API endpoint. Ensure your internet connection is active.
- In the `RecipeViewModel` file, you can change the endpoint to test the app's response to various conditions.


## Architecture

Flavorly was built based on the MVVM architectural pattern. The following details how the MVVM pattern is applied in my project

### Models

`Recipe.swift` Defines the components of a Recipe object including the cuisine type and name. The feilds of this object match the JSON object that will be fetched from the server.

`RecipeService.swift`: Fetches data from the various API endpoint and decodes it in a Recipe object. Also includes various data validation statements and error handling. This class can be in its own networking layer as well

***The Recipe.swift file can be found in the `Models` group folder while RecipeService.swift is in the `Services` group***


### Views

`RecipeListView.swift`: The main app screen where Recipes are displayed in a vertical list format. The recipes can be filtered by the cuisine type, and the user can search for a particular recipe by name.

`RecipeCardView.swift`: The card-like view in which each recipe is held. An image of a recipe, the recipe name, and the cuisine type are displayed. The user can also click a button to open various links.

`RecipeUnavailbleView.swift`: A screen to display when no recipes can be shown to the user.

***These files are located in the `Views` group folder. The UIElements folder includes other custom UI elements that were created***

### View Model

`RecipeViewModel.swift`: Interacts with the `RecipeService` class to get recipe data and updates the UI with recipe data and various interactions.

***View model is located in the `ViewModel` group folder***


---
### Focus Areas

I prioritized **UI/UX design** and **app architecture** during development.  

- **UI/UX Design**: A great user experience and an appealing interface are essential for engaging users. I focused on creating an intuitive and visually pleasing design to enhance usability and make the app enjoyable to use.
- 
- **App Architecture**: Maintaining clean, modular, and well-structured code was a key priority. A good architecture ensures the app is scalable and easy to maintain.  

---

### Time Spent

I dedicated approximately **10 hours** to this project, distributed over several days:  
- **60% on front-end development**: Designing and building the UI and user experience.  
- **40% on back-end integration**: Implementing API calls and handling data flow.  

---

### Trade-offs and Decisions

I was fortunate not to encounter significant trade-offs during development, as I successfully implemented all essential features.  

---

### Weakest Part of the Project

One potential weakness is the **loading of the recipe list**. The background for each list item is generated using a computed gradient based on the prominent colors of its associated image. While this creates a visually unique experience, the gradient computation can slow down the app if there are a large number of recipes. Nevertheless, I chose to include this feature because I believe it adds a distinctive and visually appealing touch to the app. I can correct this weakness by performing a cache of the gradients for faster load times. 

---

### External Code and Dependencies

- **[Kingfisher](https://github.com/onevcat/Kingfisher)**: A library for downloading and caching images from the web, used for fetching and displaying recipe photos.  
- **[UIImageColors](https://github.com/jathu/UIImageColors)**: A library for extracting prominent colors from images. These colors are used to generate unique gradient backgrounds for each recipe item.  

---

### Additional Information

As a developer with about **two years of experience**, I am continually learning and growing. Working on this project allowed me to refine my skills and explore new concepts. I am eager to bring my passion for coding and learning to Fetch as a team member or as part of the Fetch apprenticeship program, for which I also applied.  

Thank you for considering my project, and I look forward to the opportunity to contribute further!  
