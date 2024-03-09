**Background:**
* Using [1hr Talk Intro to Large Language Models](https://www.youtube.com/@AndrejKarpathy) to start learning about LLMs

**Notes:**
* LLM -> Large Language Model
* Dipartite Architecture (fully contained architecture):
	1. Parameters file (data stored in a 'lossy' compression format)
	2. Run file (program logic)
* Reference [[Llama 2]] as Meta's Open-Source Reference
* Logistics of the Program:
	* *Running* the program is (computationally expensive), but easy to do
	* *Setting Parameters* is an extremely involved process
* Parameter Training:
	* Take ~10TB of text from the internet
	* Procure GPU cluster (~6000 GPUs)
	* Process data for ~12 DAYS
* Neural Network:
		![[Next Word Neural Network.png]]
	* Next word prediction neural network ([[Transformer]])
		* Next word prediction forces the NN to learn a lot *about* the world *in general*
		![[LLM Transformer.png]]
		* Limitations: it seems these models don't have logical intuition (IE, can tell you Tom Cruise's Mom, but gets confused when asked who Mary Lee Pfeiffer's son is). Can't always synthesize the correct answer from the data it knows. It seems to be a 'directional' knowledge
	* Training the assistant:
		* Continue training with lots of text, but train using user/assistant prompts
		* Training is exactly the same, just change the training set
	* High-level training stages:
		1. Training using high-quantity low-quality internet data
		2. Training using low-quantity high-quality procured data
		![[LLM Training Stages.png]]