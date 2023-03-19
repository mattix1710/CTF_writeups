***

# Lazy Game Challenge

![type_binary](https://img.shields.io/badge/type-Binary-red)
![level_easy](https://img.shields.io/badge/level-easy-green)
![points_30](https://img.shields.io/badge/points-30-blue)


## Intro
> I found an interesting game made by some guy named "John_123". It is some betting game. I made some small fixes to the game; see if you can still pwn this and steal $1000000 from me!
> 
>To get flag, pwn the server at: `nc thekidofarcrania.com 10001`

## Solution
After logging onto this server, there is a question how much do we want to bet.<br>
There is also small hint that theKidOfArcania wrote: **I bet you cannot get past $1000000!**

It give me an idea of trying to bet negative number (such as -999999). Hence I could easily loose the game and loose negative number of money!

Loosing negative number is equal to gaining positive value - from the game logic my balance was then over 1000000$.

On end screen, after displaying the information about loosing the game, the message appeared and revealed the flag:

==CTFlearn{d9029a08c55b936cbc9a30_i_wish_real_betting_games_were_like_this!}==