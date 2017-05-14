## Know the history for successful data curation

2017-5-14

Knowing very little about medical science, I skipped data curation. The idea was to download all wikimedia articles about health and medicine to make a machine learning model. In total there were roughly 11,000 articles. I removed some punctuation and wiki markdown code where possible. Then I combined all articles into a single file. The file was feed to the word2vec model available on the TensorFlow GitHub. Using GPU training and minor hyperparameter optimization, the following was a part of the T-SNE output.

![medical-tsne-plot](https://github.com/EddieOne/medlayer/blob/master/medical-tsne.png?raw=true)

This was my first clue that religions have a colorful history in medical science. After more investigation it became clear that many religious organizations have been active in many areas of health and medicine. Some information was supplemental and through time has been replaced by more accurate knowledge. More, there was non-religious pseudoscience and fictional medicine articles that were fun but lacking usefulness. In addition, conspiracy theories were removed from the training data. The commonality is that medical science is iterative. The information is all time sensitive and false information is likely in need of separate modeling.
