![KDB.AI Logo](https://kdb.ai/images/logo-kdb.ai-black-bg.png)

The example [KDB.AI](https://kdb.ai) samples provided aim to demonstrate examples of the use of the KDB.AI vector database in a number of scenarios ranging from getting started guides to industry specific use-cases.

## KDB.AI Offerings

KDB.AI comes in two offerings:

1. [KDB.AI Cloud](https://trykdb.kx.com/kdbai/signup/) - For experimenting with smaller generative AI projects with a vector database in our cloud.
2. [KDB.AI Server](https://trykdb.kx.com/kdbaiserver/signup/) - For evaluating large scale generative AI applications on-premises or on your own cloud provider.

Depending on which you use, there will be different setup steps and connection details required.
You can signup at the links above and see the notebooks for connection inctructions.

## What is KDB.AI?

KDB.AI is a time-based vector database that allows developers to build scalable, reliable, and real-time applications by providing advanced search, recommendation, and personalization for Generative AI applications. KDB.AI is a key component of full-stack Generative AI applications that use Retrieval Augmented Generation (RAG).

Built by KX, the creators of kdb+, KDB.AI provides users with the ability to combine unstructured vector embedding data with structured time-series datasets to allow for hybrid use-cases which benefit from the rigor of conventional time-series data analytics and the usage patterns provided by vector databases within the Generative AI space.


## What does KDB.AI support?

KDB.AI supports the following feature set:

- Multiple index types: Flat, IVF, IVFPQ and HNSW.
- Multiple distance metrics: Euclidean, Inner-Product, Cosine.
- Top-N and metadata filtered retrieval
- Python and REST Interfaces


## Sample Breakdown

At this time, the repository contains the following samples:

### Getting Started

- [Python Quickstart](quickstarts/python_quickstart.ipynb): A quick introduction to the KDB.AI APIs in Python.

### Use-Cases

- [TSS_non_transformed](TSS_non_transformed): Temporal Similarity Search (Non Transformed) time series search.
- [TSS_transformed](TSS_transformed): Temporal Similarity Search (Transformed) for time series search. 
- [LlamaIndex Advanced RAG](LlamaIndex_advanced_RAG): Demonstration on how to use LlamaIndex with KDB.AI for RAG.
- [Document Search](document_search): Semantic Search on PDF Documents.
- [Hybrid Search](hybrid_search): Combine dense and sparse search to improve accuracy.
- [Image Search](image_search): Image Search on Brain MRI Scans.
- [Metadata Filtering](metadata_filtering): Metadata Filtering to increase search speed and accuracy.
- [Multimodal RAG ImageBind](multimodal_RAG_ImageBind): Multimodal RAG with images and text.
- [Multimodal RAG Unified Text](multimodal_RAG_unified_text): Multimodal RAG with images descriptions and text.
- [Recommendation System](music_recommendation): Music Recommendation on Spotify Data.
- [Pattern Matching](pattern_matching): Pattern Matching on Sensor Data.
- [Retreival Augmented Generation with LangChain](retrieval_augmented_generation): Retrieval Augmented Generation (RAG) with LangChain.
- [Retreival Augmented Generation Evaluation with LangChain](retrieval_augmented_generation_evaluation): Retrieval Augmented Generation (RAG) Evaluation with LangChain.
- [Sentiment Analysis](sentiment_analysis): Sentiment Analysis on Disneyland Resort Reviews.


## What Platforms Does KDB.AI Integrate With?

- [ChatGPT Retrieval Plugin](https://github.com/KxSystems/chatgpt-retrieval-plugin/blob/KDB.AI/examples/providers/kdbai/ChatGPT_QA_Demo.ipynb): Example showing a question and answer session using a ChatGPT retrieval plugin using KDB.AI Vector Database.
- [Langchain](https://github.com/KxSystems/langchain/blob/KDB.AI/docs/docs/integrations/vectorstores/kdbai.ipynb): Example showing a question and answer session using a Langchain integration with the KDB.AI Vector Database.


## Setup

This section details the setup steps required to run these samples locally on your machine.

### Prerequisites

This setup guide assumes the following:
  1. You are using a Unix terminal or similar
  2. You have `python` >= 3.8 installed
  3. You have `pip` installed

### Install Python Packages

1. The necessary pip installs are at the beginning of each notebook.
    (optional) To see a comprehensive list of requirements, see the `requirements.txt` file in the repository.

    ```bash
    pip install -r requirements.txt
    ```

> [!TIP]
> <b>Running out of disk space?</b>
> By default, pytorch installs both GPU and CPU related packages.
> This repo does not require a GPU and hence, will only make use of the CPU related packages.
> By running the below install command, you will only install the CPU related packages and save approximately 1.5GB of disk space.
> This command is optional and if run, should be run prior to the above install command.
> ```bash
> pip install torch --index-url https://download.pytorch.org/whl/cpu
> ```


### View & Execute The Samples

1. Run a jupter notebook session:

    ```bash
    jupyter notebook --no-browser
    ```

    This will load up the jupyter session in the background and display a URL on screen for you.

1. Paste this URL into your browser

    This will bring up the samples for you to interact with.


## Dataset Disclaimer

In this repository, we may make available to you certain datasets for use with the Software.
You are not obliged to use such datasets (with the Software or otherwise), but any such use is at your own risk.
Any datasets that we may make available to you are provided “as is” and without any warranty, including as to their accuracy or completeness.
We accept no liability for any use you may make of such datasets.
