# weather-app
This is primarily a repository for holding my various experiments in accessing restful API's and eventually my experiments of creating and hosting API endpoints. All code written here should be written by me(ie. there will be no "copypasta" from other repositories, documentation, or generative AI). 
Additionally I am aiming to create multiple versions of the same program to help familiarize myself with various languages. 
## Functions
The functionality will be split between two different use cases. There will be an assumption of following best practices, so there should be no hardcoded keys, global declarations where not neded/etc. However encryption at rest will be out of scope/assumed to be addressed by another tool. 
### Data Collector
1. To read an existing API endpoint at open-meteo. The given program should:
    * Load secrets from an environmental file, or if I get one stood up in time a local vault
    * Pull weather data for my location. Optional, prompt for collection of secondary location. 
    * split the data into multiple different data types. (optimally using at least one of each type for a given language. Ie. sets/tuples/dictionaries/etc)
    * save the modified data into an SQLite file. 
    * repeat collection by a defined amount in .env file.
### REST Endpoint
2. Hosting an API Endpoint (unauthenticated v1 and authenticated v2). It should:
    * Pull data from the SQLite file. 
    * Return data based off location and date range
    * Format the data in JSON
    * handle relevant error states (ie. 404, etc)
### (OPTIONAL) Front-End
3. Create a web front-end that pulls the data from the endpoint(s) and then renders the data in a graph. In a realworld scenario I would probably just do the data rendering in an application like Grafana. 
## Languages
Each individual section can be written in whichever language. I'll be splitting each folder respectively per language to keep the structure clean. Where possible priority should be given to the following as some of the most commonly used languages in my field:
1. Python
2. Golang
3. NodeJS
4. Rust
## Attribution, Security, Feedback, and Comments
This repository is meant primarily to be a solo project and so I probably won't be accepting PR's. You are welcome to clone/fork/etc. If you have feedback or a report to make please contact me at contact@chaos-cat.page. 