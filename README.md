# Machine Learning Engineer Nanodegree
## Capstone Proposal
Mehdi Khodayari
November 6th, 2017

## Proposal
In this project a labeled dataset (set of images collected from the Sentinel-1 satellite and labeled manually) is used to train a binary classification model which can predict if there is iceberg(s) in new observations or not.

### Domain Background
The Sentinel-1 satellite sends a signal to an object and collect the echo referred to as backscatter which is then converted to an image. The backscatters from any solid objects such as ship, iceberg, and land is stronger than that from water, making it possible to distinguish between solid objects from water. In fact, solid objects in the resultant images appear brighter than their surrounding (water).
The emitted signals from the satellite always hit the objects horizontally, but the backscatters are received either horizontally or vertically. Hence, two sets of information (images) are obtained from objects; the first set here is referred to as HH (transmit/receive horizontally) which corresponds to the horizontal backscatters and the second set is HV (transmit horizontally and receive vertically) which corresponds to the vertical backscatters.

In this section, provide brief details on the background information of the domain from which the project is proposed. Historical information relevant to the project should be included. It should be clear how or why a problem in the domain can or should be solved. Related academic research should be appropriately cited in this section, including why that research is relevant. Additionally, a discussion of your personal motivation for investigating a particular problem in the domain is encouraged but not required.

### Problem Statement
This is a binary classification project and the challenge is to predict the label of every image as 1 (if there is iceberg(s) in the image) or 0 (if the detected objects corresponds only to Ship(s)).

### Datasets and Inputs
This project is an ongoing [kaggle competition](https://www.kaggle.com/c/statoil-iceberg-classifier-challenge#background) (at the time of this proposal submission) and the data is given in json format. There are train and test datasets. The datasets have the following fields:

  1. id: the image id
  2. band_1, band_2: the flattened image data corresponding to HH and HV respectively each with 5625 elements (75x75 pixels)
  3. inc_angle: the incident angles of which the image was taken
  4. is_iceberg: the train dataset labels which is either 1 (if there is iceberg(s) in the image) or 0 (if the detected objects corresponds only to Ship(s))

The band_1 and band_2 fields have dB unit. The is_iceberg field only exists in the train dataset.

### Solution Statement
![alt text](https://github.com/mekhod/iceberg_ship/tree/master/images/img_1.png)

### Benchmark Model
_(approximately 1-2 paragraphs)_

In this section, provide the details for a benchmark model or result that relates to the domain, problem statement, and intended solution. Ideally, the benchmark model or result contextualizes existing methods or known information in the domain and problem given, which could then be objectively compared to the solution. Describe how the benchmark model or result is measurable (can be measured by some metric and clearly observed) with thorough detail.

### Evaluation Metrics
_(approx. 1-2 paragraphs)_

In this section, propose at least one evaluation metric that can be used to quantify the performance of both the benchmark model and the solution model. The evaluation metric(s) you propose should be appropriate given the context of the data, the problem statement, and the intended solution. Describe how the evaluation metric(s) are derived and provide an example of their mathematical representations (if applicable). Complex evaluation metrics should be clearly defined and quantifiable (can be expressed in mathematical or logical terms).

### Project Design
_(approx. 1 page)_

In this final section, summarize a theoretical workflow for approaching a solution given the problem. Provide thorough discussion for what strategies you may consider employing, what analysis of the data might be required before being used, or which algorithms will be considered for your implementation. The workflow and discussion that you provide should align with the qualities of the previous sections. Additionally, you are encouraged to include small visualizations, pseudocode, or diagrams to aid in describing the project design, but it is not required. The discussion should clearly outline your intended workflow of the capstone project.

-----------

**Before submitting your proposal, ask yourself. . .**

- Does the proposal you have written follow a well-organized structure similar to that of the project template?
- Is each section (particularly **Solution Statement** and **Project Design**) written in a clear, concise and specific fashion? Are there any ambiguous terms or phrases that need clarification?
- Would the intended audience of your project be able to understand your proposal?
- Have you properly proofread your proposal to assure there are minimal grammatical and spelling mistakes?
- Are all the resources used for this project correctly cited and referenced?
