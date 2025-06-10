# ML Driven Prompt Engineering
Build a Custom OpenAI Chatbot with ML-Driven Prompt Engineering

## Here's how I built the custom Q&A bot:

#### Step 1: Prepare a Dataset with Embeddings
Pull text data from the Wikipedia page about the year 2022(opens in a new tab). Pull text data from the Wikipedia page about the 2023 Turkey-Syria earthquake(opens in a new tab).

In each case, our dataset is initially composed of text data. Before any machine learning model can make sense of any kind of data, that data needs to be converted into numbers. For our unsupervised machine learning model, we are going to use text data that has been transformed into vectors of floating point numbers. These vectors are called embeddings and we will use an OpenAI Embedding model to generate them.


#### Step 2: Find Relevant Data with Unsupervised Machine Learning
Once our dataset has been converted into embeddings, we can get a question from the user and perform a text search of our dataset using a measure called cosine similarity. This is more sophisticated than a basic text matching search because it uses the underlying embedding vector representation of the text, not just the exact wording used in the question.

An icon indicating a question on the left, with three arrows pointing to rows of the embeddings index. Highlighted boxes show the most relevant data found using cosine similarity


#### Step 3: Compose a Custom Text Prompt
We will use the results of the previous step to compose a custom text prompt that incorporates both the user's question and the most relevant context from our dataset. We will use a tokenizer to measure the length of our prompt and ensure that it doesn't exceed the limits of the OpenAI Completion model.

Icon representing the embeddings index with relevant rows selected on the left, an arrow showing how those rows become part of the prompt along with the original question
Step 4: Query a Completion Model
Once we have the custom text prompt, the last step is to send that prompt to an OpenAI text completion model and parse the response. This will provide the user with a tailored answer to their question!

Custom prompt resulting in a correct answer
