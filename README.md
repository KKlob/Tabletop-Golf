************ RE-WRITE GAME *************************
Game will be made in GameMaker
Sprites will be made using PiskelApp.com

Idea is a 32-bit style Golf RPG game with dice roll mechanics to describe swing
Each shot will have certain requirements based on club selected, modifiers being used, wind/lie conditions
Player will roll a set number of die and chose how to apply values to shot
Will still use some concepts already thought out, just implemented in a different way



# Tabletop Golf
The premise is bringing golf to the tabletop via dice roll mechanics and a DnD style equipment system. Solo play is available though it is encouraged to play as 2-4 players + 1 GM. GM is an optional role but it makes it more fun. The twist is the game is a PvP type game. As in golf, the objective is to score the lowest you can and beat the other golfers in your group. You are competing against the other players. Along your round of 18 holes, you will have opportunities to acquire new equipment in the form of Clothes and Clubs. You will also be able to grab shot modifiers that can change the roll requirements for a shot as well as one-time-use abilities that can help your golf game or hamper an opponent. Who will come out on top?

## Base Gameplay flow overview
1) A GM will be chosen (or players can take turns being the GM for one another)
2) Players will create a golfer via assigning stat points + choosing a base bag of clubs
3) The first hole map is laid out between the players and the GM.
4) GM will roll for weather and wind conditions. Wind direction is rolled every hole.
5) Players will take turns making a tee shot. Gameplay turns follow regular golf rules. (Furthest from pin goes)
6) A Players shot consists of the following stages
   - Choosing aim point on hole map + distance to hit
   - Choosing a club to hit
   - Rolling the designated dice on the club
   - Calculate result of swing
   - GM calculates wind + kick results
   - Roll luck check
   - Mark new ball position on hole map
7) When a player makes the green, the hole's Green map is used to determine putt modifiers
   - Distance to pin
   - Uphill / Downhill
   - Moving Left / Right
8) A Player's putt consists of the following stages
   - Calculating putt modifiers
   - Option for shot modifiers / abilities
   - Roll for putt
   - Calculate result of putt
   - Roll luck check if applicable
   - Mark new ball position on hole map
   - When hole made / within tap-in range, count strokes and move to next hole

Every three holes is considered a "Match". After each Match, each golfer is given stat points to distribute, new equipment option, and other choices. After each golfer is satisfied, the next Match begins. After 6 Matches, the Player with the lowest strokes is the winner. In case of a tie, a Playoff Match will start. No stat points are given after the 6th Match nor any Playoff Match. Only equipment / shot modifiers / etc. will be offered.

## Create your Golfer
To create a golfer, a player must distribute stat points among the different attributes of their golfer
 - Power : Influences all golf clubs. Main influence in determining distance.
 - Technique : Influences all golf clubs. Main influence in determining contact with the ball.
 - Control : Influences all golf clubs. Main influence in determining control over ball flight.
 - Finesse : Influences irons and wedges. Main influence in determining ball spin.
 - Luck : Influences kick + lucky saving throws. Main influence in determining hole outs / close putts.

Each attribute starts with 1 point. A Player is given 10 points to distribute, with an additional 3 points given after every Match.

After creating a golfer, the player will receive a base bag of rental clubs from the course. These clubs all have the same stats and requirements. All golfers are equipped with base clothing (Hat, shirt, pants, shoes, gloves) that have no modifiers on them. There will be opportunities to acquire new clubs, equipment, and other gear after every 3-hole Match.

## Post-Match Gameplay Flow
After each 3-hole Match, a post-match cart girl break will begin. 
1) GM will generate clubs, clothes, shot modifiers, and abilities that will be available to the players
2) Players will take turns doing the following
   - choosing up to two clubs to swap from their bag (optional)
   - choosing a single article of clothing to swap out (optional)
   - choosing a single shot modifier to add to their shot pool
   - choosing a single ability to take (One only per golfer)
3) All charges of "Lucky Bounce" are refreshed

## End of Round Overview
After a full round of 18 holes (6 full 3-hole Matches) each players golfer has evolved into a highly skilled player. Strokes are tallied up. The player with the lowest score is the winner. In the event of a tie, each tied golfer will play a Playoff Match of another three holes.

Before the playoff match, there will be one final visit from the cart girl. She will have clubs, shot modifiers, and abilities to choose from. Only one of each may be taken. If there is still a tie after the Playoff Match, another is played. There will be no more cart girl visits.
