Project description
Topsis
for: Project-1 (UCS654) submitted by: Chaitanya Roll no: 102103615 Group: 3CO22

Topsis-Chaitanya-102103615 is a Python library for dealing with Multiple Criteria Decision Making(MCDM) problems by using Technique for Order of Preference by Similarity to Ideal Solution(TOPSIS).

Installation
Use the package manager pip to install topsis.

pip install Topsis-Chaitanya-102103615
Usage
Enter csv filename followed by .csv extentsion, then enter the weights vector with vector values separated by commas, followed by the impacts vector with comma separated signs (+,-), and followed by path of the output csv file.

Topsis sample.csv "1,1,1,1" "+,-,+,+" output.csv or vectors can be entered without " "

Topsis sample.csv 1,1,1,1 +,-,+,+ output.csv

But the second representation does not provide for inadvertent spaces between vector values. So, if the input string contains spaces, make sure to enclose it between double quotes (" ").

To view usage help, use

topsis /h

Example
sample.csv
A csv file showing data for different mobile handsets having varying features.

Model	Storage (in gb)	Camera (in MP)	Price (in $)	Looks (out of 5)
M1	16	12	250	5
M2	16	8	200	3
M3	32	16	300	4
M4	32	8	275	4
M5	16	16	225	2
weights vector = [ 0.25 , 0.25 , 0.25 , 0.25 ]

impacts vector = [ + , + , - , + ]

input:
Topsis sample.csv "0.25,0.25,0.25,0.25" "+,+,-,+" output.csv

output:
  TOPSIS RESULTS
Model	Storage (in gb)	Camera (in MP)	Price (in $)	Looks (out of 5)	P-Score	Rank
M1	16	12	250	5	0.534277	3
M2	16	8	200	3	0.308368	5
M3	32	16	300	4	0.691632	1
M4	32	8	275	4	0.534737	2
M5	16	16	225	2	0.401046	4
Other notes
The first column and first row are removed by the library before processing, in attempt to remove indices and headers. So make sure the csv follows the format as shown in sample.csv. All the categorical column are encoded to numerical values for processing.

License
MIT
