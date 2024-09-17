# Project Title

ICI_Chatbot

## Project Description

The ICI Chatbot is a project designed to provide users with easy access to information about ICI (International College of Innovation, National Chengchi University). The chatbot utilizes a trained AI model to answer questions related to ICI's website, courses, admissions, curriculum, student experiences, and more. It aims to improve student engagement, enhance efficiency, and save time by providing immediate responses and handling routine inquiries. To ensure the correctness of the data we used, all the information was gathered from ICI’s office and ICI's current students. With llama_index, we were able to create a large language model application that uses Chat GTP to help us generate accurate responses.
With the help of ICI Chatbot, an efficient way of communication will be created. The current students, professors, parents, or anyone who is interested in ICI can learn about the college by themselves, there is no need to email the office and wait for ICI’s staff to reply anymore, while ICI’s staff will be able to focus more on their work and improve the work efficiency.


## Getting Started

ICI Chatbot is written in Python, to get started with the ICI Chatbot, follow these steps: 
1. Run the Python code:
   llama_index, Openai and Gradio are the required packages for our model.

   First, we will import GPTVectorStoreIndex, SimpleDirectoryReader, Document, LLMPredictor,
   PromptHelper, ServiceContext, and GPTListIndex from llama_index. Connect to google drive to
   import the input data file. and install Openai (the Openai’s API key is required, in order
   to get access to its service.)

   Second, we must remove the heading section in the input file and because the input file is
   in the template of question-answer, one-by-one, therefore, we will remove all the questions
   also.

   Third, create a comprehensive framework for organizing and accessing document data based on
   the extracted nodes and contents by using
   - SimpleNodeParser to extract nodes from the document
   - using GPTVectorStoreIndex to create an index to store and organize the nodes that we
     extracted
   - using StorageContext to manage data storage and adding nodes to enhance our data retrieval
     capabilities, we created additional indices by using GPTVectorStoreIndex and GPTListIndex,
     which will offer a different method of organizing and accessing the nodes.
   - using GPTVectorStoreIndex to create an empty index for inserting each document into the
     index, which enables efficient retrieval or searching based on their content.
	
    Fourth, set up the model with specific settings such as the maximum size of the input, the
   number of output tokens, the maximum overlap between chucks, etc. and create an index to
   store information. Then, it configures a system to search and retrieve information from the
   index based on user queries.
   
2. Interact with the chatbot by inputting your questions or queries on Gradio:
   In order to make our model more use- friendly, we create a user interface by installing Gradio and create a function to interact with users by answering user’s
   questions.

3. See how the chatbot answers



## File Structure

The file structure of the ICI Chatbot project is as follows:
1. README.md: Contains information about the project, including instructions and descriptions.
2. FAQs.txt: Contains all the datasets we need in order to train our model to generate accurate
   answers. This file will be used solely as our database. The FAQs.txt consists of 44 pairs of
   questions and answers which covered ICI’s courses, admissions, curriculum, students'
   experiences, etc. We collected all the data from ICI’s office and ICI’s current students.
   This file is required to import to the Final Chat bot BRI llama-index.py.
3. Final Chatgpt bot BRI llama-index.py: The main Python file that implements the chatbot
   application.



## Analysis

The ICI Chatbot uses a combination of data ingestion, indexing, querying, and response generation techniques. It employs the llama_index package to build LLM (Language Model)-based applications. The code reads documents from a text file, indexes then uses GPTVectorStoreIndex for efficient searching, after that QueryEngine is used to query the stored documents. The responses are synthesized using the ResponseSynthesizer, which utilizes the LLM model.

The accuracy rate of the chatbot is reported to be 99%. However, it is important to note that if users input inquiries unrelated to ICI or beyond the scope of the provided data set, the answers may seem strange. The project emphasizes the need for future updates to the data set to maintain a high accuracy rate.


## Results

Our goal is to create an efficient way for users to get to know the International College of Innovation by using the ICI Chatbot. In this context, we will measure the efficiency by using the time spent searching for the answer and the accuracy of the answer. Normally, if you have a question about ICI, you may have to email ICI’s office or find an ICI’s current student and ask. This process takes time and also put an unnecessary workload on ICI’s staff to answer some repeated questions, which is not an efficient way of communication. 

The chatbot successfully provides an efficient and user-friendly way to access information about ICI. Users can input questions and receive immediate accurate responses related to ICI's website, admissions, courses, curriculum, student experiences, and more. The chatbot's 24/7 availability ensures that queries are answered at any time, which meets the conditions on reduce the time spent searching for an answer and a very high accuracy rate. 

In conclusion, the 99% accuracy rate and constant accessibility of the ICI Chatbot will reduce the workload on ICI's staff while simultaneously providing users with the answers to their queries. To further improve the accuracy and relevance of the chatbot's responses, the data set will need to be updated in the future. Similarly, our Python code, which uses the llama_index package, will need to be updated if the package updates in the future. 

For recommendation, Installing our chatbot on ICI's website might not be the best idea, as Taiwanese people frequently use Line. Therefore, applying our model to create a Line chatbot might match users' behaviour.


## Contributors

Jongsung Shin, Varinthon Chowanajin, Pingfa

## Acknowledgments

Project supervisor: Professor Chung Pei Pien
Data provider: ICI's office

## References

1. https://llamahub.ai/l/file
2. https://gpt-index.readthedocs.io/en/stable/guides/primer/usage_pattern.html
3. https://github.com/jerryjliu/llama_index/issues/1900
4. https://github.com/jerryjliu/llama_index

