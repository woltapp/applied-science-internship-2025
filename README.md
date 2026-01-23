# Applied Science Summer Intern Assignment 2026

## Assignment for candidates

This is a mandatory assignment for everyone applying for the Applied Science Internship. Please return your answers along with your application.

This assignment is exclusively for the Applied Science internship position.

## Table of Contents

1. [Overview](#overview)  
2. [Choosing the data](#choosing-the-data)  
3. [Choosing a modeling approach](#choosing-a-modeling-approach)  
4. [Working with the data](#working-with-the-data)  
5. [Submitting the assignment](#submitting-the-assignment)

---

## Overview

Thank you for applying for Wolt's 2026 Applied Science Internship\! The purpose of this assignment is to understand how you think, how you approach applied machine learning problems, and how you reason about solutions in a real product and production context.

This is not a research assignment, and we are not looking for perfect models.

We care more about:

- clear problem framing  
- reasonable assumptions  
- well-justified modeling choices  
- awareness of limitations and production concerns

Simple, well-explained solutions are absolutely fine.

You need to submit three things:

1. Presentation (PDF format)  
   - Exactly 8 slides, including the title slide  
   - Must follow the mandatory presentation structure below  
   - No additional slides or appendix  
2. Code used in the assignment, in a reproducible and open format  
   - Jupyter notebooks and/or Python scripts are fine  
   - Include a README.md explaining how to run your code  
   - Include a list of dependencies (for example requirements.txt)  
3. Your CV, plus optional attachments describing your studies, projects, or work experience

Good communication is a key part of success in this role.

We use the presentation as the primary screening tool, and decide based on it which assignments will be reviewed at code level in more detail. Based on this review, we will invite candidates to a technical interview followed by a final interview.

### Mandatory presentation structure

Your presentation must follow the structure below. We evaluate submissions slide by slide based on how clearly and thoughtfully you address these questions.

1. Title slide  
     
   - Your name  
   - Contact information

   

2. Problem and decision context  
     
   - What is the problem you are solving?  
   - Who uses the output of this model?  
   - What decision-making or business process does it support?  
   - Why is this problem relevant?

   

3. Data and EDA findings  
     
   - What data did you use?  
   - Key insights or findings from exploratory data analysis?  
   - Anything surprising or important for modeling?

   

4. Feature engineering and representations  
     
   - What signals did you create from the data?  
   - What did you choose not to use, and why?

   

5. Modeling approach and assumptions  
     
   - What modeling approach did you choose?  
   - What assumptions does your approach make?

   

6. Results and evaluation  
     
   - How did you evaluate the model?  
   - What metrics did you use?  
   - How good are the results for the intended use?

   

7. Limitations  
     
   - Known limitations of your approach?  
   - When would this break in a production setting?

   

8. Next steps  
     
   - If this were deployed to production, what would you do next to improve it?

## Choosing the data

We have prepared two datasets for you. Feel free to choose which data you use based on your background and ambitions. **You only need to choose one.**

### Order flow dataset

Consider the simulated flow of orders in Helsinki over 3 months in the [provided file](orders_spring_2022.csv). The dataset contains the following columns:

- order\_placed\_at\_utc: time when the order was placed in UTC  
- item\_count: number of items in the order  
- order\_category: reporting category of the order  
- actual\_delivery\_time\_minutes: actual delivery time from order placement to completion in minutes  
- estimated\_delivery\_time\_lower\_minutes: lower estimate of delivery time before the order was placed  
- estimated\_delivery\_time\_upper\_minutes: upper estimate of delivery time before the order was placed  
- venue\_location\_h3\_index: h3 geospatial index of the venue  
- customer\_location\_h3\_index: h3 geospatial index of the customer  
- courier\_supply\_index: measure of available courier supply at the time of the order placement  
- precipitation: forecasted hourly precipitation at the time of the order placement

Tip: you can refer to the [h3 documentation](https://h3geo.org/) to investigate the h3 indexes.

### Item sales dataset

Consider the daily items sales history in the [provided file](grocery_sales_autumn_2025.csv). The dataset represents simulated daily grocery sales from a number of venues in Finland, and contains the following columns:

- venue\_id: venue identifier  
- sku\_id: SKU (Stock Keeping Unit), i.e. internal product and variant identifier  
- phl1\_id, phl2\_id, phl3\_id: PHL (Product Hierarchy Level) identifiers. Each SKU belongs to a PHL3, which in turn belongs to a PHL2, which belongs to a PHL1. These represent product categories of increasing genericity.  
- country\_id: venue country identifier  
- price: unit price in EUR  
- promo\_flag: whether a promotion is active for the given SKU on a given date  
- promo\_depth: depth (as a percentage) of the promotion  
- operating\_minutes: operating minutes of the venue on the given date  
- in\_stock\_minutes: how many minutes the SKU was in stock in the given venue on the given date  
- stockout\_flag: a binary flag indicating whether the SKU ran out of stock  
- units\_sold: units of the SKU sold in the given venue on the given date

## Choosing a modeling approach

Using your chosen dataset, define a modeling task that is relevant to Wolt.

To give you an idea what we are looking for, the task might look something like these:

- Can we estimate the delivery time of an order?  
- Where will orders be delivered in the near future?  
- Based on past data, can we forecast item sales for tomorrow, next week, or later?

Your task must result in some form of predictive model. You may train one or multiple models.

Your modeling approach should follow naturally from the decision context you define. Model choice without a clear link to how the output is used will be evaluated poorly.

A simple model with strong reasoning is preferred over a complex model with weak justification.

## Working with the data

### Exploration

- Produce meaningful statistics and visualizations  
- Focus on insights that influence modeling choices or decisions  
- Exhaustive analysis is not required

### Feature engineering

- Explain what features you created and why  
- Explicitly discuss what you chose not to use

### Modeling

- Describe your approach and its benefits  
- Clearly state assumptions  
- Explain why this approach makes sense for the problem

### Evaluation

- Describe how you evaluated the model  
- Discuss what kinds of errors matter most  
- Consider how useful the model would be in practice

### Limitations

- Discuss known limitations and failure modes

---

## Submitting the assignment

Bundle everything into a ZIP archive and upload it to Google Drive, Dropbox, or a similar service. Include the download link in your application.

### Important notes

- Do not store your solution in a public GitHub repository  
- Do not share your solution publicly in any form  
- Make sure file permissions allow us to access the materials

A good check before sending your task is to unzip the Zip archive into a new folder and check that building and running the project works, using the steps you define in readme.md. Forgotten dependencies and instructions can sometimes happen even to the best of us. If we cannot access or run your submission, we unfortunately cannot review it.  
