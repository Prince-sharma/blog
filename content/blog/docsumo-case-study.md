+++
author = "Hugo Authors"
title = "DocSumo Case Study"
date = "2024-12-26"
description = "A product statergy assignment I did for DocSumo"
tags = [
    "product",
    "statergy",
]
+++
# Docsumo: Analysis of Intelligent document processing market and strategic recommendations

## Market and Competitor analysis

### Market

IDP automates the handling of documents including data capture, document classification, data extraction, validation and Integration for companies who rely heavily on processing documents to make business decisions

1. **Regional banks** depend on processing documents for processing loans, updating customer information (beneficiary, ) and many other workflows

   1. Example documents: Bank Statements, Tax Returns, Financial Statements, Business Licenses, Collateral Documents

2. **Insurance Companies (**National Life Group, Employers Insurance) depend on document processing to process insurance claims and also issue insurance

   1. Property deed, home inspections reports, etc

3. **Alternative Lenders (**OnDeck Capital, Kabbage, BlueVine, Fundbox, Celtic Bank, etc) depend on processing customer bank statements, etc

4. **Equipment Finance** (TimePayment, Ascentium Capital) companies depend on document processing for evaluating loan parameters

5. Healthcare Organizations, Legal Firms, Manufacturers, Government Agencies also process high volume of complex documents to run their business processes


### Competitors

1. Ideal customer profile and their requirements (excluding large enterprise customers)

   1. Let’s consider a mid-size US commercial lender (500-1,000 employees), processing 200-500 loan applications monthly with legacy software that requires significant manual data entry, leading to delays and errors

   2. Their focus is on reducing manual processing time to minimize lost deals, improving accuracy to cut error-related losses, enhancing customer experience with faster processing, ensuring compliance, and achieving ROI through better staff efficiency

   3. Hence the key factors for solution evaluation criteria include data accuracy, processing speed, document versatility, seamless integration, security compliance, cost-effectiveness, vendor reliability, and ease of training and use

2. Sources:

   1. Competitor website, product walkthrough in case the product is accessible with signup, Youtube and publicly accessible blogs with demos of the platform

   2. G2 and gartner websites with recent customer reviews and feature comparisons

![table of competitor study](https://raw.githubusercontent.com/Prince-sharma/prince-sharma/gh-pages/assets/images/competetior-study.png)

Key differentiators and competitive advantage of DocSumo

1. Best in class UX for document processing and review

2. Bridges the gap between traditional document processing tools (Abbyy, Kofax) and innovative AI-first competitors

3. Combines LLMs assisted OCR with deep industry-specific ML models for financial sector

Strategic positioning plan to capture more of the mid-market segment

1. P0: Strengthen the document AI standing on the financial and lending business by improving accuracy for new unstructured document and integrations to seamlessly integrate into the workflow

   1. Reduce the time for first document data extraction with high accuracy for any uploaded document type using LLM assisted document processing, prebuilt workflows for major use cases, etc

   2. Build native integration for customers to easily integrate into any workflows, allowing input and export of data into various platforms. Integrate systems used by financial and lending companies to allows support in the end to end lifecycle of document processing

2. P1: Build robust workflow builder with semantic understanding and vertical specific solutions to move up the value chain

   1. Eg. Fraud detection for the uploaded documents

      1. Since the financial company is dependent on Docsumo to get the data extracted from the customer document, flagging fraudulent document can be competitive advantage

3. P2: Expand into other similar sectors and go deep based on adoption and customer feedback


### What would your 3-month, 6-month, and 12-month product vision look like?

**Features / capabilities we should prioritize to align with Docsumo's mission**

1. Traditional OCR systems primarily rely on pattern recognition and template matching to convert images of text into machine-readable formats, LLMs improve upon these shortcomings by leveraging their ability to understand context and semantics. Unlike traditional OCR, LLMs interpret text meaning, fixing errors and ensuring better accuracy

2. LLM-assisted OCR has greatly improved the accuracy of processing unstructured documents, even with minimal training. However, the market response varies:

   1. **Established players** like Abby and Kofax have strong enterprise business workflow integrations but are slow to adopt LLM-assisted OCR

   2. **Newer competitors** like Hyperscience and Instabase focus on LLM-first products but struggle with product depth required for enterprises and high-scale document processing (source: [G2 reviews](https://www.g2.com/products/hyperscience/reviews#reviews))

3. LLM tools by themselves cannot solve enterprise use cases. Docsumo holds a unique competitive advantage by balancing both extremes. It offers highly accurate models for document classification and data extraction, tailored for financial services and commercial lending. Additionally, it provides seamless enterprise workflow integration and use-case-specific product optimizations for various document types

![Roadmap Table](https://raw.githubusercontent.com/Prince-sharma/prince-sharma/gh-pages/assets/images/roadmap-3-6-12-months.png)



### Which features or capabilities would you prioritize to align with Docsumo's mission?

Milestones for all features described below:

1. Implement a beta version in solutions mode and use existing documents to confirm accuracy improvements

2. Data analysis based on current customers data and cohorts ton  decide going deep into the feature based on feedback

3. Work with friendly customer to get feedback 

![Features Metrics Table](https://raw.githubusercontent.com/Prince-sharma/prince-sharma/gh-pages/assets/images/features-metrics.png)

### How will you balance short-term wins with long-term product scalability?

1. Clearly define success criteria and milestones for each short-term feature to measure progress effectively

2. Label early-stage features as "Beta" to set clear expectations with customers 

3. Continuously invest in platform stability, ensuring sophisticated AI & ML at scale remains a competitive advantage

4. Establish long-term scalability targets linked to enterprise customer onboarding and allocate a dedicated swimlane for scalability improvements in every release


### Which specific use cases will you prioritize (e.g., customer onboarding, claims processing) to demonstrate immediate value?

1. Ideal Customer Profile for DocSumo: Mid-market financial services, commercial lending, and B2B technology companies who rely heavily on document-intensive processes, manual data entry, and challenges with scalability and accuracy in data extraction and using legacy systems or semi-automated workflows seeking AI-based solutions to modernize operations

2. Prioritized Use Cases to Demonstrate Immediate Value

   1. Oneshot document processing for existing document work flows to reduce the dependency of uploading 10 documents and minimise the time to set up workflow for new customers


### What success metrics would you track to gauge the impact of newly launched features?

_Included in the Roadmap section on each feature level_


### How would you drive feature adoption among customers?

1. Targeted customer education

   1. Release notes

   2. Guides on how to use the feature

   3. Webinars and blog posts with Industry specific examples for the new features

   4. In product nudges

2. Onboarding strategies

   1. New feature walkthrough / demo for existing active customers


### How would you approach the go-to-market strategy for new integrations?

The integrations are for Google Drive, Box, Dropbox, S3, SharePoint, and OneDrive for imports; Google Sheets and Smartsheet for exports.

1. Product led

   1. In-product Nudges, predefined workflows with specific use case examples that use the integrations for export and import of the data

   2. Add import and export options for the current document types

2. Use case driven marketing

   1. Create blogs, guides, release notes, etc for specific use cases targeted to tech financial companies

   2. Create SEO-optimized landing pages for each integration, highlighting specific use cases (e.g., "Import financial documents from Dropbox for instant analysis")

   3. Run targeted campaigns (paid ads, email marketing) emphasizing how these integrations solve customer pain points

   4. Conduct webinars on training of various use cases for financial sectors like automated loan processing, income verifications, etc

3. Partner led

   1. Joint marketing and GTM for larger platform native integrations like salesforce, Pega and other 

   2. Ensure integrations are published in respective app marketplaces (e.g., Google Workspace Marketplace, Microsoft AppSource, Dropbox Extensions) - low priority 


### How would you integrate user feedback into the product lifecycle, specifically for the new integrations?

1. Discovery Phase:

   1. Talk to customers to identify integration needs and expected workflows, evaluate complexity to implement, reach, expected impact on the north star metric

   2. Analyze competitor integrations for common user pain points and opportunities

2. Design Phase:

   1. Share mockups or prototypes with beta users for early feedback on usability

   2. To Incorporate feedback iteratively into designs before development

3. Development Phase:

   1. Use feature flags to deploy integrations incrementally to a small user base

   2. Include events to track usage across funnel and error patterns during internal testing

4. Launch Phase:

   1. Run a beta program with power users to validate functionality and gather real-world insights

   2. Enable surveys to collect immediate post-launch feedback, when a user adds their first x integration


### What mechanisms will you use to gather feedback and iterate on the feature post-launch?

1. Contextual surveys at key touchpoints (e.g., after a file import/export)

2. Persistent "Submit Feedback" button near integration features / at the end of setting up a workflow

3. Monitor analytics (adoption rate, success rate, error rate) alongside user feedback

4. Use feedback loops (release notes, emails) to inform users of updates based on their input

5. Actively monitor feedback via support channels for any issues, enhancements, etc


## References

1. Publically available demo for the platforms on their website, youtube, etc

2. G2 and gartner to understand how customers evaluate different products

3. Example customer case study: <https://instabase.com/cases/how-axa-increases-capacity-of-underwriters-with-instabase/> 

4. OCR comparison (pre-LLM) 3 years ago: [Link](https://www.youtube.com/watch?v=5sMVA9GHziU) comparing a few tools

5. LLM assisted OCR models have vastly improved the accuracy of image OCR \[[Github](https://github.com/Dicklesworthstone/llm_aided_ocr?tab=readme-ov-file)] \[[hackernews](https://news.ycombinator.com/item?id=41203306)]

6. Different IDP companies in the market: <https://app.meticulate.ai/company_search/f9724bbc-d50b-4a99-90a1-7b041192fbd4> 

7. Financial sector document AI companies: <https://app.meticulate.ai/company_search/85119b29-d2be-4067-8583-a7a8359b5811> 


## Assumptions and appendix

1. Competitor analysis is done keeping mid market customers in mind where we have different team who can try the solution and take decision independently

   1. Enterprises can have a vastly different evaluation criteria where they issue tenders and solution providers then submit proposal, etc and have much larger closing cycles

2. I have not talked to actual customers and hence would want to validate hypothesis presented in this doc and get more insights into their needs and end to end workflows before implementing

3. Risks / challenges of using LLMs

   1. When using a hybrid LLM and OCR systems, Issues such as error diagnosis in hybrid systems—determining whether an error arose from the OCR or the LLM—pose significant hurdles


### Other strategic opportunities emerging due to LLMs

1.  Ability of LLMs to understand context and semantics for a given document file of any format opens up new use cases and markets. One of the key advantages of LLMs is their capability to interpret the meaning behind the text they process. LLMs can discern context and correct typographical errors based on surrounding information

2. Vertical solutions lending companies, to add rules and business context for their process approvals into their IDP systems, suggest decision in addition to the correct texts

3. Other companies building vertical end to end process management softwares

   1. [Extend](https://www.extend.app/): AI Agents for Unstructured Data

   2. [CommodityAI](https://www.commodityai.io/): AI-Powered Shipment Management for Commodity Traders

   3. [Lucite](https://www.lucite.ai/): Automating workflows for insurance, real estate, and finance.

   4. [PropRise](https://www.proprise.io/#features): Automating commercial real estate data collection
