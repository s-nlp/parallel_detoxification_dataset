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

## Dataset Information

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
@inproceedings{dementieva2021crowdsourcing,
    title = "Crowdsourcing of Parallel Corpora: the Case of Style Transfer for Detoxification",
    author = {Dementieva, Daryna
                 and Ustyantsev, Sergey
                 and Dale, David 
                 and Kozlova, Olga
                 and Semenov, Nikita
                 and Panchenko, Alexander
                 and Logacheva, Varvara},
    booktitle = "Proceedings of the 2nd Crowd Science Workshop: Trust, Ethics, and Excellence in Crowdsourced Data Management at Scale co-located with 47th International Conference on Very Large Data Bases (VLDB 2021 (https://vldb.org/2021/))",
    year = "2021",
    address = "Copenhagen, Denmark",
    publisher = "CEUR Workshop Proceedings",
    pages = "35--49",
    url={http://ceur-ws.org/Vol-2932/paper2.pdf}
}
```
and check the latest version of the English ParaDetox in:
```
@inproceedings{logacheva-etal-2022-paradetox,
    title = "{P}ara{D}etox: Detoxification with Parallel Data",
    author = "Logacheva, Varvara  and
      Dementieva, Daryna  and
      Ustyantsev, Sergey  and
      Moskovskiy, Daniil  and
      Dale, David  and
      Krotova, Irina  and
      Semenov, Nikita  and
      Panchenko, Alexander",
    booktitle = "Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = may,
    year = "2022",
    address = "Dublin, Ireland",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2022.acl-long.469",
    pages = "6804--6818",
    abstract = "We present a novel pipeline for the collection of parallel data for the detoxification task. We collect non-toxic paraphrases for over 10,000 English toxic sentences. We also show that this pipeline can be used to distill a large existing corpus of paraphrases to get toxic-neutral sentence pairs. We release two parallel corpora which can be used for the training of detoxification models. To the best of our knowledge, these are the first parallel datasets for this task.We describe our pipeline in detail to make it fast to set up for a new language or domain, thus contributing to faster and easier development of new parallel resources.We train several detoxification models on the collected data and compare them with several baselines and state-of-the-art unsupervised approaches. We conduct both automatic and manual evaluations. All models trained on parallel data outperform the state-of-the-art unsupervised models by a large margin. This suggests that our novel datasets can boost the performance of detoxification systems.",
}
```

***

## Contacts

For any questions please contact Daryna Dementieva via [email](mailto:dardem96@gmail.com).
