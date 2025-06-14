# Prompt-Analyser
# Prompt Analyser

## Overview
The Prompt Analyser project aims to explore the nuances of prompt engineering by analyzing how different prompt phrasing strategies affect the quality, length, and clarity of responses. This project utilizes a dataset of prompts and responses to visualize and understand the relationships between prompt characteristics and response outcomes.

The following project has been evaluated by the following metrics mentioned below.

## Features
- **Prompt Type Distribution**: Visualizes the distribution of different types of prompts in the dataset.
- **Length-Based Features**: Analyzes and displays the length of prompts across varying prompt stucture evaluations, to help determine how prompt structure impacts llm responses.
- **Sentiment Analysis**: Analyses the nuances in prompting and the impact of delivery from responses can be measured by polarity and subjectivity to evaluate how LLM's respond in a particular tone for different prompt types.
- **Semantic Similarity**: Analyses how similar responses are when comparing different prompt variants. 



## Insights

> **Prompt Type influences response length and structure**

 - **Commands** produced the longest and most stuctured responses, reflecting that clarity and structure of prompt is essential for an LLM to correctly evaluate a users request and generate the result accordingly.

 - **Questions** resulted in concise and focused outputs, based on the analysis the *Average prompt length by type* was the highest for questions, resulting in users enquiring or often requiring the factual or stepwise responses to their queries.

 - **Open-Ended** Prompts were the shortest *Average prompt length by type* often resulting in the LLM to generate more conversational or abstract answers to queries. 

 > **Longer Prompts lead to richer responses**

  - Based on the *Prompt Length vs Response Length* feature a **moderate positve correlation has been observed (~0.4-0.6) this suggested that increaing prompt length often implied a more lengthy response from the LLM.** 

  - **However extremely long prompts didn't always yield longer or insightful responses** that users required suggesting, **longer prompting always meant that the factual response output was already determined in user query. This showed signs of diminishing returns.**

  > **Prompt-Response Alignment Score varies by type**

   - Using *cosine similarity* between prompts and responses, **Commands had showed the highest alignment scores for semantic similarity, suggesting a much clearer input-output mapping.**

   - **Open-Ended prompts were the second highest, however showing more variation showed that the LLM inferred more based on it's biases and stayed less true to it's original prompt.**

> **Lingustic mapping helps to understand response complexity and suitability**

   - *Readbility metrics (Flesch/Gunning Fog)* were used to show that **Command based responses were more formal and structured and often gave users only the most required information for that prompt.**

   - **Open-Ended prompts were more readable and conversational, often showing variation in the response quality**

> **Sentiment varies with prompt category**

   - **Open-Ended prompts showed signs of the higest subjectivity and more positve polarity when compared to other prompt types, suggesting greater emotional tone and flexibility to responses.**

- **Questions and Commands were similar in subjectivity and showed lower polarity leaning towards more neutral apporaches to response stucture.**

## Best Practices for Prompt Engineering

> Response Length and Clarity 

 - Commands are the most effective for detailed responses especially for better structure in repsonse layout and response length. This can be effectively utilised in business queries.

 - Open ended prompts have better variation in clarity and often suit more for human-centered conversations, which show that these can be leveraged better in chatbot use-cases.

> Prompt Structure and Length

 - Users should often aim for specific and concise prompting to help guide the LLM towards more structured responses that utlise control and relevance to prompt query. This helps the LLM from deviating and rather provide better responses for users.

 - Long prompt queries can be utlised to help generate longer responses, but only upto a certain degree and depending on the prompt type. Mostly Open-Ended prompts and commands show charaterstics for longer response sequence, however users should be know that high quality responses often require clarity and control over prompt structure and length.

> Semantic Similarity 

 - For consistent and predictable answers, use explicit prompt sturctures, generally commands are the most suitable option for this type of task. They show the best input-output mapping, resulting in more accurate response.

- For Idea generation and creativity, open-ended and questions often give more flexibility to repsonse output. 

> Sentiment variation

 - For more polarity and subjectivity, open-ended prompts often show much greater emotional tonality than commands and questions. This can be useful for applications, that are utlised in healthcare, where a more emotional tone can help for better engagement for the user.

  - Questions and Commands lean more towards a netural tone and give a better objectivity in responses for users. These types of prompts are better utilised in chatbots.

> Lingustic features for appropriate response complexity

 - Having a High level structure for prompting can be useful for more task-based responses, these often can be helpful for providing structured responses for high-logic or multi step tasks.

 - Conversational tones are more useful, when the user is giving an open-ended or question based prompt, which result in tasks that require more emotional tone and empathetic engegement to user. These types of prompts a better utilised in chatbot integrations, where user interaction is more varied and less structured.


***

## Files
- `data/prompt_engineering_dataset.csv`: Contains the dataset used for analyzing prompts and responses in CSV format.
- `notebooks/Prompt_Analyser.ipynb`: Jupyter notebook that includes code for data loading, visualization, and analysis of prompt and response lengths.
- `src/__init__.py`: Marks the `src` directory as a Python package.
- `requirements.txt`: Lists the Python dependencies required for the project.

## Installation
To set up the project, clone the repository and install the required packages using pip:

```bash
pip install -r requirements.txt
```

## Usage
Open the Jupyter notebook `notebooks/Prompt_Analyser.ipynb` to start analyzing the dataset. The notebook contains all the necessary code to load the data, perform visualizations, and analyze the results.

## License
This project is licensed under the MIT License.