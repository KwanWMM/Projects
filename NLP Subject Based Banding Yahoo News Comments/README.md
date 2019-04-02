# NLP Project on Subject Based Banding/Streaming News
This is a small project on web scraping and various NLP techniques. The objective is to apply several techniques such as sentiment analysis and topic modelling on comments on the recent news on streaming and subject based banding and discover insights from these techniques on local news. It is not meant for arguing for or against policy(ies).
<br>
<br>
## Data
I scraped comments and replies to comments from 4 yahoo new articles and polls related to recent news about streaming and the incoming subject based banding (which contrary to popular belief, is not a sudden move. It has been trialled in schools for some years.). While the total number of comments and replies are not very large and has great selection bias, the choice was due to my personal interest in the matter, both as a Singaporean and having been an educator.
<br>
<br>
## Part 1: VADER Sentiment Analysis
The aim of using VADER was to see how it would perform on comments from Singaporeans (or at least, comments on Singapore news). VADER takes into account punctuation, capitalization, degree modifiers and is specifically attuned to sentiments expressed in social media. While it also takes into consideration Emojis, Slangs and Emoticons, I was also curious about how it would perform given Singaporean colloquialisms.  

Original paper on VADER:  
Hutto, C.J. & Gilbert, E.E. (2014). VADER: A Parsimonious Rule-based Model for Sentiment Analysis of Social Media Text. Eighth International Conference on Weblogs and Social Media (ICWSM-14). Ann Arbor, MI, June 2014.
<br>
Github link: https://github.com/cjhutto/vaderSentiment
<br>
<br>
## Part 2 Topic Modelling
The aim of topic modelling was to see if comments could be clustered by themes. Using sci-kit learn's Latent Dirichlet Allocation(LDA), the comments could be clustered into two main topics; politics and education. Slightly more than half of the comments were about the education system, streaming/subject based banding and social segregation while the rest of the comments were directed more towards politics and the government. Using sci-kit learn's Non-negative Matrix Factorization(NMF) gave similar results, with two main topics and slightly more than half of the comments being about education and social segregation while the rest were about politics and the government. Comparing how the models clustered the comments, about 78% of the comments were clustered similarly. For the remainder of the comments, that was no clear better model as some of the comments did not quite fall under either topic, some comments were more appropriately modelled by NMF but for others, LDA.

Gensim's LDA proved to struggle greatly with creating distinct topics, with or without introducing lemmatization and bigrams. There was great overlap of terms for topics generated with most terms leaning towards education. There were hints of words that might suggest a different topic but no clear distinction. This could be due to the total numbers of comments being low and them having many similar terms.

## Conclusion
VADER did not perform well for sentiment analysis, which isn't too surprising given that while it was trained on social media, it wasn't trained social media from a local context. Many articles that were flagged as having an extremely high compound score were actually held sentiments in the completely opposite direction.

For topic modelling, both LDA and NMF return rather similar topics, with slightly more than half of the comments being about education, while the remainder were focused on politics. Comments regarding education revolved around opinions of the current streaming and proposed changes to subject based banding. They also included comments on the social impact that subject based banding might bring about, whether it be segregation or cohesion. On the other hand, comments regarding politics were focused main on either policy or the government. Some criticised the late introduction of such changes and while others welcomed the new changes. The comments also included laments about the damage already done by the past and current systems and complaints about how the changes were but a new form of streaming, albeit a more granular one. Other comments also criticised the government and regarded the changes as a means of winning votes for a possible upcoming election.
