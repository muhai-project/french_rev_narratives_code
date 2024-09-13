# Narrative Prototype - The French Revolution

# Acknowledgement: 
The work reported in this paper was funded by the [European MUHAI project](https://muhai.org) from the  Horizon 2020 research and innovation  programme under grant number 951846 and the Sony Computer Science Laboratories Paris.
This work is also the result of a joint collaboration between the following partners in the project: [Sony CSL Paris](https://csl.sony.fr/project/building-narratives-computationally-from-knowledge-graphs/) & [Vrije Universiteit Amsterdam](https://krr.cs.vu.nl)
# Application domain: 
Graphs, Semantic web. 
# Citation: 
```
@article{blin2022building,
  title={Building a French Revolution Narrative from Wikidata},
  author={Blin, In{\`e}s},
  year={2022}
}
```
# Code of Conduct: 
# Code repository: 
git@github.com:muhai-project/french_rev_narratives_code.git
# Contact: 
Inès Blin
# Contribution guidelines: 
# Contributors: 
Inès Blin
# Creation date: 
24-05-2022
# Description: 
This projects aims to be a first prototype on narrative exploration. In particular, the focus of the study is the French Revolution. The idea is to explore events and participants throughout structured ([Wikidata](https://www.wikidata.org)) and unstructured ([Wikipedia](https://www.wikipedia.org)) data. Structured data can help better grasp the main entities, objects or events, while unstructured data like text can help make hypotheses on how events are linked.
# DockerFile: 
# Documentation: 
# Download URL: 
# DOI: 
# Executable examples: 
# FAQ: 
# Forks count: 
1
# Forks url: 
https://github.com/SonyCSLParis/building-fr-narrative-from-wikidata-1/tree/main
# Full name: 
Inès Blin
# Full title: 
French Revolution Narrative
# Images: 
# Installation instructions: 
If using https, run:
```python
git clone https://github.com/muhai-project/french_rev_narratives_code.git 
cd building-fr-narrative-from-wikidata
```

If using ssh, run:
```python
git clone git@github.com:muhai-project/french_rev_narratives_code.git
cd building-fr-narrative-from-wikidata
```

In the `settings` folder, create a `private.py`file and add the following paramters:
* ROOT_PATH: root path to the project directory
* AGENT: your user agent that you can find on the web.


Version of Python used: 3.9.4

Create a virtual env and activate it (example below with conda)
```bash
conda create -n <yourenvname> python=3.9.4
conda activate <yourenvname>
```

```bash
pip install -r requirements.txt
```
Then run the following:
```bash
python setup.py install
```
# Invocation: 
To run the streamlit app
```bash
cd app-demo && streamlit run app.py
```
# Issue tracker: 
Later when launching the app, you might encounter the following error:
```bash
ImportError: pycurl: libcurl link-time ssl backends (secure-transport, openssl) do not include compile-time ssl backend (none/other)
```

To prevent this error, and following [this link](https://stackoverflow.com/questions/21096436/ssl-backend-error-when-using-openssl), you can run the followings:
```bash
pip uninstall pycurl
export PYCURL_SSL_LIBRARY=openssl
pip install pycurl --no-cache-dir
```
# Keywords: 
# License: 
GPL 3.0
# Logo: 
# Name: 
french_rev_narratives_code
# Ontologies: 
# Owner: 
Inès Blin
# Owner type: 
User
# Package distribution: 
# Programming languages: 
Python
# Related papers: 
Building a French Revolution Narrative from Wikidata
# Releases (GitHub only): 
# Repository Status: 
Inactive
# Requirements: 
Cf. requirements.txt
# Support: 
# Stargazers count: 
2
# Scripts: Snippets of code contained in the repository
- [app-demo](./app-demo)

  Streamlit web application to collect data and build networks.

- [graph_building](./graph_building)

  Module to build networks using networkx or pyvis.

- [settings](./settings)

- [kb_sparql](./kb_sparql) 
  
  Using a SPARQL wrapper to query wikidata, as well as the knowledge graph created throughout the process.

- [wikipedia_narrative](./wikipedia_narrative)

    Used for the pilot: mapping Wikidata/Wikipedia, extracting infoboxes and text from Wikipedia
# Support channels: 
# Usage examples: 
# Workflows: 
