---
layout: meetup
title:  "State Department Cleantech Challenge - Code for San Francisco"
date:   2017-06-06
type: meetup
meetup: 
---

The Data Science Working Group (DSWG) of Code for San Francisco (C4SF) participated in a _"Data Science Challenge"_ the  weekend of March 31 - April 2, sponsored by the US Department of State and Booz Allen Hamilton (BAH) at the Galvanize campus in San Francisco.

Our team consisted of *eight* members of the members of the DSWG: Catherine Zhang, Jude Calvillo, Anna Kiefer, Juliana Vislova, Cherie Meyer, Peter Welte, Tyler Field, Eric Youngson (myself) and one person from the San Francisco department of Environment, Imma Regina Dela Cruz.
   
All in all, this was a great experience; we made lot's of great connections and learned a lot. As events go a data science challenge are pretty new. Basically a _hackathon_ where, hopefully, raw data is turned into insights. Given the novelty of this new type of event there was some confusion over what the final product should be and what the role of data science is in the software development process. The tools are similar but the goals are somewhat different. In software development the end result is usually an application, typically a web-application. For a data scientist, the end result--or at least the goal--is usually some kind of predictive model.

The stated "Desired Outcomes of Solution" were as follows.

  - Open source, user-friendly data science applications, 
    algorithms and/or tools that allow users to identify 
    where to build small-scale solar and micro-grids in     
    Burma.
  - The solution must have great data visualization and 
    be accessible to non-technical users
  - The underlying approach to the tool or application 
    should be scalable, and may be applied to other        
    countries and data sets

As with most data-driven projects, a big part of the challenge was in defining the problem to be solved and determining if the data we were provided was sufficient to solve the problem or more sources needed to be identified.

An additional challenge was that, although the criteria were clear enough, there were many subtleties to the problem that only came out through discussions with subject matter experts (SME) and during the demo presentation, where we presented our preliminary solution to the problem and elicited feedback from a panel comprised of the organizers and SMEs. For example, we assumed that we could rely on the government's electrification plan to exclude areas where they were already planning to invest from recommendation to the private sector.

For data we were provided access to BAH's "Sailfish" platform. Ultimately we explored several datasets found there but the available data were not sufficient for our analytical approach. The dataset we found most useful, the 2014[?] census--the first in thirty years, we found on the open web.

One aspect of this event that was conspicuously absent was any mention of the oppressed Rohingya minority, a group of about 9 million people, which was notably absent from the census data.

The challenge opened with a Happy Hour Friday night with opening remarks by Brian MacCarthy of BAH and a recording by Ambassador U Aung Lynn.

Over the course of the next day and a half we discussed our ideas with subject matter experts (SME) and presented our proposed solution to the problem, as we had come to define it, to a panel of SME, officials from the US State Department and employees of BAH. In addtion to government officials from both the US & Myanmar, several for & non-profit companies were included in the SME panel.

  - BBOXX
  - Intersect
  - Infrastructure Development Company Limited

We were provided the data in the form of access to a special subdomain of BAH's Sailfish platform put together specifically for this event. Unfortunately we weren't granted access until Thursday, just the day before the opening happy hour. We made do with the circumstances, though, given the presentations started Sunday just after lunch.

First we started with a classic brainstorming session; locked ourselves in a conference room and set a time limit to start assigning responsibilities.

We identified (4) directions for exploration to inform our model.

  1. Predict need for access to electricity
  2. Predict  willingness to pay for private investment
  3. Identify renewable energy resource potential
  4. Design user interaction

After talking individually with the SMEs and presenting to the panel, we realized that the energy resources are fairly evenly distributed throughout the countryside, however identifying households having all the indicators for enticing private investment are difficult to identify for a number of reasons.

The following census features as a household rate per township were selected by the team, in coordination with the panel, as available indicators of willingness to pay.

  - Demand for electricity (mobile phone use as proxy for 
    consumer demand)
  - Employment status
  - Housing type & ownership status
  - Likelihood of being connected to the grid
  - Current energy use: lighting used as proxy

First we decided to eliminate the areas identified by the central government's planned grid development but we were told by the panel that we couldn't quite rely on the national electrification plan and would need alternative indicators.

The main data-sets we relied on to determine the intersection of these attributes that would indicate conditions favorable to private investment were the national census data and the geo-spatial location of existing power lines.

We set to work exploring a predictive model for willingness to pay based on existing indicators in the census data such as the cost of lighting alternatives, assuming that they would prefer electric lighting as it is safer than most of the available alternatives.

Simultaneously we worked on mapping the distance from existing power lines that would contain enough townships to correlate to the current reported overall grid electrification for the country.

Future work remains to validate the predictive model using multiple years' data and integrating the predictive scoring into the GIS visualization to create an interactive tool for guiding investment and quantifying it's potential impact and revenue for investors.

Next Steps:
  1. Rigorously explore variables in Census
  2. Form a hypothesis for the ideal data that would 
     provide prediction of interest & potential to pay
