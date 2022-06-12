# Matching Prefixes
### Requirements :
* accept perfixes as configuration
* write unit tests
* explore other than linear scan
* preprocess the list of prfixes
* demonstrate the use of goroutines

---

## Ideas Explored and developed
### Idea 1: RunV1
RunV1 accepts input from user in std console input and uses 2 functions to evaluate the longest prefix.
In this approach we use a **linear search using a list**
* buildPrefixList builds the prefixList from config file mentioned in env
* longestPrefixV1 has main logic to get the longest prefix from prefixList with the input fed to it



### Idea 2: RunV2
RunV1 accepts input from user in std console input and uses 2 functions to evaluate the longest prefix.
In this approach we make use of **map of lists**
* buildPrefixMap builds the prefixMap from config file mentioned in env
* longestPrefixV2 has main logic to get the longest prefix from prefixMap with the input fed to it.



### Idea 3: RunV3
RunV1 accepts input from user in std console input and uses 2 functions to evaluate the longest prefix.
This approach is same as v1 but **we make use of go routines** just to showcase on the usecase.
* buildPrefixListV3 builds the prefixList from config file mentioned in env
* longestPrefixV3 has main logic to get the longest prefix from prefixList with the input fed to it


---
## Project structure
This Project layout tries to gain inspiration from standard Go project layout as demostrated here : https://github.com/golang-standards/project-layout

---

## Unit Tests

All unit tests were run successfully and even benchmarking were performed on actual logic

--- 
## Develpoment environment

Development was done adn tested in a windows machine and Visual studio editor was used for the development.

---
## Test and Build 
* **Batch file testAndBuild.bat** was used for automating testing and build process.

* Makefile was also made available just in case if needed.
  Use command make build/test/all accordingly.
---
## Deploy :
The binary is generated in deploy folder on running of the build script as mentioned above. 
Program expects user to have filled a environment variable "CONFIG_FILE" with path and filename of the prefix list config file and defaults to vaule "sample_prefixes_(3).txt". It accepts input from user and gives the longest matching prefix from the prefix list fed as config. 