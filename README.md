

#### Table of contents
1. [Introduction to BERT](#introduction)
2. [BERTweet](#Bertweet)
3. [BERTweet Language Model Sentiment Classifier](#Classifier)
    - [Pre-trained models](#models2)
    - [Example usage](#usage2)
    - [Normalize raw input Tweets](#preprocess)
4. [Using BERTweet with `fairseq`](#fairseq)


# <a name="introduction"></a> An Introduction to BERT Language Model


With the breakthrough of "Transfer Learning" in Natural Language Processing (NLP), the landscape has been completely transformed. Regarded as "Language Modelling” in the NLP landscape, Transfer learning can exploit almost infinite amount of unlabelled textual data to get dynamic representations of word vectors as oppose to the static word vectors generated by the early NLP models. The main idea behind language modelling was to pre-train an extremely large unsupervised model on a NLP tasks to generate and ‘Transfer’ the contextually aware words vectors acquired to a downstream task at hand. In addition to this, the development of “Transformers” by Google AI in a paper called "Attention is all you need”, came over the limiting properties of the gradient based learning algorithms in RNN’s (Recurrent Neural Networks). 


As opposed to the sequential processing of RNN’s, Transformers can perform input processing in parallel, enabling them to deal with larger corpora more efficiently. Being non-sequential and able to process sentences as a whole, transformers utilised a novel technique called ‘Multi Head Self-Attention’ to ‘Attend’ to words and their context throughout the entire sentence and learn the contextual relationship between different words. This was in contrast to previous recurrent based models such as LSTM’s, which captured word dependencies by relying on the past hidden states, which lead to the risk of losing and forgetting past information. 

With these developments, the "Bidirectional Encoder Representations from Transformers" (BERT) was introduced. Regarded as "conceptually simple and empirically powerful" by the Google researchers, BERT was pre-trained on two unsupervised tasks; Next Sentence Prediction (NSP) and Masked Language Model (MLM). The combination of the two enabled BERT to alleviate the unidirectionality limitation of the previous GPT model. Bidirectionallity being the most emphasised innovative feature by the researchers, BERT has outperformed all the previous models in most of the NLP tasks, particularly in sentiment classification. 

<p align="center">
<img src="/Figures/Figure4.png" width="500" height="420">
</p>

# <a name="Bertweet"></a> BERTweet: A pre-trained language model for English Tweets 



BERTweet is the first public large-scale language model pre-trained for English Tweets. BERTweet is trained based on the RoBERTa pre-training procedure. The corpus used to pre-train BERTweet consists of 850M English Tweets (16B word tokens ~ 80GB), containing 845M Tweets streamed from 01/2012 to 08/2019 and 5M Tweets related to the COVID-19 pandemic.

# <a name="Classifier"></a> BERTweet Language Model Sentiment Classifier


This is a implementation of the Bertweet language model for sentiment classification of tweets. 
  The fine-tuning precedure is depicted visually in the graph below. 
  This model Achieved state of the art results (73% Accuracy) based on the SemEval task7a benchamrk. 

![ScreenShot](/Figures/Figurex.png)




