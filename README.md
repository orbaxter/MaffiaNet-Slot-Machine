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