3. Student Grievance Redressal System
The Problem

Student grievances are usually written as unstructured text, which makes manually sorting them into categories time-consuming. I wanted to build a system that could automatically classify a grievance into its relevant category.

The Data

I worked with a labeled grievance-text dataset. The exact original source and dataset details aren't documented in my current project records, so I don't claim a specific source.

The Approach

I built a text-classification pipeline using:

Grievance text → TF-IDF → Logistic Regression → Predicted category

TF-IDF converts the text into numerical features that the classifier can use, while Logistic Regression predicts the appropriate predefined grievance category.

Results

The project achieved approximately 86% accuracy on the project evaluation.

What I Built

The result was a working classification demo where a user could enter grievance text and receive a predicted category.

It was not deployed at my university or used to route real grievances, so I present it as a proof of concept rather than claiming real-world impact.

What I Learned

This project gave me practical experience working with unstructured text and showed me how relatively simple NLP techniques can turn raw text into something that can be automatically classified.
