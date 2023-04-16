# Facebook-Post-Sentiment-Analysis-NLP-using-RNNs

## Background
As one of the largest social media websites in the world, Facebook is an attractive platform for businesses to reach their consumers. Almost all consumer-facing businesses have virtual presence on Facebook, in the form of Facebook business pages. Everyday, Facebook users who visit these business pages generate a large amount of posts. These user posts may represent customer complains, questions, or appreciations directed towards the focal businesses.

For businesses, these user posts contain valuable information about customers' needs and preferences, and understanding what the user posts are talking about represents an important opportunity to get to know your customers in real-time.

## Dataset and Task
Use a labeled dataset named "FB_posts_labeled.txt". It is a tab-delimited file with the following fields:

postId: this is a unique identifier for each user post. There are 7961 posts in total;
message: this is the text of each post;
Appreciation: this is a binary (0/1) indicator of whether a post is an appreciation;
Complaint: this is a binary (0/1) indicator of whether a post is a customer complaint;
Feedback: this is a binary (0/1) indicator of whether a post is a customer feedback (e.g., questions and suggestions).

## Result 
Appreciation, Complaint, and Feedback are the three mutually exclusive content categories / classes in this dataset. They were labeled by humans, and the labeling isn't perfect (i.e., there may be ambiguous cases where the labels are not appropriate). The task is to build a text classifier to predict the content category of a post based on its textual content.

## Technical Approach
I used embedding layer to convert text into numerical embeddings
Used oversampling becuase of imbalanced data (SMOTE)
Then ran different RNNs like LSTM, GRU, Bidirectional GRUs to process temporal information
Added a target softmax dense layer to predict review class (Appreciation, Complaint, Feedback)

## Results
Final F1 score - 0.74
Using BERT embeddings - 0.84
