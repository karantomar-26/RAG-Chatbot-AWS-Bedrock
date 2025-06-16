# RAG Chatbot with AWS Bedrock

A Retrieval‑Augmented Generation (RAG) chatbot that uses AWS Bedrock, Amazon S3, and Amazon OpenSearch Serverless to answer questions based on your own documents.

## Overview

This project demonstrates how to:
- Store documents in Amazon S3
- Chunk and embed them using AWS Bedrock
- Index embeddings into OpenSearch Serverless
- Build a chatbot that retrieves relevant information and generates grounded answers

## Architecture

1. Upload documents (e.g., PDF, text, markdown) into an S3 bucket.
2. Create a Bedrock Knowledge Base connected to the S3 bucket.
3. Bedrock chunks, embeds, and stores them in a vector index (OpenSearch Serverless).
4. User submits a query.
5. Bedrock embeds the query, retrieves top-k document chunks via vector similarity, and sends them to the LLM.
6. The LLM generates a response grounded in the retrieved content.

## Prerequisites

- AWS account with permissions for:
  - AWS Bedrock (Knowledge Bases + embedding and generative models)
  - Amazon S3
  - Amazon OpenSearch Serverless
- AWS CLI configured
- Python 3.8+ environment
- (Optional) Infrastructure-as-code (CDK or Terraform)

