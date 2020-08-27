# Supervised learning
- Supervised learning addresses the task of predicting targets given inputs.
	- The targets, which we often call labels, are generally denoted by **y**.
	- The input data, also called the features or covariates, are typically denoted **x**.
	- Each (input, target) pair is called an example or instance.
		- We denote any particular instance with a subscript, typically **i**, for instance (x<sub>i</sub> , y<sub>i</sub>).

## Regression
- A good rule of thumb is that any How much? or How many? problem should suggest regression.
	- **How many hours will this surgery take?**: regression
	- **How many dogs are in this photo?**: regression.

## Classification
- In classification, we want our model to look at a feature vector, e.g., the pixel values in an image, and then predict which category (formally called classes), among some (discrete) set of options, an example belongs.
	- For hand-written digits, we might have 10 classes, corresponding to the digits 0 through 9.
	The simplest form of classification is when there are only two classes, a problem which we call binary classification.
	- For example, our dataset X could consist of images of animals and our labels Y might be the classes {cat, dog}.
- When we have more than two possible classes, we call the problem **multiclass classification**.
	- Common examples include hand-written character recognition [0, 1, 2, 3 ... 9, a, b, c, ...].

## Tagging
- The problem of learning to predict classes that are not mutually exclusive is called multi-label classification.

## Search and ranking
- Take web search for example, the goal is less to determine whether a particular page is relevant for a query, but rather, which one of the plethora of search results is most relevant for a particular user.

## Recommender systems
- Recommender systems are another problem setting that is related to search and ranking.
	- The problems are similar insofar as the goal is to display a set of relevant items to the user.
	- The main difference is the emphasis on **personalization to specific users** in the context of recommender systems.

## Sequence Learning
- They require a model to either ingest sequences of inputs or to emit sequences of outputs (or both!).
	- These latter problems are sometimes referred to as **seq2seq problems**.
		- Language translation is a seq2seq problem.
		- **Tagging and Parsing:** In general, the goal is to decompose and annotate text based on structural and grammatical assumptions to get some annotation.
		- **Automatic Speech Recognition:** With speech recognition, the input sequence **x** is an audio recording of a speaker, and the output **y** is the textual transcript of what the speaker said.
		- **Text to Speech:** Text-to-Speech (TTS) is the inverse of speech recognition. While it is easy for humans to recognize a bad audio file, this is not quite so trivial for computers.
		- **Machine Translation**

# Unsupervised learning
- It could be frustrating to work for a boss who has no idea what they want you to do.
	- The boss might just hand you a giant dump of data and tell you to do some data science with it!
		- This sounds vague because it is.
		- We call this class of problems unsupervised learning, and the type and number of questions we could ask is limited only by our creativity.
- Another important and exciting recent development in unsupervised learning is the **advent of generative adversarial networks (GANs)**.
	- These give us a procedural way to synthesize data, even complicated structured data like images and audio.
	- The statistical mechanisms are tests to check whether real and fake data are the same.