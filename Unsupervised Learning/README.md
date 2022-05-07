# Unsupervised learning

Unsupervised learning is a type of algorithm that learns patterns from untagged data. The hope is that through mimicry, which is an important mode of learning in people, the machine is forced to build a compact internal representation of its world and then generate imaginative content from it. In contrast to [supervised learning](https://en.wikipedia.org/wiki/Supervised_learning) where data is tagged by an expert, e.g. as a &quot;ball&quot; or &quot;fish&quot;, unsupervised methods exhibit self-organization that captures patterns as probability densities [[1]](https://en.wikipedia.org/wiki/Unsupervised_learning#cite_note-Hinton99a-1) or a combination of neural feature preferences. The other levels in the supervision spectrum are [reinforcement learning](https://en.wikipedia.org/wiki/Reinforcement_learning) where the machine is given only a numerical performance score as guidance, and [semi-supervised learning](https://en.wikipedia.org/wiki/Semi-supervised_learning) where a smaller portion of the data is tagged. Two broad methods in Unsupervised Learning are Neural Networks and Probabilistic Methods.

## **Neural works**

Tasks vs Methods

Neural network tasks are often categorized as discriminative (recognition) or generative (imagination). Often but not always, discriminative tasks use supervised methods and generative tasks use unsupervised (see Venn diagram); however, the separation is very hazy. For example, object recognition favors supervised learning but unsupervised learning can also cluster objects into groups. Furthermore, as progress marches onward some tasks employ both methods, and some tasks swing from one to another. For example, image recognition started off as heavily supervised, but became hybrid by employing unsupervised pre-training, and then moved towards supervision again with the advent of dropout, relu, and adaptive learning rates.

Training

During the learning phase, an unsupervised network tries to mimic the data it&#39;s given and uses the error in its mimicked output to correct itself (ie. correct its weights &amp; biases). This resembles the mimicry behavior of children as they learn a language. Sometimes the error is expressed as a low probability that the erroneous output occurs, or it might be expressed as an unstable high energy state in the network.

In contrast to Supervised method&#39;s dominant use of Backpropagation, Unsupervised Learning also employ other methods including: Hopfield learning rule, Boltzmann learning rule, Contrastive Divergence, Wake Sleep, Variational Inference, Maximum Likelihood, Maximum A Posteriori, Gibbs Sampling, and backpropagating reconstruction errors or hidden state reparameterizations. See the table below for more details.

Energy

An energy function is a macroscopic measure of a network&#39;s activation state. In Boltzmann machines, it plays the role of the Cost function. This analogy with physics is inspired by Ludwig Boltzmann&#39;s analysis of a gas&#39; macroscopic energy from the microscopic probabilities of particle motion p {\displaystyle \propto } ![Shape1](RackMultipart20220507-1-gpoazl_html_49ac0cb03196381.gif)  eE/kT, where k is the Boltzmann constant and T is temperature. In the RBM network the relation is p = e−E / Z,[[2]](https://en.wikipedia.org/wiki/Unsupervised_learning#cite_note-Hinton2010-2) where p &amp; E vary over every possible activation pattern and Z = {\displaystyle \sum \_{AllPatterns}} ![Shape2](RackMultipart20220507-1-gpoazl_html_49ac0cb03196381.gif)  e -E(pattern). To be more precise, p(a) = e-E(a) / Z, where a is an activation pattern of all neurons (visible and hidden). Hence, early neural networks bear the name Boltzmann Machine. Paul Smolensky calls -E the Harmony. A network seeks low energy which is high Harmony.

![](RackMultipart20220507-1-gpoazl_html_6c3c8e69bede05ec.png)

![image](https://user-images.githubusercontent.com/101298565/167270377-0f8af717-d514-44c9-9b42-bb49723e167c.png)
