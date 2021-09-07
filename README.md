# C# Live Project

In one of my last courses of the Tech Academy Software Developer boot camp, I was thrown in to an existing project for a theater website. This site was built with the C# MVC framework, and my task was to implement a Cast Member section of the site. To do this, I implemented a code-first database to save cast members to, with their pertinent information, plus the appropriate CRUD pages.

This also involved a Cast Member controller, which I programmed to display the cast members according to the production they were in. 

![Controller](https://user-images.githubusercontent.com/83970546/132374736-b4552a11-743d-4c90-9549-1715a12c81bf.png)

Also in the controller, I implemented a search feature. As can be seen above, if the search bar is empty, then all cast members are displayed. However, when user input is searched, only cast members where the user input is contained in the name or the bio is shown. This also hides any of the productions that no longer show any cast members. This was done using Razor syntax within my HTML Index page. First, I iterated through the model to find how many different production titles there were, and saved each title to a list.

![Index1](https://user-images.githubusercontent.com/83970546/132375830-342c5509-5406-4ee9-b1bf-7d9be24ad9bd.png)

Next, I iterated through the model again to build the index page. Since the controller already ordered the cast members by production title, I could then print each cast member to a card under their production title.

![Index2](https://user-images.githubusercontent.com/83970546/132376045-5846968c-ea76-44b0-b536-b3e2006b84b7.png)

The output looked like this:

![IndexPage](https://user-images.githubusercontent.com/83970546/132376074-0bc681d0-ac0e-421a-a30e-4edabf80e5af.png)

As you can see, there is some nice CSS styling and hover effects when a user mouses over the cast members. I was required to stick within the constraints given to me, like certain layout features and color schemes, but overall I was happy with how things turned out. Also, please take no mind over the fake names and images for cast members. I simply added those names for testing purposes, and the images came from a random array of images.

One bit of coding that I enjoyed implementing, without any direction to do so, was on the Details page for cast members. When adding a new cast member, there were certain fields like "MainRole" (which was built with an Enum), "Character", "Year Left" (when the cast member left the cast), and a "Current Member" check box. What I decided to do was only display the Character information if the MainRole was an actor. This is because if the MainRole was in production or a different area, they would not play a character. No need to display blank info. Also, if the Current Member box was checked, that meant that the cast member had not left staff, so the Year Left info would also not be displayed. These little sections of logic made for a more appealing product. See below for the code and display.

![Details Logic](https://user-images.githubusercontent.com/83970546/132377144-686a2755-5492-4a68-9406-7ed547619019.png)

![DetailsPage](https://user-images.githubusercontent.com/83970546/132377161-24b1dbce-d4af-4d28-9a1a-5009e1f23008.png)
