![image](https://github.com/xaspectdevteam/ChatHOOK/assets/141177040/8ebe007a-b9f0-4aa4-a950-cfd5111a588b)

# ChatHOOK Generative AI Architectural Pattern

Conversational AI is hot but boring. When we say “let’s have a conversation,” we don’t necessarily mean “I’ll type some text and you will answer with more text.” Human conversations are first and foremost face-to-face interactions. They're also between a human and a character or between a character and a character. But they're not between text and text.
But what about our conversations with AI chatbots?

Introducing ChatHOOK the next stage in the generative AI wave, and the first platform to enable face-to-face conversations with an “AI Digital Human” in a natural way: 
    
![Xaspect Generative AI Interactive Digital Human Chatbot demo screenshot](https://github.com/xaspectdevteam/ChatHOOK/assets/141177040/d8f40897-769a-44f7-b95d-db683c5a3aef)

Using a “conversational workflow”, users interact via the ChatHOOK UI that offers customizable profiles and filters to create content, then present that content across multi-modal data displays (text, graphics, video and audio).

ChatHOOK is complimentary to the large language models that drive generative AI such as ChatGPT, but will allow users to interact in a more human, engaging and effective way.
Behind ChatHOOK’s AI Digital Human is a neural search engine that uses cross-modal machine learning. 

The three main components of any search engine are the indexer, the query processor, and the ranking algorithm. In a traditional (symbolic) search engine, each of these components would be designed separately using rule-based methods and would require multiple platforms and apps.
However, in the ChatGP neural search engine, all three components are designed into a single platform using deep learning methods.

This approach has several advantages. 

First, it allows for end-to-end training of the system which can lead to better performance overall. 

Second, because all of the components are unified under one framework, it’s easier to share information between them which can also lead to better performance. 

Finally, it makes it possible to use the same framework to build other types of neural search engines (e.g. an image search engine or a video search engine) which can be very helpful in domains where multiple modalities are important.
ChatHOOK Neural Search is not limited to textual data.  It can be used with any type of data, including images, videos, audio, and 3D data. Therefore, ChatHOOK neural search enables the construction of search systems that are more flexible and powerful than traditional symbolic search engines.  ChatHOOK creates a vector representing an image that contains information about the shape, color, and content of the image, which can be used to better match it with other images or document.
 
![image](https://github.com/xaspectdevteam/ChatHOOK/assets/141177040/fa0b0a8f-95c0-43d9-a670-c8e7221690dd)

# ChatHOOK ARCHITECTURAL PATTERN FOR CONTINUOUS INSIGHTS -  Technical Overview

This architecture orchestrates core functions for systems that are making real-time decisions given a multi-modal data
ecosystem. This continuous insights pattern covers common use cases across multiple industry segments such as
Financial Services, Healthcare, Government, Retailing, etc.

Data Sources: A contributing data source may contain information about an individual or organization. A data source
may be a data store (e.g., SQL, NoSQL, NEO4J, MongoDB, HADOOP), a file (e.g., CSV), or a queue containing records.
Loading multi-modal data is handled by submitting all records in the data source to the transform function. After
historical data has been loaded, adds, changes and deletes caused by ongoing business operations are auto-labeled.

Transform: Each data source is programmatically labeled by user-created labeling functions, which capture
labeling rationales and can be applied to vast amounts of unlabeled data and aggregated to auto-label large
training sets. When requirements change, data drifts or new error modes are detected, training sets need to be
relabeled. Recreating all training labels is as simple as adding or modifying a small, targeted number of
labeling functions and re-executing them.

ChatHOOK Generative AI: ChatHOOK ingests the transformed (programmatically labeled records) which may
consist of any type of data, including images, videos, audio, and 3D data. The ChatHOOK indexer, query
processor, proprietary ranking algorithms, and neural search engines (e.g., an image search engine or a video
search engine) are very helpful in use cases where multiple modalities are important. ChatHOOK stores all the
received records via graph tables, in a relational database (e.g., PostreSQL, AWS Aurora, Db2, MySQL). Results from
each graph are posted, in real time, to an Output Queue in ChatHOOK JSON format for consumption (see below).

Analytics, Consume &Visualize: Real-time processes e.g., risk scoring and decisioning systems will read the
Output Queue and direct further action, as desired e.g., responding to an MDM or other source system in real-time.
The Output Queue also keeps other data stores in sync: including NEO4J, Elasticsearch, reservoirs, lakes,
warehouses, marts, etc. The ChatHOOK RestAPI and synchronized data store are called by end user applications
providing such capabilities as user search, graph visualization, enterprise applications e.g., case management,
dashboards, reporting, etc.


# Example Use Case

# Accelerating Catalog Tagging Automation with Xaspect’s ChatHOOK Data-Centric AI Platform: An “X” Success Story (Actual name redacted per request)

One of our missions at “X” is to help our 22 million customers find the products they are looking for. For example, when a customer searches for a “modern yellow sofa” on “X”, we want to show the most relevant options from the tens of thousands of sofas available in our catalog. To do that, it is important to have a strong understanding of the products we sell. We use machine learning algorithms to analyze and understand the descriptive information (e.g. color, shape) of over 40 million products provided by more than 20 thousand suppliers in our catalog.

# What are product tags?

We use product tags to organize and store descriptive information about our products. These tags capture specific attributes of each product, such as its color, design, and pattern, in a structured manner. This allows us to provide targeted search results to our customers. For example, when a customer searches for a "modern yellow sofa," only products that have “color” tagged as “yellow” and “style” tagged as “modern” will be displayed in the search results. Moreover, we use product tags to enhance customer-facing experiences such as personalized recommendations and marketing campaigns.

We currently have more than 10 thousand product tags to describe over 40 million products in the catalog. We store a variety of different tags for each product.  
We use these product tags to power how customers can search and filter products. For example, they may search for “modern yellow sofa”.

We develop machine learning algorithms to extract product tags from images which are available when suppliers upload products to our catalog. With this effort, we aim to obtain comprehensive and accurate information about our products and simplify the product addition process for suppliers while ensuring that customers can easily find what they are looking for and trust what they receive is what they purchased.

# The challenge of manually tagging products

Without Machine Learning, we would have to rely on suppliers or human agents for product information. This information is then used to show relevant products to customers. But there are some challenges with this approach.

First, this manually provided information is:

1.	Inconsistent, where one supplier calls a sofa 'red' while another calls it 'orange’
2.	Inaccurate - dimensions of a chair may be incorrect because the width and height measurements are flipped
3.	Incomplete, with a supplier only providing a basic color name "blue sofa" instead of a more granular color name such as "cerulean sofa"

This means that customers have a less than ideal experience trying to find the right product. For example, a customer may order a chair that doesn't fit their space or can't find the right color they want. Second, asking dozens of questions for each product can be a laborious and time-consuming process for our suppliers.

# Extracting Product Tags from Imagery: Challenges Faced
 
# Visual tags describe products on features like Design, Pattern, or Subject/Theme

Many tags in our catalog describe visual characteristics of products, such as design, pattern, and theme. Examples of design-related tags include "Barrel Chair," "Wingback Chair," and "Curved Sofa." Meanwhile, pattern-related tags include "Chevron Rug," "Striped Curtain," "Floral Accent Pillow,” etc. Examples of theme-related tags include “Outer Space Rug,” “Bird Decorative Object,” etc.

We began by developing a suite of deep learning models trained on “X” imagery that can extract these product tags at scale. However, we have thousands of tags and building models for these tags requires a large amount of labeled data for training and highly curated ground truth data for evaluation. We initially relied on two sources: supplier-provided labels and labels annotated by human agents. However, these sources have their limitations. Supplier-provided labels might be incorrect, or the supplier might not provide tags at all. On the other hand, hand-labeling thousands of tags is time-consuming, difficult to modify with changing taxonomies, and not the best use of human agents' time.

# Limited success with off-the-shelf foundation models

To unblock ourselves from the requirement of a large amount of hand-labeled training data, we then experimented with an off-the-shelf foundation model, CLIP, for zero-shot image retrieval tasks. This worked well for some of the tags such as the subject of a piece of Wall Art (Animal, Nature, etc.), which covers less than 5% of the product tags. But, it did not work for most of the “X” catalog specific tags (e.g. style, design, product types, shape, pattern, season etc.) due to two main reasons. First, the highly confident predictions were still inaccurate. Second, the off-the-shelf model was not able to provide all required tags. We still needed a better way to solve our need for high quality training data and expedite our model development process.

# Enter the “X” & Xaspect computer vision design partnership!
 
Tagging the “subject” of the wall art as “squirrel”: Using off-the-shelf CLIP model, accuracy improved by more than 50 percentage points
 
However, Tagging the pattern of accent chairs as “Chevron”: Off-the-shelf CLIP model cannot distinguish between “Chevron” and “Geometric” very well.

# “X” & Xaspect Computer Vision

Xaspect's main product, the Xaspect ChatHOOK platform, enabled our data scientists to use an iterative process to programmatically label large sets of data leveraging foundation models and weak supervision rather than manually hand-labeling every data point. Xaspect has helped many Fortune 500 companies build NLP models to solve their bespoke business problems. With this partnership, Xaspect expanded on their core data-centric development offering and applied it to computer vision workflows, piloting their new capabilities with our product tagging use case.

# Key Capabilities Utilized:

# - Xaspect’s computer vision workflow for Tagging
 
# - Xaspect’s computer vision workflow for Data preprocessing and iterative model development

We collaborated with the computer vision research team at Xaspect and discussed our challenges with the quality of our training data. During our partnership, we also uncovered additional data quality issues with our dataset such as “duplicate images” and “outlier images - images that are incorrectly associated with products.” The Xaspect team designed a workflow that included: 

1. Data Preprocessing 
2. Iterative Model Development steps to solve these challenges, enabling us to quickly curate vast amounts of training data in minutes instead of the weeks and months required for manual annotation.
 
The “Data Preprocessing and Curation” step ensures the high quality of initial training and evaluation datasets.

1.	Data Cleaning: We encountered quality issues on our data, such as duplicate and outlier images. The Xaspect workflow included deduplication feature that prevents overlapping samples in the training and evaluation dataset and outlier removal step which ensures that datasets only contain relevant images associated with valid products.
2.	Training/Validation data preparation: Preparing training and validation data is critical to ensure the quality of the trained model and we did not have a representative validation set for any given tag. The “validation data preparation” feature in the Xaspect workflow allows for the sampling of a validation set using a combination of uniform, stratified, and similarity-based sampling methods. These samples are then sent to human agents/subject matter experts for labeling. This feature helps create a validation set that has high coverage and diversity, ensuring the quality of the trained model.

“Iterative Development” is the next step that enables us to efficiently label visual data and iteratively build better models. 

The key features include:

1.	Explore and label programmatically: This involves creating labeling functions with prompts (text or images) using pre-trained foundation models. For example, by providing a prompt "Chevron area rugs," we can generate thousands of labels that can be further filtered with human supervision.
2.	Model: Another feature is the denoising model, which helps to clean up the labels generated by combining the labeling functions via label model.  We can then train a model (e.g. "Chevron" or "Not Chevron") using the resulting de-noised labels.
3.	Analyze: This feature enables us to visually analyze the failure modes of the model on the validation data (e.g. “Geometric” pattern mistakenly tagged as “Chevron”) which allows us to iteratively obtain richer training data (e.g. add geometric accent chairs as negative labels) to create better models.
4.	Validation in the loop: Prior to our design partnership with Xaspect, labeling the validation dataset using only human agents (HITL) came with a large amount of upfront effort. This involved preparing training materials, training and managing the human agents, and still, there were quality issues in the validation dataset. Xaspect’s "validation-in-the-loop" feature enables subject matter experts (e.g. Merchants or Category managers) and data scientists to rapidly correct errors or augment the validation dataset as necessary, addressing these challenges.

In this two-step, iterative workflow, we start with “X” specific product images and relevant metadata, and very quickly, we can get the labeled training data as well as models trained on a specific tag (e.g. “Chevron” pattern or not).
 
# Results from the design partnership? Large time savings and accuracy improvements over our baselines.

The results from this design partnership were quite promising. Some highlights include:

1.	Accuracy improvements over our baseline model (using supplier labels): We trained the models on labeled training data using Xaspect’s platform and compared with baseline models trained with supplier-provided labels. We saw consistent improvements on models across design, pattern, shape and theme tags over the supplier baseline. We were able to improve F1 scores by 20 percentage points or more.
2.	Massive time savings over Human-in-the-Loop (HITL) workflows: We compared the time it takes to build and iterate models using a manual labeling workflow vs Xaspect’s iterative approach starting with the same data for one tag (Area rug pattern) and found that we were able to achieve the same or better accuracy 10 times faster by leveraging Xaspect ChatHOOK. These time savings will be compounded as we scale training to thousands of tags allowing us to get models in production in months compared to years it would take with HITL workflows.
3.	Iterative workflows: Tags and searches from customers evolve over time, and updating a model to adjust to these changes is a time consuming and a manual task. With the iterative, data-centric workflow that Xaspect ChatHOOK provides, it becomes easy to add a new tag, or to modify an existing tag, enabling catalog backfills or clean ups at scale in a rapid and cost-effective manner. 

# Results on Chevron pattern tag:
 
# Results for “Chevron Accent Chairs” based on mode? Accuracy improved by more than 20 percentage points

Accurate models enable us to provide more relevant products for customers, so that when they are looking for a “chevron accent chair” or a “yellow modern sofa”, they find just what they need. We are also able to provide this experience sooner compared to using HITL workflows. This translates to better customer satisfaction and potentially increased revenue for the company. We currently leverage labeled data from Xaspect’s platform and train the models in-house. We then deploy them in our orchestration platform built on Google Cloud. In the future, we will launch an A/B test to understand the impact of our models in a customer’s journey.

# Future Xaspect ChatHOOK Releases will:

1.	Leverage new features and capabilities for various use cases. 

a.	Improve Object Detection and Segmentation - In order to get better at extracting information from parts of the product images (for example frame color, upholstery color, arm type, number of products) we are currently exploring object detection and segmentation capabilities.  
b.	Fine-tuning foundation models - While foundation models have certainly shown great promise, they are inherently limited by the data they have been trained on. We would like to fine-tune foundation models with “X” datasets (e.g. text-image pairs) to improve their representations. This should enable us to have even faster model iterations and more accurate models. 
c.	Leveraging generative AI for iterative labeling & model building - One area of future work would be leveraging generative AI models to create synthetic data. With Xaspect ChatHOOK we can use data-centric methods to see where we may have gaps in our training data. For example, if we do not have enough examples of floral accent chairs in our dataset, we can use generative AI to create more training examples. In the future we hope to add generative models in the loop to let us programmatically shore up these weak points.

2.	Introduce No Code/Low code ML development and deployment across “X” - we would like to include Xaspect ChatHOOK in our enterprise MLOps workflows that includes data processing, training/evaluation, deployment, and monitoring across “X” so that subject matter experts and operators can automate tagging with no or minimal code. This will help subject matter experts realize value without the bottleneck of our ML teams’ bandwidth.
