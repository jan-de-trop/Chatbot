# Chatbot fine-tuned to answer FAQs
## An application of NLP to question-answering tasks
### Goal: create a tool that automatically answers frequently asked questions posed by students, ex.:
- What is the deadline for exercise
submission?
- Will the sessions be recorded?
- Where to submit the homework?


### Datasets:
- SQuAD2.0: contains ~100,000 questions, Train set, Dev Set. 
- Univ.ai Frequently Asked Questions: Faq.csv, Test.csv, and manually added context

### Baseline Model: RNN with sentence piece word embeddings
![image](https://user-images.githubusercontent.com/77740301/121856246-e9779b00-cd11-11eb-8ad7-1efcd7304ff1.png)

### ALBERT 
A pretrained model from HuggingFace was trained on SQuAD2.0 for 3 epochs and fine-tuned on the FAQ data with the manually added context.
![image](https://user-images.githubusercontent.com/77740301/121856575-43786080-cd12-11eb-815b-48307ea7a39b.png)

### ALBERT with cross-encoder
As a solution to the adding the context for a dataset manually, automatic context retrieval was used. 
![image](https://user-images.githubusercontent.com/77740301/121856833-9225fa80-cd12-11eb-8520-d9780028ddb5.png)
![image](https://user-images.githubusercontent.com/77740301/121856882-a36f0700-cd12-11eb-898f-804ab9357014.png)

The model was fine-tuned on the FAQ data and performed satisfactorily.
![image](https://user-images.githubusercontent.com/77740301/121857225-0496da80-cd13-11eb-9995-658902fb694e.png)
