# Converting NBA2k20 Dataset into RDFLib and Visualizing with Graphviz and SPARQL.

by Ikhsan Assidiqie

### Table of Contents

- Introduction
- Dataset
- Conversion to RDFLib
- Visualizing with Graphviz
- SPARQL Queries
    - ASK Query
    - DESCRIBE Query
    - Aggregate Query
    - Nested SPARQL Query
    - Federated Query
- Conclusion

## Introduction

This documentation outlines the process of converting the NBA2k20 dataset into RDF using the RDFLib Python library.
Additionally, we will use Graphviz to visualize the generated RDF graph. The documentation also provides examples of
SPARQL queries on the converted RDF dataset, which includes ASK query, DESCRIBE query, aggregates query, nested SPARQL
query, and federated query.

## Dataset

The NBA2k20 dataset is a collection of player statistics and attributes from the NBA2k20 basketball video game. It
contains information such as player names, teams, positions, ratings, and various game-related attributes.

Source: https://www.kaggle.com/datasets/isaienkov/nba2k20-player-dataset

## Conversion to RDFLib

To convert the NBA2k20 dataset into RDF format, we will use RDFLib, a popular Python library for working with RDF data.
We will create RDF triples representing players, their attributes, and relationships between them.

#### Helpful Libraries

In order to use `rdflib` library, we need to install the library from `!pip install rdflib`

- `from rdflib import Graph, Namespace, Literal`
- `from rdflib.namespace import RDF, RDFS, XSD`

The above code creates an RDF graph representing players and games from the NBA2k20 dataset and saves it to a file in
Turtle format.

## Visualizing with Graphviz

To visualize the RDF graph, we can use Graphviz, a graph visualization software.

1. Install Graphviz from [Graphviz Site](https://graphviz.org/download/)
2. Convert the RDF file to DOT format: Use a Python script to convert the Turtle file to the DOT format compatible with
   Graphviz.

And then, you need to install graphviz library with command in pip:

- `!pip install pygraphviz`

Next, you need to import it using this command: `import pygraphviz as pgv`

3. Generate the visualization: Open a terminal/command prompt and run the following command to generate a PNG image from
   the DOT file.

- `dot -Tpng nba2k20_dataset.dot -o nba2k20_dataset.png`

# Progress

1. Download `dataset` from kaggle.
2. Convert data from tabular format into graph/ rdf format
3. Add graph/ rdf data into RDFLib
4. Visualize the rdf data in your RDFLib using _graphviz_
5. Query the graph/ rdf data using SPARQL inside your RDFLib.
   - ASK Query
   - DESCRIBE Query
   - AGGREGATE Query
   - NESTED SPARQL Query
   - Federated Query
6. Visualize result every SPARQL Query
7. Dump RDF data/ graph from RDFLib into .ttl format
8. Merge code files and `.ttl` into the same folder and renamed into `StudentId-FinalProject`.