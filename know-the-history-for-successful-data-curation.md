## Know the history for successful data curation

2017-5-14

Knowing very little about medical science, I skipped data curation. The idea was to download all wikimedia articles about health and medicine to make a machine learning model. In total there were roughly 11,000 articles. I removed some punctuation and wiki markdown code where possible. Then I combined all articles into a single file. The file was fed to the [Skipgram word2vec model][1] available on the TensorFlow GitHub. Using [GPU training][2] and minor hyperparameter optimization, the following was a created from part of the T-SNE result.

![medical-tsne-plot](https://github.com/EddieOne/medlayer/blob/master/medical-tsne.png?raw=true)

This was my first clue that religions have a colorful history in medical science. After more investigation it became clear that many religious organizations have been active in many areas of health and medicine. Some information was supplemental and throughout time has been replaced by more accurate knowledge. More, there was non-religious pseudoscience and [fictional medicine][3] articles that were fun but lacking usefulness. In addition, conspiracy theories were removed from the training data. The commonality is that medical science is all time sensitive. To overcome the problem of poor data, curation is needed in the short term. In the long term, a seperate model may be needed to classify old and fake information.

[1]: https://github.com/tensorflow/tensorflow/blob/master/tensorflow/examples/tutorials/word2vec/word2vec_basic.py
[2]: https://www.youtube.com/edit?o=U&video_id=ePVmMGkpka8
