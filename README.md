Chance discovery is all about discovering something new. Its objective is to find chances or breaking events from documents. It produces ideas and input into the creative process of identifying business opportunities.

In this project, I used a dataset of AI tool descriptions from Futurepedia (futurepedia.io). Futurepedia is organized 
into categories. The tools in this dataset are all from the customer support category. The goal is to identify chances that discuss ideas for new AI tools.


![graph html1](https://github.com/abibatoki/ChanceDiscovery/assets/149620766/362ec3c3-4c10-4433-90dc-fe97c72087a7)
Fig 1: M = 30, k = 12

where M is the most frequent terms in the document
K is the link between bridging terms and clusters

Figure 1 is an opportunity graph made with the keygraph algorithm, a technique based on word co-occurrence at the sentence level. It captures the context in which words occur.

The black nodes represent well-established ideas or concepts. The red nodes introduce novel or emerging ideas as connections between them.
The opportunity graph is not ready to be interpreted because the clusters and the bridging terms are not linked.

#Adding “customer” and “support” as stopwords

![graph html2](https://github.com/abibatoki/ChanceDiscovery/assets/149620766/23088ec1-2543-4bb3-a2f3-04fc0d0129f3)

Fig 2: M = 30, K = 12

"customer" and "support" were added as stopwords because all tools in this category are to provide customer support.
The updated opportunity graph is now easier to interpret because there are four clusters, each with a bridging term connecting them to the central idea ‘ai’. Cluster1: {chatbot, chatgpt, user, website}, its bridging term is ‘answer’, Cluster2: {platform, chatbots,
business}, its bridging term is ‘sale’, Cluster3: {service, provide, ai}, its bridging term is 'response', and Cluster4: {ai, tool}, its bridging term is 'design'.

#Remowing "ai" and "tools" because they are common words in a database on AI tools.


![graph html3](https://github.com/abibatoki/ChanceDiscovery/assets/149620766/7f6fbe99-3be8-4a13-bd9c-3f08cdd2dd21)

Fig 3: M = 30, K = 12

By removing "ai" and "tools", we now have about six clusters and a bridging term ‘train’ connected to two clusters: clusters 2 & 3.
Cluster1: {ai-powered, business, conversational}
Cluster2: {enable, chatbot, platform, provide, insight}
Cluster3: {tool, chatbots, service, response}
Cluster4: {ai-powered, chatbot, tool, design}
Cluster5: {business, platform, chatbots, tool}
Cluster6: {business, provide, response, time}

#Identifying the verbs among the black nodes and the most central one.

The verbs are create, enable, design, provide, and answer. The most central is ‘Provide’.
Using the concordance tool, the word ‘provide’ adds insight into the capability of the AI tool (chatbot)

#Remove 'Provide' and describe the impact on the graph

![graph html4](https://github.com/abibatoki/ChanceDiscovery/assets/149620766/c191de4f-3c08-4397-9ec3-c119663979bd)

Fig 4: M = 30, K = 12

After removing the word ‘provide’, we now have four verbs among the black node: create, enable, answer, and design. Two verbs among the red nodes: improve and enhance. One noun among the black node (insight) is lost, while one noun (satisfaction) is added to the red node.

#Reducing M from 30 to 25

![graph html5](https://github.com/abibatoki/ChanceDiscovery/assets/149620766/4e0aa4a9-de3d-48bf-9767-2adc6d81ce47)

Fig 5: M = 25, K = 12

#Evaluation and Interpretation of Fig 5
Cluster labels and words associated with each

![image](https://github.com/abibatoki/ChanceDiscovery/assets/149620766/41b854ed-93ee-4252-9727-ff83cdd8a491)

#Identify potential chances and the clusters they connect. Discard any chances that do not discuss ideas for new AI tools.

‘chat’ and ‘assistant’ were discarded because:

(i) They were connected to only one cluster

(ii) They are expected to be common words in a database on chatbot

(iii) They did not discuss ideas for a new AI tool

‘knowledge’ and ‘base’ were interpreted as ‘knowledge-base’ because they were used in the same context.

![image](https://github.com/abibatoki/ChanceDiscovery/assets/149620766/ec7bff90-ec16-45d7-a722-8b7ab04facc8)

#Table of chances and scenario descriptions

![image](https://github.com/abibatoki/ChanceDiscovery/assets/149620766/3434c364-08f0-4f74-b697-e10f1dc40ed6)

#Process used to create the scenarios using the concordance of the bridge word

Scenario 1: ‘train’ is a bridge word connecting website, service, and enable. Its concordance talks about a platform that allows businesses to train their chatbot.

Scenario 2: ‘knowledge-base’ is a bridge word connecting website, service, and enable. Its concordance talks about a support tool powered by the company’s knowledge base.

Scenario 3: ‘boost’ is a bridge word connecting website and enable. Its concordance talks about enhancing customer interaction leading to improved productivity.

Scenario 4: ‘offer’ is a bridge word connecting enable and chatbot. Its concordance talks about offering the ideal customer experience.

In summary, we looked at the clusters connected to the bridge term and the context in which the bridge term was used before coming up with our scenarios.

#Ranking the scenarios by confidence and their potential

Knowledge base (high) - Having a robust knowledge base is foundational to any AI chatbot service. This ensures that the chatbot can provide accurate, reliable, and relevant information to users' inquiries. Without a knowledge base, the chatbot might not be able to give any responses at all, or the responses could be inaccurate or irrelevant, which would undermine the user's trust in the tool. Moreover, a knowledge base grounded in the company’s specifics (like FAQs or proprietary data) ensures that the chatbot's responses are tailored to the context of the business and its customers.

Train (high) - Customizing the chatbot with the company's data is crucial for providing personalized and context-aware responses. Training with specific datasets allows the chatbot to understand the nuances of the company's offerings, language, and customer interactions. This is a significant step up from generic LLMs because it can grasp and reflect the company's unique value proposition, culture, and customer service approach.

Boost (medium) - Connecting the chatbot to a large language model like ChatGPT can greatly enhance its conversational capabilities, making the interactions more fluid, natural, and varied. This can be a game-changer in terms of user experience because it can handle a wider range of queries with more sophisticated dialogue, and it can learn from interactions to improve over time. However, this is ranked third because, without a strong knowledge base and training, even a powerful LLM can fall short in delivering high-quality, context-specific assistance.

Offer (low) - Providing a good user experience is certainly important, but it is somewhat of a broader and more subjective goal compared to the other scenarios. It is the result of effectively implementing the above aspects (knowledge base, training, and boost). While it is the ultimate aim, the specifics of how to achieve a good user experience can vary greatly and are influenced by the successful implementation of the other three scenarios. This is why it's ranked last - not because it's unimportant, but because it's an outcome of the other three scenarios being executed well.

In summary, the importance of these scenarios is based on how foundational they are to the creation of a new AI tool. A knowledge base provides the essential data upon which the AI operates; training ensures that the responses are customized and relevant; the boost from an LLM enhances conversational capabilities; and the offer of a good user experience is the culmination of implementing the first three effectively.







