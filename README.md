# ChanceDiscovery
Chance discovery is all about discovering something new. Its objective is to find chances or breaking events from documents. It produces ideas and input into the creative process of identifying business opportunities.


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



