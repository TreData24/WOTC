# Whos Streets Our Streets
Combining Named Entity Recognition (NER) and Natural Language Processing (NLP)  techniques to identify properties owned or managed by entities named in the class action lawsuit  against RealPage, Inc in Washington DC. The final project allows users to input their DC address and building names and get an output telling them whether their address is owned by any of the  fourteen Real Estate conglomerates mentioned in the lawsuit.

# Final Product:
Property Ownership Classification Application
Input: Property address or building name.
Model: Bert model “dbmdz/bert-large-cased-finetuned-conll03-english”
Output: The building [BUILDING NAME] is located at [FULL ADDRESS] and is owned by [DEFENDANT].

# Problem Statement: 
Washington DC is among the most expensive cities to live in in the world. Rents and mortgages 
alike have skyrocketed within DC as of the past few years. This is not a natural occurrence of 
supply and demand but rather a concerted effort by real estate conglomerates and other special 
interest groups. The issue of transparency becomes very relevant when discussing housing 
security and fair pricing. The primary problem that we seek to address within this project is how 
much of the city of the district of Colombia is owned by any of the fourteen landlords included in 
November 1st, 2023, antitrust lawsuit against RealPage. 
How can we empower DC residents with transparency regarding their rental prices and who literally owns their streets? 

# Background and Significance:
In October 2022, Hausfeld LLP, Berger Montague PC, Lieff Cabraser Heimann & Bernstein, 
LLP, and Justice Catalyst Law, filed a federal antitrust class action against RealPage, Inc. and 
several of it’s property management clients. Since this class action suit, many other states have 
begun to follow, beginning their own cases against RealPage and its affiliates. As of November 
1, 2023, the District of Columbia filed a antitrust lawsuit against RealPage, Inc. and fourteen of 
the largest landlords in the District alleging violations of the D.C. Antitrust Act. As a labor 
analyst at the Department of Employment Services, issues related to the wellbeing of the citizens 
of Washington DC are an integral part of my work. Topics such as housing have a direct 
correlation with employment and unemployment statistics which are foundational to my daily 
analysis. As such I hope to leverage a deep learning model to help Washingtonians achieve more 
transparency in their own housing pursuits and rental agreements.

# Deep Learning Application:
This project uses BERT (Bidirectional Encoder Representations from Transformers) for Named Entity Recognition (NER) to identify and classify entities like addresses, building names, and defendant names from user inputs.

Why BERT?
Handles real-world text variations (e.g., "1st Street" vs. "First Street")
Contextual understanding from both left and right of tokens
Fine-tuned for token classification tasks

Role in the Project:
Detects entities in user input (address/building name)
Maps input to database entries of defendant properties
Returns ownership information accurately

# Workflow
1. Requirement Analysis: Users input address/building name → Output ownership info.
2. Data Gathering:
   - Initial attempt: Legal documents via MyTax.DC.gov
   - Pivot: Web scraping rental websites of defendants for property listings.
3. Environment Setup:
   - Libraries: pandas, transformers, torch
4. Data Preparation:
   - Load scrubbed data from Excel into pandas DataFrames
   - Normalize text (ordinals, special characters, lowercase)
5. Model Integration:
   - Load pre-trained BERT model for NER
   - Extract entities from user input
6. Matching Logic:
   - Compare input against defendants’ property database
   - Return ownership details
7. Testing & Debugging:
   - Ensure accuracy and robustness
   - Document code for clarity

# Tech Stack
- Language: Python
- Libraries: transformers, torch, pandas
- Model: dbmdz/bert-large-cased-finetuned-conll03-english
- Data Source: Web-scraped property listings from defendants’

# Work Cited:
1. DCist. "DC Attorney General Sues Landlords Over Rent Practices." DCist, 
dcist.com/story/23/11/01/dc-attorney-general-lawsuit-landlords-realpage/rent.
2. MyTax.DC.gov.
3. Office of the Attorney General for the District of Columbia. "Attorney General Schwalb 
Sues RealPage Residential." District of Columbia, www.oag.dc.gov/release/attorneygeneral-schwalb-sues-realpage-residential.
4. Open Data DC. Open Data DC, opendata.dc.gov/.
5. https://www.avaloncommunities.com/district-of-columbia/
6. https://bellpartnersinc.com/properties/bell-capitol-hill
7. https://www.bozzuto.com/apartments-for-rent/dc/
8. https://www.camdenliving.com/apartments/washington-dc/
9. https://www.equityapartments.com/washington-dc/
10. https://www.gables.com/community/528461
11. https://www.highmarkres.com/maryland/dc
12. https://www.jbgsmith.com/property/residential/
13. https://livecapitolrose.com/
14. https://www.maac.com/district-of-columbia/washington-dc/post-massachusetts-avenue/
15. https://www.meridiangalleryplace.com/?switch_cls[id]=97281
16. https://www.parktriangleapts.com/?switch_cls[id]=97281
17. https://wcsmith.com/apartments/
18. https://www.udrive.com/washington-dc-apartments/
