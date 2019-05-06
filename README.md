# Introduction

Have you ever tried to remember this song name, where you know what the song is about, and some parts of the lyrics, but can't remember what song it is? Today we are going to learn a very easy way *(read: overly complicated but hey, we're learning something new- way)* to be able to remember what song it is. 

Today we are going to learn about a text analytics/NLP method called topic modeling. Topic modeling is primarily used for two reasons: 

* Identifying what a particular document or corpus of documents is talking about.
* What are the top terms relating to a topic. 


## Theory

We will need to understand two main theories related to topic modeling before we proceed. 

### 1. LDA: Latent Dirichlet Allocation

LDA is a generative probabilistic model of a corpus. The basic idea is that the documents are represented as random mixtures over latent topics, where a topic is characterized by a distribution over words. Latent Dirichlet allocation (LDA), first introduced by Blei, Ng and Jordan in 2003, is one of the most popular methods in topic modeling. LDA represents topics by word probabilities. The words with highest probabilities in each topic usually give a good idea of what the topic is can word
probabilities from LDA. 

Various methods have been proposed to estimate LDA parameters, Gibbs sampling is one of the more commonly used method:

Gibbs sampling, is a Monte Carlo Markov-chain algorithm, powerful technique in statistical inference, and a method of generating a sample from a joint distribution when only conditional distributions of each variable can be efficiently computed. According to our knowledge, researchers have widely used this method
for the LDA.

*Parts of the above text taken from: https://arxiv.org/pdf/1711.04305.pdf . Please go through the document for mathematical explanation of how LDA works.*

### 2. TFIDF: Term Frequency Inverse Document Frequency

TFIDF is another method (not exactly relating to topic modeling but commonly used together) which helps us get the top terms for a given document, when the document is a part of a bigger corpus. The main idea behind TFIDF is:

* The terms which describe the document appear a lot in the document. 
* The terms which particularly describe **this** document appear less across all other documents.

Therefore, to find the top terms for a given document, we just need to find the term frequency for each document (common words having higher frequency value), and then multiply that with an inverse of document frequency(how frequently does that term appear across all documents?)

***
