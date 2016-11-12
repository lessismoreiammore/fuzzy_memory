
#What is a hipster, man?#

My project's main purpose was to create a simple memory game in pure HTML, CSS, JS and place it in a nice UI.
I prefer to make a kind of eLearning project about hipsters.

The planning and implementation process you can see [here](https://trello.com/b/HxNq4h6u/fuzzy-memory).

##1. Example##

This screenshot show the basic flow of the game

*Beginning of the game*

![screenshot_1](readme_files/screenshot_1.png)

*End of the game*

![screenshot_2](readme_files/screenshot_2.png)

The game is repeated after the user presses the **"Play again↻"** button.

##2. Installation##

No installation is required since the project is a simple web application with a JS script inside.

To run the project, simply click the [index.html](index.html) in the project folder.

The project was tested in major modern browsers (Safari, Chrome, Firefox, etc.) and behaves correctly.

The code was checked by the [W3C Markup Validation Service](W3C Markup Validation Service) and [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/).

All the selectors were checked whether they require any web browser prefix.

##3. Program flow##

The website is organized in a sequential way. Firstly, the users get to know about common hipster stereotypes.

Secondly, the users look at the "study" material so that to enhance their knowledge in the topic.

Last but not the least the play a simple memory game to match pairs of features that only true hipsters have!

The game result is stored so that to be shown along with a message with further steps to dive into the topic if necessary. The message is shown only if all the pairs are solved.

The rating system is chosen on the basis of game experience and estimated to such levels based on the amount of clicks done by the user:

scores amount | type of level
-------|----------------------------------------
8-16 | The super hipster level
16-24 | The middle hipster level
24 or higher | Not the hipster level

##4. Code example##

This code snippet solved the problem to write an output to the user at the end of the game

```javascript
function userOutput(j, i) {
    let newH = document.getElementById('message');
    newH.textContent = "Your hipster score is " + j;
    let newP = document.createElement('p');
    newP.id = "deleted";
    newP.textContent = i;
    document.getElementById('result').appendChild(newP);
}
```

This code snippet helps to erase the message after the user presses reshuffle button
```javascript
var deletedChild = document.getElementById('deleted');
if (typeof(deletedChild) != 'undefined' && deletedChild != null) {
    var sorrowParent = document.getElementById('result');
    sorrowParent.removeChild(deletedChild);
}
```

##5.Image copyright##

Backround image [courtesy](https://images.unsplash.com/photo-1444374711498-d02625421725?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&s=6df0cd196b9e26)

Game icons [courtesy](http://www.flaticon.com/packs/hipster-style-2)
