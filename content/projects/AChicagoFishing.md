+++
date = '2026-02-13T21:55:02-06:00'
draft = false
title = 'Chicago Fishing Anglers - Palantir Foundry'
+++

*February 2026 - Present*

### Background
Growing up in Rochester, NY, surrounded by Lake Ontario and the Erie Canal, fishing has always been my favorite hobby. After moving to Chicago, with the Chicago River and Lake Michigan just steps away, I wanted to bring that same curiosity into a technical space.

I built Chicago Fishing Anglers as a data platform in Palantir Foundry to model the freshwater fishing ecosystem in Chicago. My goal was to create a data-driven dashboard that helps anglers determine:
- The best locations to catch specific fish species
- Optimal bait and rig types
- Seasonal timing patterns
- Who has successfully caught similar species and could share advice

This project blends geospatial analytics, ontology modeling, AI agents, and user-driven data writeback — all built around something I genuinely care about.

### What I did
#### Generated Realistic, Notional Datasets
Using AI-assisted data generation, I created structured datasets modeling:

1. Fish Species Data
- Native Chicago freshwater species
- Average length and weight
2. Fisherman Data
- Username
- Display name
- Contact email
3. Catch Records
- Fisherman username
- Timestamp of catch
- Species caught
- Length and weight
- Geolocation (accurately mapped to the Chicago River, lakefront, and ponds)
- Bait type and rig type

This allowed me to simulate a realistic Chicago fishing ecosystem before layering analytics on top.

#### Built Data Pipelines + Ontology
Using Pipeline Builder, I:
- Cleaned and validated all datasets
- Standardized schema relationships
- Created primary/foreign keys for later mapping
![pipeline builder](12.png)

#### Using Ontology Manager, I:
- Created 3 object types: Fisherman, Catch, and Species
- Defined relationships/links between objects and added properties for later usage
- Created Actions to allow for data writeback feature
- Structured the ontology to represent Chicago’s fishing ecosystem

This created a semantic layer that allowed AI agents and dashboards to reason over structured fishing data.

#### Built Interactive Workshop Dashboard
Using Palantir Workshop, I created a dynamic Chicago map visualizing historical catch locations where users can filter for:
- Fish species
- Bait type
- Rig type

This allows users to explore which combinations of bait and rig type have historically performed best for specific fish species. Furthermore, I designed an AIP Agent named, “Rod”.

Using AIP Agent Studio, I built an AI agent named Rod that allows users to:
- Ask where to catch specific fish species
- Request bait or rig recommendations
- Identify anglers who have successfully caught a certain species
- Receive contextual, data-driven responses grounded in ontology data

This moves the dashboard from static visualization to conversational intelligence.

![Chicago fishing dashboard](13.png)
![Rod chat agent](14.png)
![Rod chat agent response](15.png)

#### Implemented Data Writeback
I created a form-based action where users can select the “Report your Catch” button to submit their own catch data.
Users enter:
- Their username + contact information
- The species of fish they caught
- Timestamp of when they caught the fish
- Catch length + weight
- Click on the Chicago map to enter the geolocation of their catch
- Specify bait + rig type

The form appends records directly to the ontology, continuously enriching the dataset and improving downstream recommendations.

| | | 
|---|---|
| ![Report your Catch button](16.png) | ![Action form](17.png) |

### What I Want to Continue Building
1. “Rodett” – Geospatial Recommendation Agent

I am currently developing a second AIP agent, Rodette, that will:
Automatically generate geoshapes on the Chicago map to highlight statistically optimal catch zones for specific species. I also would like Rodett to dynamically adjust recommendations based on seasonality and bait selection

![Rodett](18.png)

2. Predictive Modeling Layer

I would like future enhancements to include:
- Logistic regression or gradient models predicting probability of species catch by:
- Water temperature
- Time of year
- Bait + rig type

3. Seasonality Intelligence

I want to incorporate:
- Water temperature ranges
- Species spawning windows
- Seasonal migration patterns

4. Community Features

I want to incorporate:
- Angler profiles with catch history
- Performance metrics
- Social knowledge sharing for tips and tricks 
