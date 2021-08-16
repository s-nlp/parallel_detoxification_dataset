# Parallel Detoxification Dataset
This repository contains parallel detoxification dataset for the task of elimination toxicity from the texts. The pipeline used for this dataset collection was presented in "Crowdsourcing of Parallel Corpora: the Case of Style Transfer for Detoxification" paper presented at [VLDB 2021 Crowd Science Workshop](https://crowdscience.ai/conference_events/vldb21).

***

## Data Collection Methodology
The whole pipeline of the collection was divided into three tasks:
- Task 1: detoxified paraphrase generation;
- Task 2: content preservation check of obtained results from Task 1;
- Task 3: toxicity check of obtained results from Task 1;

Here you can see the schematical illustration of the collection pipeline:

![Alt text](https://github.com/skoltech-nlp/parallel_detoxification_dataset/blob/main/collection_pipeline_small.jpg)

***

## Dataset Infomration

Currenlty, the dataset consists of 2,779 pairs of `toxic sentence <-> detoxified sentence`. The unique `toxic sentences` covered are 1108. For each `toxic sentence` there no more than 4 `detoxified sentence`.

Example of samples:
|toxic_comment   |civil_comment   |
|---|---|
|this is scaring the shit out of me.|This is really scaring me.|
|this is a joke , are you all fucking retards?|This is a joke, are you all crazy?|
|all you trump clowns are seriously messed up.|Trumps voters are seriously mislead.|

***

## Citation

If you find this repository helpful, feel free to cite our publication:
```
to be updated
```

***

## Contacts

For any questions please contact Daryna Dementieva via [email](mailto:daryna.dementieva@skoltech.ru) or [Telegram](https://t.me/dementyeva_ds).
