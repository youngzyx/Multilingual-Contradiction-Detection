# Multilingual-Contradiction-Detection
#### Team: [Yoli Wu](https://github.com/hereisyoli), [Young Zeng](https://github.com/youngzyx/)

## Goal
Classifying pairs of sentences (consisting of a premise and a hypothesis) into three categories - entailment, contradiction, or neutral.  

## Dataset
* the train and test set include text in 15  different languages:
  * Arabic, Bulgarian, Chinese, German, Greek, English, Spanish, French, Hindi, Russian, Swahili, Thai, Turkish, Urdu, and Vietnamese.
* Train: 12120(2.77 MB) (include premise, hypothesis, language, label)
* Test: 5195(1.18 MB)

Link: https://www.kaggle.com/competitions/contradictory-my-dear-watson/data 

### Example
#### Premise:
`He came, he opened the door and I remember looking back and seeing the expression on his face, and I could tell that he was disappointed.`

#### Hypothesis 1:
`Just by the look on his face when he came through the door I just knew that he was let down.`<br/>
We know that is true based on the information in the premise, so this pair is related by **entailment**.

#### Hypothesis 2:
`He was trying not to make us feel guilty but we knew we had caused him trouble.`<br/>
We can't know if it is true based on the premise, therefore the relationship is **neutral**

#### Hypothesis 3:
`He was so excited and bursting with joy that he practically knocked the door off it's frame.` <br/>
We know that is not true given the information on the premise, hence the relationship of this pair is **contradiction**


## Models
### [XLM-RoBERTa](https://huggingface.co/joeddav/xlm-roberta-large-xnli)
> This model takes xlm-roberta-large and fine-tunes it on a combination of NLI data in 15 languages. It is intended to be used for zero-shot text classification, such as with the Hugging Face ZeroShotClassificationPipeline.

## Result

## Reference
#### Tips
**NLI** (Natural language inference) model is a model that attempts to infer the correct label based on the two sentences.
  
