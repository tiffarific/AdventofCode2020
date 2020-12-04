Sequence:
Read the puzzle
Get the data into Notepad++ for data wrangling
See below for Notepad++ steps
Paste data into Excel
????
Profit!!!!


Notepad++ used to work on the data two times
1. get all the data on one line per Credential
2. separate the height unit from the number


1. To get all the data on one line per Credential:
Replace all occurances of two newlines ("\r\n\r\n") with something unique (used "****")
Replace all occurances of two newlines with nothing
Replace all occurances of "****" with a single newline with a space before (" \r\n") it (the space for uniformity, helps with a different formula)
Done


Example
Original Data:

iyr:2013 hcl:#ceb3a1
hgt:151cm eyr:2030
byr:1943 ecl:grn

eyr:1988
iyr:2015 ecl:gry
hgt:153in pid:173cm
hcl:0c6261 byr:1966

hcl:#733820
hgt:166cm eyr:2025 pid:79215921 byr:1952 iyr:2014 ecl:blu

eyr:2022
hgt:165cm hcl:#733820
iyr:2013 pid:073015801 ecl:oth
cid:101


Transformed Data:
iyr:2013 ecl:brn hcl:#623a2f cid:246 byr:1948 pid:122719649 hgt:160cm eyr:2026 
iyr:2012 hcl:#b6652a hgt:160cm pid:223041037 eyr:2029 byr:1920 ecl:oth cid:212 
pid:166619054 cid:125 hcl:#cfa07d hgt:164cm byr:1946 ecl:brn iyr:2014 eyr:2023 


2. To separate the unit from the number
replace all occurances of "cm" with "\tcm" (tab cm)
replace all occurances of "in" with "\tin" (tab in)
