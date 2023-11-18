# Stats, Clubs, Swings, and Distances. How the Fuck does this work?!

This will be a working document on how the stats, clubs, swings, and distances are done. This will provide the basic structure for the math and code that follows.

## Stats
#### Power: Main influence in determining distance. 
 - Roll >= Power req.
#### Technique: Main influence in determining contact with the ball.
 - Low req <= Roll <= High req
#### Control: Main influence in determining control over ball flight.
 - Low req <= Roll <= High req
#### Finesse: Main influence in determining ball spin + kick
 - Low req <= Roll <= High req
#### Luck: Influences kick + lucky saving throws. Main influence in determining hole outs / close putts.

## Clubs
Every club has it's own features for roll requirements as well as how a golfer's stats affect the swing. Each category of club (Driver, Fairway Wood, Iron, Wedge, Putter) will have different ways stats affect a swing result as well as within each category of club. The table below outlines all of the clubs currently in the game as well as the roll requirements and modifiers for each.

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
		<td> Control / Finesse </td>
		<td> Finesse </td>
	</tr>
	<tr>
		<td> Fairway Woods </td>
		<td> Power / Technique </td>
		<td> Control / Finesse </td>
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
		<td> Technique </td>
		<td> Power / Control / Finesse </td>
		<td> Power / Control / Finesse </td>
	</tr>
</table>

----------------------
<table>
	<tr>
		<th> Club Brand </th>
		<th> Club Type </th>
		<th> Power Req </th>
		<th> Technique Req </th>
		<th> Control Req </th>
		<th> Finesse Req </th>
		<th> Max Carry Distance </th>
		<th> Max Rollout Distance </th>
		<th> Club modifiers </th>
	</tr>
	<tr>
		<td> Rental </td>
		<td> Driver (D20) </td>
		<td> 15 </td>
		<td> 8-11 </td>
		<td> 8-11 </td>
		<td> 6-13 </td>
		<td> 230 </td>
		<td> 20 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> 3 Wood </td>
		<td> 15 </td>
		<td> 8-11 </td>
		<td> 8-11 </td>
		<td> 7-12 </td>
		<td> 200 </td>
		<td> 15 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> 6 Iron </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> 180 </td>
		<td> 6 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> 7 Iron </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> 160 </td>
		<td> 5 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> 8 Iron </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> 145 </td>
		<td> 4 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> 9 Iron </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> 130 </td>
		<td> 4 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> Pitching Wedge </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> 115 </td>
		<td> 3 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> Sand Wedge </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> 90 </td>
		<td> 2 </td>
		<td> None </td>
	</tr>
	<tr>
		<td> Rental </td>
		<td> Putter </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
		<td> TBD </td>
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

