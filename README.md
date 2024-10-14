# are-you-my-mother
This repo contains my final project for the University of Colorado, Boulder class CSCA 5642: Introduction to Deep Learning. I was inspired by the classic children's book "Are You My Mother?" (You can read it in PDF format here; it's very short.) In this story, a baby bird loses track of its mother and approaches various members of its community — a kitten, a hen, a dog, a cow, a boat, a plane and a digger — asking each, "Are you my mother?" Eventually it finds its mother again and all is well.

This little bird could have saved itself some trouble with a neural network trained on birds!

So that's what I'd like to create. My goal is to build a model that, given two input images — one of a baby bird, one of anything else — can make two predictions.

First, it will predict whether the second photo is of a bird. If not, it will tell the baby bird the second photo is not its mother.

Second, if the second photo is determined to be a bird, it will predict whether it is the same kind as the baby bird, and thus could be its mother. This second step is necessary because in the text, one of the potential mothers the baby bird approached was a hen. That's a bird, but not the right kind.

I will use two datasets to train this model. The first is a great, very large and well labeled dataset of male, female and juvenile birds from the Cornell Lab of Ornithology, available here. This will help our model in its second step of determining whether a baby and adult bird are the same kind.

The model will also need some training images of things other than birds to help with its first step — determining whether the second input image is even a bird at all. I'll use the well-known CIFAR 100 dataset from the University of Toronto for this task. A big advantage of this dataset is that its 20 superclasses of image types include lots of reasonable proxies for the kinds of non-birds the baby bird in the story approaches, but it does not include birds, so I won't have to find and exclude them.
