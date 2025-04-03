# Parallel Text Detoxification Dataset
This repository contains parallel text detoxification dataset for the task of elimination toxicity from the texts. The pipeline used for this dataset collection was presented in "Crowdsourcing of Parallel Corpora: the Case of Style Transfer for Detoxification" paper presented at [VLDB 2021 Crowd Science Workshop](https://crowdscience.ai/conference_events/vldb21).

***
📰 **Updates**

Check out **TextDetox** 🤗 https://huggingface.co/collections/textdetox/ -- continuation of ParaDetox project!

**[2025] !!!NOW OPEN!!! TextDetox CLEF2025 shared task: for even more -- 15 languages!** [website](https://pan.webis.de/clef25/pan25-web/text-detoxification.html) 🤗[Starter Kit](https://huggingface.co/collections/textdetox/)

**[2025] COLNG2025**: Daryna Dementieva, Nikolay Babakov, Amit Ronen, Abinew Ali Ayele, Naquee Rizwan, Florian Schneider, Xintong Wang, Seid Muhie Yimam, Daniil Alekhseevich Moskovskiy, Elisei Stakovskii, Eran Kaufman, Ashraf Elnagar, Animesh Mukherjee, and Alexander Panchenko. 2025. ***Multilingual and Explainable Text Detoxification with Parallel Corpora***. In Proceedings of the 31st International Conference on Computational Linguistics, pages 7998–8025, Abu Dhabi, UAE. Association for Computational Linguistics. [pdf](https://aclanthology.org/2025.coling-main.535/)

**[2024]** We have also created versions of ParaDetox in more languages. You can checkout a [RuParaDetox](https://huggingface.co/datasets/s-nlp/ru_paradetox) dataset as well as a [Multilingual TextDetox](https://huggingface.co/textdetox) project that includes 9 languages.

Corresponding papers:
* [MultiParaDetox: Extending Text Detoxification with Parallel Data to New Languages](https://aclanthology.org/2024.naacl-short.12/) (NAACL 2024)
* [Overview of the multilingual text detoxification task at pan 2024](https://ceur-ws.org/Vol-3740/paper-223.pdf) (CLEF Shared Task 2024)

**[2022] ParaDetox** for English, the full version with experiments, was presented at ACL2022! [repo](https://github.com/s-nlp/paradetox/tree/main) [paper](https://aclanthology.org/2022.acl-long.469/)
***

## Data Collection Methodology
The whole pipeline of the collection was divided into three tasks:
- Task 1: detoxified paraphrase generation;
- Task 2: content preservation check of obtained results from Task 1;
- Task 3: toxicity check of obtained results from Task 1;

The crowdsourcing was conducted with [Toloka.ai](https://toloka.ai) crowdsourcing platform.

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
