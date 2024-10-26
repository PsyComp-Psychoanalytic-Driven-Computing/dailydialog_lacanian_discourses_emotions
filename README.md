# DailyDialog - Lacanian Discourses and Emotions Dataset

## Description
This dataset contains annotated dialogues from diverse conversation scenarios. It aims to explore the relationships between emotions and discourse types, drawing from Lacanian discourse theory as well as empirical analysis of conversational patterns. The dataset includes annotations for different types of emotions and Lacanian discourses detected within the dialogues.

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset Details](#dataset-details)
3. [Research Background](#research-background)
4. [Data Format](#data-format)
7. [License](#license)
8. [References](#references)

### Introduction
This dataset is the result of an interdisciplinary research effort combining psychoanalysis and computer science. Specifically, it aims to bridge the concepts of Lacanian discourses with empirical emotion detection in natural language processing (NLP).

### Dataset Details
- **Total Dialogs**: 40
- **Total Dialog Parts**: 276
- **Annotations**:  
  - **Emotions**: Each dialogue part includes one or more emotion annotations, based on the set of emotions used in the [GoEmotions dataset](https://github.com/google-research/google-research/tree/master/goemotions). To complete the set of emotions for this work, two additional emotions, “anguish” and “anxiety”, were added, as they are highly referenced in psychoanalytic literature. The full list of emotions can be found in the file emotions.txt
  - **Discourses**: Dialogue parts are also categorized into one or more Lacanian Discourses and each annotation includes a confidence score.

### Research Background
The dataset originates from research combining psychoanalysis and computer science to analyze how emotions are expressed within the framework of Lacanian discourses. Lacanian theory identifies various social roles that people assume in discourse, namely the "Master," the "Hysteric," the "Analyst," the "University," and the "Capitalist." These roles, or discourses, provide a model to examine the underlying dynamics of conversation, allowing for a deeper understanding of motivations, emotions, and power structures.

The goal of this research is to identify patterns in emotional expression within these discourses, potentially making the automated identification of discourses more accessible and nuanced. Such automated methods can contribute to interactive systems in areas like mental health diagnostics and detection of misinformation.

### Data Format
The dataset is provided in JSON format. Each entry contains:  
- **Dialog ID**: A unique identifier for each dialogue.
- **Dialog Parts**: Each part includes:  
  - **Text**: The actual dialogue text.
  - **Emotions**: A list of detected emotions with associated confidence scores.
  - **Discourses**: A list of Lacanian discourses present, along with their respective confidence scores.

**Example Format**:  
```json
{
    "AnnApptExc__5": {
        "dialog_part_0": {
            "dialog_text": "I am not convinced by your explanation. Could you explain it?",
            "emotions": [
                {"emotion": "curiosity", "confidence_score": 0.778},
                {"emotion": "disappointment", "confidence_score": 0.444},
                {"emotion": "confusion", "confidence_score": 0.333}
            ],
            "discourses": [
                {"discourse_name": "Analyst", "confidence_score": "High"},
                {"discourse_name": "Hysteric", "confidence_score": "High"}
            ]
        }
    }
}
```
## License
All datasets in this repository are released under the [CC BY 4.0 International license](https://creativecommons.org/licenses/by/4.0/legalcode).
This license permits unrestricted use, distribution, and adaptation of the dataset, provided appropriate credit is given to the original source.

## References
- Gadalla, M., Nikoletseas, S., & Amazonas, J. R. A. (2024). *Combining Psychoanalysis and Computer Science: An Empirical Study of the Relationship Between Emotions and Lacanian Discourses*. [TBC].

