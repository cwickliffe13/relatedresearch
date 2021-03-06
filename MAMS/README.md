# Multi-agent MicroServices

## 2019

### Collier, et al.

- [MAMS: Multi-Agent MicroServices](Collier_2019.pdf)

   [Collier](https://people.ucd.ie/rem.collier/), [O'Neill](https://people.ucd.ie/eoin.oneill/), [O’Hare](https://people.ucd.ie/gregory.ohare/), and [Lillis](https://people.ucd.ie/david.lillis/) demonstrate, in their article,the integration of agent technology into microservices-based systems by leveraging on the similarities between agents and microservices approaches.  Following close similarities underlying the design principles of both multi-agent systems and microservices, the authors propose a class of system comprising Plain-Old MircroServices (POMS) and Agent-Oriented MicroServices (AOMS): MAMS. The authors use the Organization as a Service (OaaS) model to conceptualize the design and operation of the proposed MAMS framework. Through the model, the authors introduce the idea of reusable components of a larger microservices architecture where AOMS would provide standardized implementations of common organizational structures and auctions. The adopted OaaS model dictates the internal mechanism of implementations to use agents, whereas the external interface is realized as a set of Representational State Transfers (REST) resources, allowing both AOMS and POMS to use them. The MAMS concept, developed through the illustration of the Vickery auction as a service, in the article, demonstrates seamless exposure of agents’ internal states and inboxes as resources to traditional microservices, through a REST API interaction. The REST API interactions are supported by the ASTRA Message Service tool and the [FIPA-ACL](http://www.fipa.org/repository/aclspecs.html)  messaging to expose agents’ virtual resources as well as inboxes. The proposed MAMS model adapted the ASTRA programming language to support the creation of virtual resources and FIPA-ACL based communication via RESTful inboxes. That means the MAMS model builds an internal network of resources (States of agents and agent inboxes) supported by Agent communication language as well as ASTRA Message Service, and links the internal resources marked ‘public’ and identified through a globally unique Uniform Resource Identifier to the external entities (microservices) via RESTful inboxes. To make the developed MAMS framework consistent with the [Continuous Integration/Continuous Delivery model](https://en.wikipedia.org/wiki/CI/CD) characterizing microservices-based approaches, the authors restructured ASTRA into a set of Maven artifacts by re-engineering the ASTRA compiler to work as part of a Maven Plugin that can be easily integrated into its build lifecycle.  

   - **Key Takeaways:** 
   •	The illustrated MAMS can be used seamlessly by other microservices. This can be easily extended to include external agents through the use of FIPA-ACL and public inboxes.
•	The illustrated MAMS structure adapts the OaaS model, which dictates the internal mechanism of implementations to use agents, whereas the external interface is realized as a set of Representational State Transfers (REST) resources, allowing both AOMS and POMS to use them.
•	The proposed MAMS model adapted the ASTRA programming language to support the creation of virtual resources and FIPA-ACL based communication via RESTful inboxes.
•	The proposed MAMS model compels re-engineering of the ASTRA compiler, used to create virtual resources, to conform to the Continuous Integration/Continuous Delivery model characterizing microservices-based approaches
•	Even though the demonstrated MAMS model majors on the similarities of the principles characterizing both agents and microservices, certain inconsistent aspects like the bounded context of agents interfere with their mobile interaction with microservices, because agents are bound to a specific Uniform Resource Identifier.

   - **What can go wrong:**
  The association of every agent resource with a globally unique URL limits the mobility of agents, thus hindering the extent of interaction with microservice requests. The redirection process increases run-time, which may lead to delays in the case of multiple concurrent requests. Delays can also emanate from transaction limits set on a particular MAMS platform.
   - **What to look out for:** 
   •	Embracing Web models to provide a simple decentralized global unique naming system for agents can act as a basis for driving new decentralized approaches to build MAS.
•	The demonstrated MAMS framework is an essential step in achieving a longer-term goal of realizing Hypermedia MAS: agent-based systems that can discover, consume and integrate hypermedia services that act as an enabler for Semantic Web and Linked Data systems.

  - **Why the structure is superior:** 
 •	The MAMS approach presents a framework that can be used seamlessly by other microservices and can be easily extended to include external agents through the use of FIPA-ACL and public inboxes.
•	The MAMS approach provides a library of reusable solutions that other auctions and organizational mechanisms can adapt. 
•	The MAMS structure offers secure solutions by only exposing agents that need to interact with external systems. 
•	The alignment of MAMS deployment with industry best practice allows developers to leverage on a wide range of industry-standard tools and components available to microservices-based systems.
•	The implementation strategy and concrete agent technologies are well defined in the demonstrated MAMS structure. 
•	The demonstrated MAMS framework is made consistent, through re-engineering of the ASTRA compiler, with the Continuous Integration/Continuous Delivery model, which characterizes microservices-based approaches



### Pump, et al.

- [Applying Microservice Principles to Simulation Tools](Pump_2019.pdf)

- Authors: Richard Pump, [Arne Koschel](https://www.hs-hannover.de/service/personenfinder/person/1000003410/), [Volker Ahlers](http://www.volkerahlers.de/)

Microservices are a type of software development in which applications are arranged as loosely coupled services which are fine-grained with lightweight protocols.  The advantages of microservices include working well at scale, and rapid development of new components.  However, microservices often entails creating an entirely new architecture and replacing an old system with a piecemeal re-implementation. As a result, pure microservices architectures are not feasible in every project.  Instead, in this study, microservice principles were used to prototype architecture for the connection of two widely-used simulation tools in the context of urban transport simulation (MATSim and AnyLogic).  The proposed system uses microservice principles to combine the two tools into a single tool supporting civil engineer decision-making on innovative urban transport concepts.  This approach improved the usability of complex software and allowed developers to develop parts of the software independently, in conformation to the project's organizational structure which was geographically located in different places.

   - **Challenges of microservices and, specifically, this approach:** 
   
      - Microsimulations rely on monolithic simulation frameworks, and modeling only small parts of the scenario still requires a rich framework to provide the extensive functionalities needed.
      
      - One of the challenges in microservices is that rebuilding systems to adhere to microservices architecture can be very time consuming and likely costly.  The approach outlined in this study modeled only small parts of the scenario with microservices principles, and did not rebuild the scenario in a full microservices architecture, which made it possible to use fewer resources. 

      -  Another challenge was that this study featured multiple teams building the system in different physical locations, so independence was a paramount factor.  Existing applications were split up within the boundaries of the project, which was made easier due to the microservices approach which emphasizes modularity.

      - Complexity of simulations adds difficulty.  The approach outlined in this paper only works for simulations which are not very complex; very complex simulations can usually not be written by a small team in a reasonable time frame.
  

  - **Advantages of microservices and this specific approach:** 
      - This approach combined two simulation frameworks to create a unified front end, which made the software more usable.
      - Usage of microsimulations allows rapid technical development of new simulations, reducing
overall development time.
      -	Simulation accuracy is increased -- by reducing the time needed for technical development, more time can be dedicated to detailed research and data gathering about real-life behavior and structure.
      -	Keeping simulation scenarios small can help reduce the number of people needed to implement software, which can be a big advantage in cases where the software is to be used as a tool in a given project.  If the concepts modeled are kept to a small number and parameters are used for configuration scenarios, the amount of code needed is actually minimal.
      -	This framework may be potentially used in the cloud, which is the subject of future work by this research group.
