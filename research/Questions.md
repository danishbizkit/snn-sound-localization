
# Questions & challenges


## Modelling questions / aims

Starting point:

* What are the best strategies for localising sounds with a spiking neural network?
* Can we train networks end-to-end to perform as well or better than hand-crafted solutions?
  - _Danish_: I have some preliminary work on this which I would like to extend.
* Can we understand what these trained networks are doing in a high level way?
  - _Dan_: I'm going to try out a few ideas for this.
* Do these networks do something similar to what has been proposed in the literature (labelled line models, hemispheric models, pattern match decoders) or something completely different?
* Do different optimal models emerge in different parameter regimes (head size, signal to noise ratio, multiple sound sources)?
  - _Danish_: I have some preliminary results with computational studies of head size vs processing in the auditory periphery that could be applicable.
* How do the results depend on the neuron model and available dynamics? For example, does adaptation matter and in which conditions?
  - _Alberto_: I'm interested into looking at this (neuron and synapse model, plasticity).
  - _Danish_: I'm also interested in looking at this from the plasticity and spatial working memory perspectives. I am looking into neural models combining plasticity and working memory that could be interesting to apply here.


## Technical challenges

* Delay learning: can we train delays with surrogate gradient descent?
* Alternatives to surrogate gradient descent?
  - _Danish_: I'm working with neuron models with temporal correlation-based plasticity rules, which in principle could capture delays.
* Add a more realistic auditory periphery (cochlear filtering and more realistic spiking model).
  - _Danish_: I have a simple biophysical model of auditory periphery that I can apply quickly.
* Number of time steps might be an issue for a more realistic model. May want to use dt=0.1ms and duration>=100ms so more than 1000 time steps.
* Add a more realistic sound localisation task (natural sounds, background noise, multiple sound sources).
  - _Tomas_: experiment with this, starting with multi-frequency sounds
* Consider multiple architectures, potentially matching the auditory system.
* Consider more complicated neuron models and perhaps make some of these neuron model parameters trainable; for what situations can that help?
  - _Danish_: I'm working with neuron models with temporal correlation-based plasticity rules, which in principle could capture ITD cues.
* How to understand what the learned network does?
* Use regression instead of classification
* Which level of biological realisms does the learning need to comply to? Which observables are available at the synapse as input to a learning rule?
