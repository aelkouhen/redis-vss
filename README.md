# Rediscover Redis for Vector Similarity Search
Redis Vector Similarity Search Workshop Materials.

## Shared Materials

<table>
    <tr>
        <td><a href="https://drive.google.com/file/d/1pINEMJ_WFa5gusTl4oqtDLBGg3NbTuZ7"><img src="images/Vid.png" style="float: right;" width="500" height="200"/></a> Video Tutorial (FR) </td> 
        <td width="50%"><a href="https://docs.google.com/presentation/d/1-81YCn6ORjXM9HEbLLez9I-8s6DCVq28"><img src="images/Deck.png" style="float: right;" width="500" height="200"/></a> Slides Deck </td> 
    </tr>
</table>

## Table of Contents

* [Pre-requisites](#Pre-requisites)
* [Text Vector Search](#demo-1-text-vector-search-)
* [Visual Vector Search](#demo-2-visual-vector-search-)
* [Hybrid Search](#demo-2bis-hybrid-search-)
* [Semantic Search](#demo-3-semantic-search-)
* [Retieval-Augmented Generation using GCP VertexAI](#demo-4-retieval-augmented-generation-rag-gcp)
* [Retieval-Augmented Generation using AWS Bedrock](#demo-4bis-retieval-augmented-generation-rag-aws)

## Pre-requisites
You need to create a Redis Enterprise DB with `RedisJSON` and `RediSearch` modules. Then, Use the public endpoint in the notebooks.

To create a Redis Enterprise database, you can use [Redis Cloud](https://app.redislabs.com/) or you can provision a cluster in your own infrastructure using [TerrAmine](https://github.com/amineelkouhen/terramine).

<img width="1501" alt="Capture d’écran 2023-10-06 à 15 59 35" src="https://github.com/aelkouhen/redis-vss/assets/22400454/56e95c06-4a71-4ec7-8244-59cc207b4915">

## Demo 1: Text Vector Search [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aelkouhen/redis-vss/blob/main/1-%20Text%20Vector%20Search.ipynb) 

In this demo, you will learn how to:
- Create vector embeddings for text,
- Persist vector integrations in Redis,
- Create a Secondary Search Index on these Vectors,
- Find similarity between a new vector (text) and already persisted vectors.

<img width="1081" alt="Capture d’écran 2023-11-24 à 23 53 34" src="https://github.com/aelkouhen/redis-vss/assets/22400454/0080140c-553b-412e-856e-bd766fbca6c6">

## Demo 2: Visual Vector Search [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aelkouhen/redis-vss/blob/main/2-%20Visual%20Vector%20Search.ipynb) 

In this second demo, you will learn how to:
- Create vector embeddings for products (by image),
- Persist vector embeddings in Redis,
- Create a Secondary Search Index on these Vectors,
- Find similarity between a new vector (image) and the already persisted vectors.

![ezgif-2-9f2d8adeb3](https://github.com/aelkouhen/redis-vss/assets/22400454/665fce8f-85d5-4b09-8352-3f3d91f43755)

## Demo 2bis: Hybrid Search [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aelkouhen/redis-vss/blob/main/2bis-%20Hybrid%20Search.ipynb)

In this demo, you will learn how to:
- Create vector embeddings for products (by image),
- Persist JSON documents containing the vector embeddings and other fields (e.g., tag, location, price...) in Redis,
- Create a Secondary Search Index on these documents,
- Find similarity between a new vector (image) and the already persisted vectors.
- Search for similarity between a new vector (image) and already persisted vectors, pre-filtered by a tag, a location, or a price range.
  
![Capture d’écran 2023-10-02 à 14 40 28](https://github.com/aelkouhen/redis-vss/assets/22400454/0f44f5aa-c74b-472a-ae69-a224d136dfe2)

## Demo 3: Semantic Search [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aelkouhen/redis-vss/blob/main/3-%20Semantic%20Vector%20Search.ipynb)

In this demo, you will learn how to:
- Create vector embeddings for a private knowledge base (e.g., White papers, blog posts, newsletters...),
- Persist vector embeddings in Redis,
- Create a Secondary Search Index on these Vectors,
- Search semantically (natural language) for the already persisted vectors (relevant resources),
- Use Redis as a semantic cache.
  
![Semantic_Search](https://github.com/aelkouhen/redis-vss/assets/22400454/09fc612a-6276-4c12-9986-c8fa7ac4e25d)

## Demo 4: Retieval-Augmented Generation (RAG) on GCP VertexAI [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aelkouhen/redis-vss/blob/main/4-%20Retrieval-Augmented%20Generation%20(RAG)%20-%20GCP.ipynb)

In this last demo, you will learn how to:
- Create vector embeddings for a private knowledge base (e.g., PDF files, blogs posts, Database),
- Persist vector embeddings in Redis,
- Create a Secondary Search Index on these Vectors,
- Search semantically (natural language) for the already persisted vectors (relevant resources),
- Use relevant resources as a prompt context for LLM conversation,
- Generate an augmented response (natural language) using GCP VertexAI models (PaLM),
- Use Redis as a standard cache,
- Use Redis as a semantic cache,
- Use Redis as Q/A history.

![RAG](https://github.com/aelkouhen/redis-vss/assets/22400454/527f06e7-fcfc-4b78-a479-56a29c0ee03e)

## Demo 4bis: Retieval-Augmented Generation (RAG) on AWS Bedrock [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aelkouhen/redis-vss/blob/main/4-%20Retrieval-Augmented%20Generation%20(RAG)%20-%20AWS.ipynb)

In this last demo, you will learn how to:
- Create vector embeddings for a private knowledge base (e.g., PDF files, blogs posts),
- Persist vector embeddings in Redis,
- Create a Secondary Search Index on these Vectors,
- Search semantically (natural language) for the already persisted vectors (relevant resources),
- Use relevant resources as a prompt context for LLM conversation,
- Generate an augmented response (natural language) using AWS Bedrock models (Anthropic Claude 2),
- Use Redis as a standard cache,
- Use Redis as a semantic cache,
- Use Redis as Q/A history.

![RAG-AWS](https://github.com/aelkouhen/redis-vss/assets/22400454/fb682bb1-be9f-437e-8cfc-9976df1493a0)
