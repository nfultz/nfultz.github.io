[Deep Learning](http://www.deeplearningbook.org/)

So what is the magic that separates deep learning from the rest, and can crack problems for which no group of humans has ever been able to program a solution? The first ingredient, from the early days of neural nets, is a timeless algorithm, rediscovered again and again, known in this field as "back-propagation". It's really just the chain rule—a simple calculus trick—applied in a very elegant way. It's a deep integration of continuous and discrete math, enabling complex families of potential solutions to be autonomously improved with vector calculus.



The key is to organize the template of potential solutions as a directed graph (e.g., from a photo to a generated caption, with many nodes in between). Traversing this graph in reverse enables the algorithm to automatically compute a "gradient vector," which directs the search for increasingly better solutions. You have to squint at most modern deep learning techniques to see any structural similarity to traditional neural networks, but behind the scenes, this back-propagation algorithm is crucial to both old and new architectures.



But the original neural networks that used back-propagation fall far short of newer deep learning techniques, even using today's hardware and datasets. The other key piece of magic in every modern architecture is another deceptively simple idea: components of a network can be used in more than one place at the same time. As the network is optimized, every copy of each component is forced to stay identical (this idea is called "weight-tying"). This enforces an additional requirement on weight-tied components: they must learn to be useful in many places all at once, and not specialize to a particular location. Weight-tying causes the network to learn a more generally useful function, since a word might appear at any location in a block of text, or a physical object might appear at any place in an image.



 --- [Edge.org](http://edge.org/response-detail/26794)

[Extending "Let It Go" with LSTM](http://elnn.snucse.org/sandbox/music-rnn/#hn)

[Deep Learning for Beginners](http://randomekek.github.io/deep/deeplearning.html)

[Neural Networks in Javascript](http://blog.webkid.io/neural-networks-in-javascript/)

[Understanding LSTM Networks -- colah's blog](http://colah.github.io/posts/2015-08-Understanding-LSTMs/)

[Deep Learning with MXNetR](http://dmlc.ml/rstats/2015/11/03/training-deep-net-with-R.html)

[A Neural Network in 11 lines of Python (Part 1) - i am trask](http://iamtrask.github.io/2015/07/12/basic-python-network/)

[Self-Organizing Maps with Google’s TensorFlow | Sachin Joglekar's blog](https://codesachin.wordpress.com/2015/11/28/self-organizing-maps-with-googles-tensorflow/)

The earliest deep-learning-like algorithms that had multiple layers of non-linear features can be traced back to Ivakhnenko and Lapa in 1965 (Figure 1), who used thin but deep models with polynomial activation functions which they analyzed with statistical methods. In each layer, they selected the best features through statistical methods and forwarded them to the next layer. They did not use backpropagation to train their network end-to-end but used layer-by-layer least squares fitting where previous layers were independently fitted from later layers. --- [Deep Learning in a Nutshell: History and Training | Parallel Forall](http://devblogs.nvidia.com/parallelforall/deep-learning-nutshell-history-training/)





LIBFFM is an open source tool for field-aware factorization machines (FFM). For the formulation of FFM, please see this slide. It has been used to win two recent click-through rate prediction competitions (Criteo's and Avazu's).



It supports



    l2-regularized logistic loss



Main features include



    using SSE instructions to accelerate vector operations

    cross validation for parameter selection  --- [LIBFFM: A Library for Field-aware Factorization Machines](http://www.csie.ntu.edu.tw/~r01922136/libffm/)

[TensorFlow whitepaper](http://download.tensorflow.org/paper/whitepaper2015.pdf)

[ Neural Networks with Few Multiplications](http://arxiv.org/abs/1510.03009)

Deep learning is part of a broader family of machine learning methods based on learning representations of data. [wikipedia](https://en.wikipedia.org/wiki/Deep_learning)

[Neural Turing Machines FAQ – when trees fall…](https://blog.wtf.sg/2015/01/15/neural-turing-machines-faq/)

[Time Travel in Deep Learning Space: An Introduction to Deep Learning Models and How Deep Learning Models Evolved from the Initial Ideas](http://arxiv.org/abs/1510.04781v1)

[Deep Learning for Visual Question Answering](https://avisingh599.github.io/deeplearning/visual-qa/)

[26 Things I Learned in the Deep Learning Summer School - Marek Rei](http://www.marekrei.com/blog/26-things-i-learned-in-the-deep-learning-summer-school/)

[Deeplearning4j - Using Neural Networks With Regression](http://deeplearning4j.org/linear-regression.html)

[ Towards universal neural nets: Gibbs machines and ACE](http://arxiv.org/abs/1508.06585)

[What's Wrong With Deep Learning?](https://docs.google.com/file/d/0BxKBnD5y2M8NVHRiVXBnOVpiYUk/view?sle=true)

"Realistically, deep learning is only part of the larger challenge of building intelligent machines. Such techniques lack ways of representing causal relationships (...) have no obvious ways of performing logical inferences, and they are also still a long way from integrating abstract knowledge, such as information about what objects are, what they are for, and how they are typically used. The most powerful A.I. systems, like Watson (...) use techniques like deep learning as just one element in a very complicated ensemble of techniques, ranging from the statistical technique of Bayesian inference to deductive reasoning." - Gary Marcus

[Generating Magic cards using deep, recursive neural networks - Custom Card Creation - Creativity - MTG Salvation Forums - MTG Salvation](http://www.mtgsalvation.com/forums/creativity/custom-card-creation/612057-generating-magic-cards-using-deep-recursive-neural)

Was deep learning the cause of [[Foul-mouthed Watson]]?

[Alex Korbonits: Deep Learning with Python: getting started and getting from ideas to insights in mi - YouTube](https://www.youtube.com/watch?v=MVyauNNinC0)

[Deep Learning via Hessian-free Optimization | GitXiv](http://gitxiv.com/posts/v5tX6rgdXs9Fqo63r/deep-learning-via-hessian-free-optimization)

[Hacker's guide to Neural Networks](https://karpathy.github.io/neuralnets/)

[Deeplearning4j - Open-source, distributed deep learning for the JVM](http://deeplearning4j.org/restrictedboltzmannmachine.html)

[DEEP LEARNING](http://www-labs.iro.umontreal.ca/~bengioy/dlbook/)

[Critique of Paper by "Deep Learning Conspiracy" (Nature 521 p 436) Machine…](https://plus.google.com/100849856540000067209/posts/9BDtGwCDL7D)

