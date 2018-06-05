# Expiry List
## Requirements:
### The supermarket has two rules:
1. Expired items must be removed
2. Items that have been on the shelf for more than **N** weeks must be removed

#### Items can have 4 states:
1. **new** - the item has arrived this week
```
001: *****Cheese***** 12-JUN-2017 ****New**** [0 checks]
```
2. **valid** - the item is not expired and has been on the shelf for LESS than **N** weeks
```
001: *****Cheese***** 12-JUN-2017 ***Valid*** [1 check ]
```
3. **old** - the item is not expired but has been on the shelf for MORE than **N** weeks
```
001: *****Salad***** 20-JUN-2017 *****Old***** [2 checks]
```
4. **expired** - the item has expired (the date is older than the current week date)
```
020: *****Nutella***** 24-MAY-2017 *****Expired***** [0 checks]
```
Each week **M** new products arrive. The progam must be start from the current date plus **K** days and run for **X** weeks
Each weekly list must be printed after a duration of **R** seconds
(**N,M,K,X,R** should be configurable by the supermarket manager and should have meaningful variable names)

#### Bonus
- use a config object to store all the manager settings 
- make the duration **R** a random number between MIN and MAX set by the manager
- use colors in the console log printout
- accept a date format in the config object (user defined) and format the dates accordingly. Don't use moment.js

#### Documentation
- Add a detailed readme.md file describing your project.
- Generate a JSDoc documentation for your code and put it in a folder called /JSDoc

#### Important
- Variables must have meaningful names
- The code is well documented
- The code is well indented
- The data structures must be effective and the code must be efficient
- You need to be able to explain each line of your code
- Your output should match the sample outputs provided

Example of print:
| ID | ITEM NAME | DATE OF LOAD | STATE |NUMBER OF CHECK|
|----| ----------|--------------|-------|---------------|
```
001: *****Cheese***** 12-JUN-2017 ****New**** [0 checks]
```
```
002:       Meat       29-MAY-2017     New     [0 checks]
```
```
002: .....Nutella.... 13-JUN-2017 ....New.... [0 checks]
```
```
002: ||||||Rice|||||| 19-JUN-2017 ||||New|||| [0 checks]
```

---

## Items
Each item have:
1. a unique ID
2. a name
3. an expiration date
4. any other properties that you think are needed

- The ID is unique!
- The ID is a zero padded number e.g. 01 or 001 (should be configurable)
- The names is randomly generated from a given set
- The expiry dates is randomly generated between the start and finish date of the weekly runs
- All the names and states is padded to have the same length
- The padding character MUST be configurable
- The date is exactly formatted e.g 03-JUN-2017
- In general the printout to the console should always be aligned properly

---

## Resources

[Github](https://github.com/)
[W3school](https://www.w3schools.com/)
[Dillinger](https://dillinger.io/)

-------------------------------------------------------------------------------------------------------------

## Coding
Example of colored text in console:
```js
console.log('%c the green hulk got mad!', 'color: green; font-weight: bold;');
```
Example of object manager settings
```js
var settings = {
    userName:"",
    password:"",
    firstSetting:"",
    secondSetting:"",
};
```

---
## Installation

Guide to installation

---
## Contribute

- Issue Tracker: github.com/$project/$project/issues
- Source Code: github.com/$project/$project

---
## Support
|ROLE     |FIRST NAME | LAST NAME | CONTACT                             |
|---------| ----------|-----------|-------------------------------------|
|Chief    |Marius     |Cozma      |marius.cozma@edu.itspiemonte.it      |
|Developer|Leandro    |Allemandi  |leandro.allemandi@edu.itspiemonte.it |
|Developer|Gabriela   |Andrei     |gabriela.andrei@edu.itspiemonte.it   |
|Developer|Andrea     |Tallone    |andrea.tallone@edu.itspiemonte.it    |

---
## License
The project is licensed under the ITS-ITC Foundation.
Piazza Dei Mestieri 2
Via Jacopo Durandi 10
10100 Turin (To) Italy

Contact:
Tel: +39 011 0371500
P.IVA 10600860018
C.F. 97734430016
Numero REA TO – 1147027
Registro PG Pref. di Torino nr. 731
PEC its-ictpiemonte@pec.it
