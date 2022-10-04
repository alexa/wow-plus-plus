# WOW++

This README describes WOW++, an augmented version of the WOW dataset that contains multiple knowledge sentences 
for the last turn within a dialogue.

We hope releasing this dataset will benefit the community for research in knowledge selection 
for open-domain dialog.

The original WOW dataset can be [found here](https://parl.ai/projects/wizard_of_wikipedia/).

WOW++ contains three different splits of data:
train/random (test seen)/topic (test unseen). The three files in the dataset include:
- `full_test_random_augmented_wow.json` (198 dialogues)
- `full_test_topic_augmented_wow.json` (200 dialogues)
- `full_train_augmented_wow.json` (400 dialogues)

## Conversation Format
Each file consists of a mapping from dialogue id to a dict with the following info:
- `turns`: The dialogue text
- `topic`: The topic selected for the original dialogue
- `start_speaker`: Which speaker began the dialogue
- `id`: The dialogue id
- `knowledges`: The knowledges provided to the Turker in the original dialogue
- `gold_sentence`: The chosen knowledge sentence by the Turker in the original WOW
- `annotated_sentences`: The annotated WOW++ knowledge sentences with confidence levels (percentage of Turkers that agreed in picking that sentence).


## Citation
If you use the dataset in your work please cite the following 
```
@inproceedings{eric2021multi,
  title={Multi-Sentence Knowledge Selection in Open-Domain Dialogue},
  author={Eric, Mihail and Chartier, Nicole and Hedayatnia, Behnam and Gopalakrishnan, Karthik and Rajan, Pankaj and Liu, Yang and Hakkani-Tur, Dilek},
  booktitle={Proceedings of the 14th International Conference on Natural Language Generation},
  pages={76--86},
  year={2021}
}
```