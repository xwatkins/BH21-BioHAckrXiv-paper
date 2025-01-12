---
title: 'Integration of visualisation tools for disease mechanisms and their annotations: UniProt, Nightingale and the MINERVA Platform'
title_short: 'Integration of UniProt, Nightingale and Disease Maps'
tags:
  - visualisation
  - protein databases
  - UniProt
  - Nightingale
  - Disease Maps
authors:
  - name: Thijs van Beek
    orcid: 0000-0002-8283-7204
    affiliation: 1
  - name: David Hoksza
    orcid: 0000-0003-4679-0557
    affiliation: 2
  - name: Piotr Gawron
    orcid: 0000-0002-9328-8052
    affiliation: 1
  - name: Marek Ostaszewski
    affiliation: 1
    orcid: 0000-0003-1473-370X
  - name: Xavier Watkins
    orcid: 0000-0001-9327-5887
    affiliation: 3
affiliations:
  - name: LCSB, University of Luxembourg, Luxembourg
    index: 1
  - name: Charles University, Prague, Czech Republic
    index: 2
  - name: European Bioinformatics Institute, Canbridge, UK
    index: 3
date: 11 November 2021
bibliography: paper.bib
event: lamola2021
biohackathon_name: "BioHackathon Europe"
biohackathon_url:   "https://biohackathon-europe.org"
biohackathon_location: "La Mola, Spain 2021"
group: Project 13
authors_short: Thijs van Beek \emph{et al.}
---

# Introduction

Research on human diseases often involves their molecular mechanisms, in an attempt to explain genetic risk factors, identify affected molecular pathways or propose plausible drugs. Number of bioinformatic resources catalog and encode different facets of this information. We need to combine these resources efficiently, and equip the researchers with visualisation tools to make the process of exploring and combining knowledge faster and more informative.

Our work focuses on visualisation of protein level annotations, from gene/protein annotation, 
protein-protein interaction, pathways and genomic variation. We integrate i) protein-level annotations of UniProt (https://uniprot.org) with an embedded browser of Disease Maps (disease-maps.org) and ii) the protein residue level information with Disease Maps ([Nightingale library](https://ebi-webcomponents.github.io/nightingale/#/)).

We demonstrate the overall setup with both visualisation workflows on the COVID-19 Disease Map.
In particular, the list of UniProt entries related to COVID-19 can be shown side-by-side with the Map, allowing simultaneous exploration of both resources. Moreover, a dedicated plugin showing protein structures in the Map gives detailed view into the structure of all annotated proteins.

# Results

## An interface between UniProt and Disease Maps

UniProt is a widely recognised protein knowledge base, offering curated information about protein structure and function. Recently, UniProt started to develop disease-centric resources, like Alzheimer’s disease portal and COVID-19 platform (https://diseases.uniprot.org, https://covid-19.uniprot.org). These portals list and organise information about proteins related to a particular disease. 

In turn, Disease Maps (disease-maps.org) provide a standardised, diagrammatic way to encode mechanisms of human diseases (https://biohackrxiv.org/gmbjv/), with COVID-19 as a prime example (https://fairdomhub.org/projects/190). Disease Maps are manually curated and rely on web-based platforms to explore them [@mazein_systems_2018]. One of them is the MINERVA Platform [@gawron_minerva-platform_2016], offering a range of exploration and visualisation functionalities. One of these functionalities is the recently developed widget (https://gitlab.lcsb.uni.lu/minerva/widget) allowing easy embedding of MINERVA-hosted maps into other websites.

We combined these two resources by extending the newly developed UniProt website (https://beta.uniprot.org) to embed the widget for the [COVID-19 Disease Map](https://covid19map.elixir-luxembourg.org/minerva/index.xhtml?id=covid19_map_BH21_v1). This way a dedicated COVID-19 collection of UniProt (https://covid-19.uniprot.org) is flanked by the diagrams of the Map.

![UniProt (beta) embedding the COVID-19 Disease Map via MINERVA widget \label{fig_nmp}](./unpb_mnvw.gif)

The content of two resources is matched based on their UniProt identifiers. After harmonisation, 51 of identifiers (only human proteins) of the UniProt colection are missing in the map. The reason for this difference is that the curators of the Map diagrams did not find sufficient evidence for concrete molecular interactions linking these proteins to particular pathways. This can be resolved in subsequent steps by curation of the Map supported by bioinformatic workflows like text mining and network analysis [@ostaszewski_covid19map_2021].

## A Nightingale plugin in the MINERVA Platform

We used the Nightingale library (https://ebi-webcomponents.github.io/nightingale/#/), a suite of standardised modular data visualisation components, 
including the protein feature annotation viewer ProtVista, a protein interaction visualisation and a 3D viewer Mol* (https://molstar.org). [...]

We defined standards for the data exchange for Nightingale components, to make them easily usable by other ELIXIR resources.

![A Nightingale plugin in the MINERVA Platform \label{fig_nmp}](./nghtgl_mnv_plg.png)


# Conclusions


