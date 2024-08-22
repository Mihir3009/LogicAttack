# LogicAttack: Adversarial Attacks for Evaluating Logical Consistency of Natural Language Inference

You may want to check out our paper - [LogicAttack: Adversarial Attacks for Evaluating Logical Consistency of Natural Language Inference](https://aclanthology.org/2023.findings-emnlp.889/)

Recently Large Language Models (LLMs) such as GPT-3, ChatGPT, and FLAN have led to impressive progress in Natural Language Inference (NLI) tasks. However, these models may rely on simple heuristics or artifacts in the evaluation data to achieve their high performance, which suggests that they still suffer from logical inconsistency. To assess the logical consistency of these models, we propose a LogicAttack, a method to attack NLI models using diverse logical forms of premise and hypothesis, providing a more robust evaluation of their performance. Our approach leverages a range of inference rules from propositional logic, such as Modus Tollens and Bidirectional Dilemma, to generate effective adversarial attacks and identify common vulnerabilities across multiple NLI models. We achieve an average ~53% Attack Success Rate (ASR) across multiple logic-based attacks. Moreover, we demonstrate that incorporating generated attack samples into training enhances the logical reasoning ability of the target model and decreases its vulnerability to logic-based attacks.

# Data Release

Please see the `./data` folder to access the LogicAttack datasets re-purposed from SNLI and MNLI.

**License**: MIT License

## JSON file format

```
{
    "instances": [
        {
            "pairID": "string", 
            "premise": "string",
            "hypothesis": "string",
            "premise_negated": "string",
            "hypothesis_negated": "string",
            "label": "string",
            "attack_samples": [
                {
                    "pairID": "string",
                    "premise": "string",
                    "hypothesis": "string",
                    "label": "string",
                    "used_rule": "string"
                },
                {
                    "pairID": "string",
                    "premise": "string",
                    "hypothesis": "string",
                    "label": "string",
                    "used_rule": "string"
                }
                // More attack_samples as needed
            ]
        }
        // More instances as needed
    ]
}
```

## BibTeX Entry and Citation Info ##

If you are using our dataset, please cite our paper:

```bibtex
@inproceedings{nakamura-etal-2023-logicattack,
    title = "{L}ogic{A}ttack: Adversarial Attacks for Evaluating Logical Consistency of Natural Language Inference",
    author = "Nakamura, Mutsumi  and
      Mashetty, Santosh  and
      Parmar, Mihir  and
      Varshney, Neeraj  and
      Baral, Chitta",
    editor = "Bouamor, Houda  and
      Pino, Juan  and
      Bali, Kalika",
    booktitle = "Findings of the Association for Computational Linguistics: EMNLP 2023",
    month = dec,
    year = "2023",
    address = "Singapore",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.findings-emnlp.889",
    doi = "10.18653/v1/2023.findings-emnlp.889",
    pages = "13322--13334",
}
```

## Stay tuned for ...

- Release of source code for data generation, inference, and analysis 

## Contact Information ##
* For help or issues in using LogicAttack, please submit a GitHub issue.
* Please contact Mutsumi Nakamura (mutsumi@asu.edu), and Mihir Parmar (mparmar3@asu.edu) for communication-related to LogicAttack.
