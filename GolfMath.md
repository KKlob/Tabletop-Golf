# Stats, Clubs, Swings, and Distances. How the Fuck does this work?!

This will be a working document on how the stats, clubs, swings, and distances are done. This will provide the basic structure for the math and code that follows.

## Attributes
Attributes determine the Golfer's strengths and weaknesses. Clarity and Simplicity in attributes is top-most priority as it will drive what clothes / clubs / shot modifiers / abilities a player will choose to get their Golfer ahead of the competition. A Golfer's game has been divided into 4 main swing attributes and a luck attribute (as luck is a functional component of the real game). Any golf club will have a base modifier for each attribute (X) that helps determine how a player's skill influences the shot (rounded to the nearest 0.5). Some clubs take advantage of a high-skill player while others offer more forgiveness for low-skilled players. Clothes will also add certain modifiers to a golfer's stats. 

#### Power: Main influence in determining distance. 
 - Shot Power >= Club Power Req
 - Shot Power = Power roll + (Power Stat / X )
#### Technique: Main influence in determining contact with the ball.
 - Low Req <= Technique Req <= High req 
 - Shot Technique = Technique roll
 - Technique stat / X = additional forgiveness to Technique Roll
#### Control: Main influence in determining control over ball flight.
 - Low req <= Roll <= High req
 - Shot Control = Control Roll
 - Control stat / X = additional forgiveness to Control Roll
#### Finesse: Main influence in determining ball spin + kick
 - Low req <= Roll <= High req
 - Shot Finesse = Finesse Roll
 - Finesse stat / X = additional forgiveness to Finesse Roll
#### Luck: Influences kick + lucky saving throws. Main influence in determining hole outs vs. tap-in putts.

## Clubs
Every club has it's own features for roll requirements as well as how a golfer's stats affect the swing. Each category of club (Driver, Fairway Wood, Iron, Wedge, Putter) will have different ways stats affect a swing result as well as within each category of club. A club's Power roll is always used as the Primary value for distance calculation. A club will also have a combination of two attributes that will weigh into the distance calculation (Technique / Control / Finesse)
*Note the Putter has a range for Power and does not have a Finesse Roll. The Putting section will explain why.

The table below outlines all of the clubs currently in the game as well as the roll requirements and modifiers for each.

<table>
	<tr>
		<th>Club Category</th>
		<th> High Req </th>
		<th> Medium Req </th>
		<th> Low Req </th>
	</tr>
	<tr>
		<td> Drivers </td>
		<td> Power / Technique / Control </td>
		<td> Control </td>
		<td> Finesse </td>
	</tr>
	<tr>
		<td> Fairway Woods </td>
		<td> Power / Technique </td>
		<td> Control </td>
		<td> Finesse </td>
	</tr>
	<tr>
		<td>Longer Irons (3i - 6i) </td>
		<td> Power / Technique / Control </td>
		<td> Technique / Control / Finesse </td>
		<td> Finesse </td>
	</tr>
	<tr>
		<td> Shorter Irons (7i - 9i) </td>
		<td> Technique / Finesse </td>
		<td> Power / Technique / Finesse / Control </td>
		<td> Control </td>
	</tr>
	<tr>
		<td> Wedges </td>
		<td> Technique / Finesse </td>
		<td> Power / Technique / Finesse </td>
		<td> Power / Control </td>
	</tr>
	<tr>
		<td> Putters </td>
		<td> Technique / Control </td>
		<td> Power </td>
		<td> Finesse </td>
	</tr>
</table>

----------------------
( P ) = Primary Attribute
( S ) = Secondary Attribute
<table>
	<tr>
		<th> Club Brand </th>
		<th> Club Type </th>
		<th> Power Req </th>
		<th> Technique Req </th>
		<th> Control Req </th>
		<th> Finesse Req </th>
		<th> Max Carry Distance </th>
		<th> Club modifiers </th>
	</tr>
	<tr>
		<td> Rental </td>
		<td> Driver (D20) </td>
		<td> 18 | 1.5</td>
		<td> 8-11 | 1.5 (P)</td>
		<td> 7-12 | 1.5 (S)</td>
		<td> 5-14 | 1.5</td>
		<td> 230 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> 3 Fairway Wood (D20) </td>
		<td> 17 | 1.5</td>
		<td> 8-11 | 1.5 (P) </td>
		<td> 7-12 | 1.5 (S) </td>
		<td> 6-13 | 1.5</td>
		<td> 190 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> 6 Iron (D20) </td>
		<td> 16 | 1.5 </td>
		<td> 8-11 | 1.5 (P) </td>
		<td> 7-12 | 1.5 (S) </td>
		<td> 6-13 | 1.5 </td>
		<td> 175 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> 7 Iron (D20) </td>
		<td> 15 | 1.5 </td>
		<td> 8-11 | 1.5 (P) </td>
		<td> 7-12 | 1.5 (S)</td>
		<td> 7-12 </td>
		<td> 160 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> 8 Iron (D20) </td>
		<td> 14 | 1.5 </td>
		<td> 8-11 | 1.5 (P) </td>
		<td> 7-12 | 1.5 </td>
		<td> 7-12 | 1.5 (S) </td>
		<td> 145 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> 9 Iron (D20) </td>
		<td> 13 | 1.5 </td>
		<td> 8-11 | 1.5 (P) </td>
		<td> 7-12 | 1.5 </td>
		<td> 7-12 | 1.5 (S) </td>
		<td> 130 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> Pitching Wedge (D20) </td>
		<td> 12 | 1.5 </td>
		<td> 8-11 | 1.5 (S) </td>
		<td> 6-13 | 1.5</td>
		<td> 8-11 | 1.5 (P) </td>
		<td> 115 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> Sand Wedge (D20) </td>
		<td> 11 | 1.5 </td>
		<td> 8-11 | 1.5 (S) </td>
		<td> 6-13 | 1.5 </td>
		<td> 8-11 | 1.5 (P) </td>
		<td> 90 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> Putter (D20) </td>
		<td> 8-11 | 1.5 </td>
		<td> 8-11 | 1.5 (P) </td>
		<td> 8-11 | 1.5 (S) </td>
		<td> N/A </td>
		<td> N/A </td>
		<td> None </td>
	</tr>
</table>

## Rolling for swing
Every club will have four roll requirements to perform a good swing. A player must roll all requirements to achieve a perfect golf shot. Not achieving all roll requirements results in a lesser golf shot (hard slice, less distance, lower flight, etc.)

- Player chooses Club / Shot Modifiers / Abilities and is ready to roll.
- Player uses designated club die to roll requirements
- Player calculates shot result

## Distances
Each hole will have a map with a hex grid overlaid on top. Each hex will represent 10 yards. Distance calculations will be displayed in both yards and hexes. It will be displayed in the following format.
 - Distance: XXX yards
 - Left / Right: +/- XXX yards
To determine where the ball rests, follow the aim line out to Distance, then move left/right.

The distance a ball will go depends on the Golfer and the club they swing. Distance is primarily weighted by a swing's Power roll as well as by a club's Primary and Secondary attributes (Technique / Control / Finesse). 

Putting is a separate calculation and will be explained later.

#### Power - Main attribute for distance
If the Power roll meets/exceeds the roll requirement, the distance calculation starts with the following:
  - Distance = Aim Point Distance.

If the Power roll hits the highest value (EX: D20 rolls a 20), the distance calculation starts with the following:
 - Distance = Aim Point Distance + ( APD * 10%)
 - Clubs can change this to be more than just highest value (?)

If the Power roll does not meet the roll requirement, The distance calculation starts with the following:
 - Pd = Aim Point Distance * (Power Roll / Power Req)

#### Primary and Secondary - Attributes that affect Power Distance
If both attributes meet their breakpoints, no additional calculation is necessary

If Primary / Secondary attribute fails to meet breakpoint, we find the difference between the roll and the breakpoint. The chart below outlines how it affects distance:

<table>
	<tr>
		<th> Difference </th>
		<th> Primary </th>
		<th> Secondary </th>
	</tr>
	<tr>
		<td> 1 </td>
		<td> 3% </td>
		<td> 1% </td>
	</tr>
	<tr>
		<td> 2 </td>
		<td> 5% </td>
		<td> 2% </td>
	</tr>
	<tr>
		<td> 3 </td>
		<td> 8% </td>
		<td> 4% </td>
	</tr>
	<tr>
		<td> 4 </td>
		<td> 12% </td>
		<td> 7% </td>
	</tr>
	<tr>
		<td> 5 </td>
		<td> 17% </td>
		<td> 11% </td>
	</tr>
	<tr>
		<td> 6 </td>
		<td> 23% </td>
		<td> 15% </td>
	</tr>
	<tr>
		<td> 7 </td>
		<td> 30% </td>
		<td> 20% </td>
	</tr>
	<tr>
		<td> 8 </td>
		<td> 38% </td>
		<td> 26% </td>
	</tr>
</table>
    
Distance calculation is as follows: (Yd = Y Distance)
 - Yd = Pd - ( [ Pd * Primary ] + [ Pd * Secondary ] )

#### Control - Main attribute that affects Draw/Fade 
- For every shot, the "aim line" and intended ball flight is **always** straight.
- Shot modifiers can alter this behavior to allow for intended draw/fade path (explained in shot modifiers)
- The Control roll designates if a ball will stay on path or hook/draw/fade/slice.
- Control roll below breakpoint = Hook/Draw (Left)
- Control roll above breakpoint = Fade/Slice (Right)
- The table below helps determine how far off the ball flight is

<table>
	<tr>
		<th> Difference </th>
		<th> x% of Total Distance </th>
	</tr>
	<tr>
		<td> 1 </td>
		<td> 2% </td>
	</tr>
	<tr>
		<td> 2 </td>
		<td> 4% </td>
	</tr>
	<tr>
		<td> 3 </td>
		<td>6% </td>
	</tr>
	<tr>
		<td> 4 </td>
		<td> 8% </td>
	</tr>
	<tr>
		<td> 5 </td>
		<td> 10% </td>
	</tr>
	<tr>
		<td> 6 </td>
		<td> 12% </td>
	</tr>
	<tr>
		<td> 7 </td>
		<td> 14% </td>
	</tr>
	<tr>
		<td> 8 </td>
		<td> 16% </td>
	</tr>
</table>

The following equation determines the distance to the left/right the ball landed relative to path. 
 - (Xd = X Distance, Cd = Control Difference %)

Xd = Yd * Cd 

#### Combined Distance Calculations
To summarize, the following is a quick recap of all calculations. 

Pd = Power Distance
- IF Power Roll >= Power Req: Pd = Aim Point Distance
- IF Power Roll == highest roll value: Pd = Aim Point Distance + (APD * 10%)
- IF Power Roll < Power Req: Pd = Aim Point Distance * (Power Roll / Power Req) 

Yd = Y Distance
Yd = Pd - ( [ Pd * Primary ] + [ Pd * Secondary ] )

Xd = X Distance, Cd = Control Difference %
Xd = Yd * Cd

Net Yd = Yd - Xd

Distance displayed as [Yd , Xd]
 - Move down aim path to Yd yards, then move left/right Xd yards.

#### Finesse Kick / Rollout

## Putting
The putting process is different from any other golf shot because it only has one lie type (Unless modified) and stays grounded. The ball is subject to power, slopes and undulations across the green. Each Hole comes with a "Green Map" showing the different areas that are sloped, the direction they slope towards, as well as any modifiers that area will have on a putt.

Putters will always have a range for Power instead of a general check to allow for shot / long putts. They will also only have two additional attributes labeled Primary and Secondary. These represent the line you choose. 

Green Modifiers affect the following:
 - Distance (Uphill / Downhill): Affects the Power Roll
 - Direction (Left / Right): Affects the Primary/Secondary Attribute Rolls
 - A combination of both

After determining the Green modifiers, the process and calculation are as follows:

#### Distance:
Calculate distance (in ft.) from pin by drawing a straight line from ball to pin.
Rolling Power within putter's Power req means good speed
 - Over breakpoint: too much speed
 - Under breakpoint: too little speed

The table below describes how Over/Under breakpoint translates to distance:
<table>
	<tr>
		<th> Over / Under </th>
		<th> % Distance </th>
	</tr>
	<tr>
		<td> 1 </td>
		<td> 3% </td>
	</tr>
	<tr>
		<td> 2 </td>
		<td> 6% </td>
	</tr>
	<tr>
		<td> 3 </td>
		<td> 9% </td>
	</tr>
	<tr>
		<td> 4 </td>
		<td> 12% </td>
	</tr>
	<tr>
		<td> 5 </td>
		<td> 15% </td>
	</tr>
	<tr>
		<td> 6 </td>
		<td> 18% </td>
	</tr>
	<tr>
		<td> 7 </td>
		<td> 21% </td>
	</tr>
	<tr>
		<td> 8 </td>
		<td> 24% </td>
	</tr>
</table>

Putt Power Distance = Putt Distance +/- (Putt Distance * Power Difference %) *Rounded to nearest 0.5 ft

EX: For a 20ft. putt with no green modifiers:
 - within breakpoint: Distance = Putt Distance
 - Over 2: Distance = Putt Distance + (Putt Distance * 6%) | 21.2 -> 21 ft Distance
 - Under 4: Distance = Putt Distance - (Putt Distance * 12%) | 17.6 -> 18ft Distance

#### Primary / Secondary Club attributes - Distance Calculation
The Primary and Secondary club attributes will influence distance in that they represent the line you take. Green modifiers may affect one or both of the Rolls for these attributes.

 - Over: Right of line
 - Under: Left of line

The table below describes how Over/Under breakpoints influence distance:
<table>
	<tr>
		<th> Over/Under </th>
		<th> Primary % </th>
		<th> Secondary % </th>
	</tr>
	<tr>
		<td> 1 </td>
		<td> 3% </td>
		<td> 1% </td>
	</tr>
	<tr>
		<td> 2 </td>
		<td> 6 % </td>
		<td> 3% </td>
	</tr>
	<tr>
		<td> 3 </td>
		<td> 9% </td>
		<td> 5% </td>
	</tr>
	<tr>
		<td> 4 </td>
		<td> 12% </td>
		<td> 7% </td>
	</tr>
	<tr>
		<td> 5 </td>
		<td> 15% </td>
		<td> 9% </td>
	</tr>
	<tr>
		<td> 6 </td>
		<td> 18% </td>
		<td> 11% </td>
	</tr>
	<tr>
		<td> 7 </td>
		<td> 21% </td>
		<td> 13% </td>
	</tr>
	<tr>
		<td> 8 </td>
		<td> 24% </td>
		<td> 15% </td>
	</tr>
</table>

Primary Distance (Left/Right) = Putt Distance * Primary Difference %
Secondary Distance (Left/Right): Putt Distance * Secondary Difference %

These two will determine how far off the line a putt is as well as what direction it went.

#### Bringing Putt Power Distance + Primary/Secondary Distance together

Bringing back our Power Distance math:
Putt Power Distance = Putt Distance +/- (Putt Distance * Power Difference %) *Rounded to nearest 0.5 ft

Combining this with our previous 20ft. putt example
For a 20ft. putt with no green modifiers:
Power: hit | Technique: -1 | Control: +2
Power Distance =  20ft (Hit within breakpoint)
Primary (Technique): 20ft * 3% = 1ft. left
Secondary (Control): 20ft * 3% = 1ft. right

In this scenario, the Primary and Secondary traits would cover each other and the putt would then end with a luck check. We end with a luck check as Putting (and golf in general) does have a certain amount of luck to it. The following will outline Putting rules:
 - Putts within 3ft. are a standard tap in. 
 - Putts outside 3ft. must be rolled and will have this gameplay flow:
	 - distance will be counted, aim line drawn and Green modifiers applied to the putt
	 - Roll is done for each of Putter's attributes
	 - Putt roll is calculated
		 - IF Putt Power Distance is on point and Primary/Secondary keep ball on line, a luck check is done
			 - Base check is TBD, if passed ball is made
				 - luck roll is based on putt distance, number of green modifiers, and a golfer's luck attribute
			 - If luck check fails, ball just misses and is considered a tap in
		- Else IF Putt Power Distance is on point and Primary/Secondary do not keep ball in line
			- calculate left/right distance, move ball position to new position.
				- IF Ball is within 3ft. = tap in
				- ELSE Roll new putt
		- ELSE 
			- calculate Putt Power Distance and Primary/Secondary Distances, calculate new ball position and place.
				- IF within 3ft. = tap in
				- ELSE Roll new putt
		
## Luck Check
Luck check is based on the following traits of any shot
 - A Golfer's Luck attribute
 - The shot's Distance relative to it's max distance (N/A on Putters | Calc'd on Putt Distance instead)
 - The anticipated lie modifiers (Green Modifiers for Putting)
 - Any weather conditions that may apply

***** NOTE: LUCK IS ONLY IMPLEMENTED FOR PUTTING *****

A Luck Check is done any time a Player uses one of their "Lucky Bounce" charges (Not available while putting) or whenever a shot is made (When applicable for a putter)

#### Luck Check for Putting
A luck check for putting is done whenever a putt is on line and hit with good power. Hitting core requirements for the other rolls helps decrease the luck requirement. A golfer's Luck attribute will also decrease the Luck requirement. The luck check is set by the following math:

Luck Req = 4 (Base Luck Req) + # of Green Modifiers + (Distance / 3) - (1 * # of core req hit) - (Golfer Luck attribute * 1.5)
