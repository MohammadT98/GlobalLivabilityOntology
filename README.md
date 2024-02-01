# Global Livability Ontology
Welcome to the Global Living Conditions Data Project! This repository is a comprehensive effort to gather, organize, and integrate information from 29 distinct datasets, each shedding light on different aspects that impact the living conditions across countries worldwide. Using the power of the Semantic Web, our goal is to build a detailed, linked set of data. This data can help us analyze, compare, and understand different factors that play into the quality of life in various places.

## Overview
The Global Living Conditions Data Project covers a lot of ground. We look at things like the economy, education, freedom, happiness, health, natural disasters, and much more. This gives us a full picture of what life is like in different corners of the world. By putting this information into an RDF format and setting up an ontology to define how all these pieces relate to each other, we open the door to deep dives and comparisons that can reveal important insights about life quality. What sets this project apart from others is our extensive use of Semantic Web technologies, which not only enables the integration of a wide variety of data but also allows for more complex queries and insights than traditional datasets. This approach facilitates a more nuanced understanding of global living conditions, providing a unique tool for researchers, policymakers, and the curious public.

Here's what you'll find in this repository:

- **Accessibility**
- **Conflict and Peace**
- **Economic Conditions**
- **Education Levels**
- **Levels of Freedom**
- **Friendliness**
- **Overall Happiness**
- **Work Culture**
- **Natural Disasters**
- **Beauty Perceptions**
- **Population Details**
- **Religious Beliefs**
- **Travel Tips and Warnings**

## Structure
The project is structured as follows:

- **Datasets/**: Contains the raw CSV files used to populate the RDF graph.

- **PopulatedData/**: Contains the Turtle (.ttl) files that represent the serialized RDF graph, one for each aspect of global livability.

## Technical Requirements
To engage with the Global Livability Ontology, a basic understanding of Semantic Web technologies is beneficial. Familiarity with SPARQL for querying RDF data and experience with RDF libraries in programming languages such as Python can greatly enhance your ability to explore and analyze the data. Tools like Protégé for ontology editing for are also useful. Furthermore, incorporating GraphDB as part of the technical stack can provide a robust platform for managing, storing, and querying the ontology data. 

## Getting Started

To explore the Global Livability Ontology, clone this repository and browse through the PopulatedData directory to access the Turtle files. You can use RDF tools and SPARQL endpoints to query and analyze the data.

## Ontology
In the development of our ontology, we carefully created 14 unique classes, along with one additional class specifically designed to hold detailed information about countries, such as their names and languages spoken. To fill these classes with meaningful data, we conducted a thorough search, identifying and combining 29 datasets that match the various attributes of each class in a way that makes logical sense.

![](Images/OntologyModel.png)

To link these classes together, we implemented a single object property, 'belongsToCountry,' which connects all the individual classes to the main Country class. This creates a well-organized and interconnected web of data. Additionally, for certain classes where it was relevant, we created subclasses to further categorize the data. These subclasses allow for the automatic sorting of instances into more specific groups based on the criteria we set. This method enhances the detail and precision of our ontology, enabling more sophisticated analysis and insights.

## Data Cleaning and Preparation
**Convert Countries to ISO 3166-1 Alpha-2 Codes**

As part of our data preparation process, we convert country names of all datasets to their corresponding ISO 3166-1 alpha-2 codes using the pycountry library. This standardization facilitates consistency across datasets and enhances the reliability of our data integration efforts.

**Checking for Consistency**

Our data cleaning process includes checks for consistency and completeness, ensuring that all country values across tables exist in the Country class. This step is crucial for maintaining the integrity of our datasets.

**Handling Multiple Values and Trimming**

We identify countries with multiple entries within the same dataset and resolve these discrepancies to ensure data accuracy. Additionally, we trim strings to remove any leading or trailing spaces, further standardizing our data.

**Merge DataFrames**

We also merge various datasets to enrich the information available for each country. This process involves aligning data based on country attributes and ensuring that our final datasets are comprehensive and cohesive.

## Populating the Data
The process of populating the RDF graph involves meticulously mapping and integrating data from each of our datasets into a coherent semantic structure. This involves creating RDF triples that link entities with their attributes and relationships according to our ontology. The populated data in the RDF graph is then serialized into Turtle format, making it ready for analysis. This structured approach allows us to capture the complexity of global living conditions in a format that is both rich in detail and flexible for querying.

<img src="./Images/ClassHierarchy.png" width=400 height=400>
<img src="./Images/Class%20Relationships.png" width=400 height=400>

## Serialization
A key aspect of our project is the serialization of our integrated datasets into Turtle (.ttl) format. Turtle provides a more readable format for RDF data, making it easier for humans to understand and machines to process. This step is crucial for ensuring that our data is accessible and usable, allowing for the complex querying and analysis that sets our project apart.

## Queries


## Datasets Used
Below are links to the datasets utilized in this project:

https://www.kaggle.com/datasets/adityakishor1/all-countries-details

https://www.kaggle.com/datasets/nelgiriyewithana/countries-of-the-world-2023

https://worldpopulationreview.com/country-rankings/best-healthcare-in-the-world

https://worldpopulationreview.com/country-rankings/countries-without-mcdonalds

https://worldpopulationreview.com/country-rankings/internet-speeds-by-country

https://worldpopulationreview.com/country-rankings/countries-with-most-beautiful-women

https://worldpopulationreview.com/country-rankings/countries-with-the-most-handsome-men

https://www.kaggle.com/datasets/ramjasmaurya/conflicts-among-nations

https://worldpopulationreview.com/country-rankings/most-peaceful-countries

https://www.kaggle.com/datasets/abhijitdahatonde/worldwide-average-iq-levels

https://worldpopulationreview.com/country-rankings/countries-that-censor-the-internet

https://worldpopulationreview.com/country-rankings/countries-where-alcohol-is-illegal

https://worldpopulationreview.com/country-rankings/countries-where-abortion-is-illegal

https://worldpopulationreview.com/country-rankings/gender-equality-by-country

https://worldpopulationreview.com/country-rankings/countries-where-burqa-is-mandatory

https://worldpopulationreview.com/country-rankings/countries-with-mandatory-military-service

https://worldpopulationreview.com/country-rankings/lgbt-rights-by-country

https://worldpopulationreview.com/country-rankings/friendliest-countries

https://worldpopulationreview.com/country-rankings/least-racist-countries

https://worldpopulationreview.com/country-rankings/most-homophobic-countries

https://www.kaggle.com/datasets/jahaidulislam/world-happiness-report-2005-2021

https://worldpopulationreview.com/country-rankings/countries-with-the-most-holidays

https://worldpopulationreview.com/country-rankings/most-overworked-countries

https://worldpopulationreview.com/country-rankings/hardest-working-countries

https://www.emdat.be/

https://www.kaggle.com/datasets/abdurrakibmollah/religious-populations-across-the-world

https://worldpopulationreview.com/country-rankings/least-religious-countries

https://worldpopulationreview.com/country-rankings/most-visited-countries

https://worldpopulationreview.com/country-rankings/worst-countries-to-visit

