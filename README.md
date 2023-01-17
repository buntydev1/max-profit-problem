# water-tank-problem

Find all the combinations of unit possible by ensuring the total construction time is LESS than the Time Unit given. 

The approach to find the combinations is as below:

a) Take a single type of unit (Possible Types: Theatre, Pub, Commercial park) and make other unit types as zero.
b) Take two unit types together and exhaust/permute across all the possible combinations with the third unit type as zero.
c) Finally Permute across all the three unit types. 

d) Once all the combinations are available, calculate the total earnings by using the below formula: 
[(Time unit - construction end time) * number of units * rent for each T establishment] +  [(End Time - construction time) * number of units * rent for each P establishment] +  [(End Time - construction time) * number of units * rent for each C establishment]=  total earnings

e) Sort the results from the above caluclations and select combination giving out the maximum earning value. 

for example take 24 units 
	c0t0p5,c0t4p0,c2t0p0 - permuting on single type of unit
	c0t1p4,c0t2p3,c0t3p2,c1t2p0,c1t0p0 - permuting on two unit
	c1t1p2                             - permuting on three unit

now using all combinations , calculate total using formula mentioned in d
