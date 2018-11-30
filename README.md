# MaffiaNet Slot Machine

This is some code we produced for MaffiaNet (http://www.maffianet.com) - it renders and runs our slot machine in the casino.

This code requires an external API which we **haven't** included, but the general output of the API is this (comma seperated values):

```
result1, result2, result3, moneyChange, currentMoney
```

where the 3 results are the 3 values between 1 and 9, the moneyChange is the amount of money gained or lost, and the currentMoney is the money the user has (as this updates on the page).

Sample API output:
```
1,5,3,-270,450.217.272
```

The API URL is defined in the JavaScript section, you just have to put it in the variable named "apirequest".
```
apirequest = ""; //insert API url here
```

The slot machine generates random numbers for a while and then uses the numbers given by the API, there is no way of cheating using this system as the winnings have already been calculated before the API gives the result.

# Images

There are multiple images used in this slot machine, there are 9 images (1-9) which are the different items in the slot machine (in MaffiaNet these are lemons, oranges, etc.) and there is also a logo. These all have their own unique names that are used by the script.

The logo uses logo.png, defined here:
```
logo = document.getElementById("logo");
```

The 9 different items are defined here:
```
//import all images of all possible options
var img = document.getElementById("1");
var img2 = document.getElementById("2");
var img3 = document.getElementById("3");
var img4 = document.getElementById("4");
var img5 = document.getElementById("5");
var img6 = document.getElementById("6");
var img7 = document.getElementById("7");
var img8 = document.getElementById("8");
var img9 = document.getElementById("9");
```

Other things, such as the percentages/multipliers, can also be changed in the JavaScript.
Multipliers/percentages can be changed to suit here:
```
//draw text
slotCtx.font = "20px Arial";
slotCtx.fillText("20%", 40, 360);
slotCtx.fillText("15%", 140, 360);
slotCtx.fillText("15%", 240, 360);
slotCtx.fillText("12.5%", 40, 420);
slotCtx.fillText("12.5%", 140, 420);
slotCtx.fillText("3.5%", 240, 420);	
slotCtx.fillText("7.5%", 40, 480);	
slotCtx.fillText("6.5%", 140, 480);	
slotCtx.fillText("7.5%", 240, 480);	
```

This is free to use as long as you credit the author.