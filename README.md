# MConvKB

This repository introduces Multi-layered ConvKB (MConvKB), an extension of ConvKB the for Knowledge Graph completion task.

The two main changes are:
(i) we added non-linear fully connected layers motivated by VGG architectures which acts as the last layer classifier, and
(ii) we initialized the model with different pre-trained translational knowledge graph embeddings (TransE and TransD) to explore its effect in the model performance.

## Results

The model was evaluated on the RezoJDM16k dataset with the following results:

| **Model** | **MRR** | **MR** | **Hits@10** | **Hits@3** | **Hits@1** |
|-----------|---|---|---|---|---|
| TransE    | 0.179 | 203.31 | 0.432 | 0.242 | 0.041 |
| TransH    | 0.218 | 177.12 | 0.498 | 0.291 | 0.069 |
| TransD    | 0.208 | 186.19 | 0.474 | 0.278 | 0.064 |
| DistMult  | 0.220 | 194.47 | 0.445 | 0.252 | 0.109 |
| ComplEx   | 0.253 | 201.58 | 0.533 | 0.304 | 0.117 |
| ConvKB    | 0.218 | 186.65 | 0.493 | 0.275 | 0.078 |
| MConvKB   | 0.337 | 158.27 | 0.590 | 0.384 | 0.218 |

## References

ConvKB
```
@inproceedings{Nguyen2018,
  author={Dai Quoc Nguyen and Tu Dinh Nguyen and Dat Quoc Nguyen and Dinh Phung},
  title={A Novel Embedding Model for Knowledge Base Completion Based on Convolutional Neural Network},
  booktitle={Proceedings of the 16th Annual Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (NAACL-HLT)},
  pages={327--333},
  year={2018}
}
```

RezoJDM16K Dataset
```
@article{mirzapour2022,
  title={Introducing RezoJDM16k: a French Knowledge Graph DataSet for Link Prediction},
  author={Mirzapour, Mehdi and Ragheb, Waleed and Saeedizade, Mohammad Javad and Cousot, K{\'e}vin and Jacquenet, H{\'e}lene and Carbon, Lawrence and Lafourcade, Mathieu}
  booktitle={(Proceedings of the 13th Language Resources and Evaluation Conference (LREC)},
  year={2022}
}
```

