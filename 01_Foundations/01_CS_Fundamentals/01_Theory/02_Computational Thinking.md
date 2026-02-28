---
📖 book: Introduction to Computer Science (OpenStax)
📑 chapter: CH_02 - Computational Thinking
---
# Computational Thinking

> [!ABSTRACT] 🎯 Core Objectives
> - Define computational thinking
> - Discuss computational thinking examples
> - Describe how business solutions design heuristics and how patterns are used
> - Discuss the role of enterprise architecture (EA) and related architecture domains
> - Differentiate between enterprise and solution architecture
> - Analyze similarities between architectures and apply patterns
> - Discuss how to accelerate the creation of applications


## 🏗️ Concepts to Master
- Computational Thinking
- Computational Thinking Concepts
- Computational Thinking Techniques : Decomposition, Pattern Recognition, Abstraction, Algorithm

## ❓ Fundamental Problems & Questions
> [!QUESTION] 
> *What is computational thinking?  Why is computational thinking important ? How to think computationally ? How to use computational thinking in practice ?* 


## 📝 Lecture Synthesis

### 🧠 Concepts Analysis
> [!INFO] **Computational Thinking**
> - **Explanation of the concept**:  Computers can be used to help us solve problems. However, before a problem can be tackled, the problem itself and the ways in which it could be solved need to be understood. Computational thinking allows us to do this. It allows us to take a complex problem, understand what the problem is and develop possible solutions. We can then present these solutions in a way that a computer, a human, or both, can understand.
> - **Usage**: Computational thinking serves as the bridge between the problem and its resolution. It empowers solution designers to navigate the complexity of a given problem, separate its components, and formulate possible solutions. It involves breaking down complex problems into smaller, more manageable parts and devising systematic approaches to solve them. 

>[!INFO] *Computational Thinking Concepts*
>- **Decomposition**: The analytical process of breaking down complex concepts or problems into smaller parts.
>- **Pattern recognition** (logically organizing and analyzing data): to structure information in a way that facilitates effective problem-solving.
>- **Representing data through abstractions**: An **abstraction** is a simplified representation of complex systems or phenomena. Computational thinking involves representing data through an abstraction, such as a simulation, which uses models as surrogates for real systems.
>- **Automation** through algorithmic thinking: Using a program or computer application to perform repetitive tasks or calculations.
>- **Identification, analysis, and implementation of solutions**:  to achieve optimal efficiency and effectiveness through a combination of steps and resources.
>- **Generalization and transferability**: Generalizing and transferring this problem-solving process across a wide variety of problems showcases the adaptability and applicability of computational thinking.

>[!INFO] *Computational Thinking Techniques*
>There are four key techniques (cornerstones) to computational thinking:
>- **decomposition** : breaking down a complex problem or system into smaller, more manageable parts
>- **pattern recognition** : looking for similarities among and within problems
>- **abstraction** :  focusing on the important information only, ignoring irrelevant detail
>- **algorithms** : developing a step-by-step solution to the problem, or the rules to follow to solve the problem

>[!INFO] *Adaptive Design Reuse*
> While computational thinking commonly employs a bottom-up strategy for crafting well-structured components, adaptive design reuse adopts a top-down methodology, emphasizing the creation and assembly of business solutions by combining existing design components.
> - A **design componen**t is a reusable element within a larger system that serves a specific purpose.
> - A business **solution architecture** is a structural design that is meant to address the needs of prospective solution users.
> - An **architectural pattern** is a reusable solution to a recurring problem in software architecture design.
> - A **blueprint** is a detailed plan or design that outlines the structure, components, and specifications of a building, product, system, or process.



### 🔍 Key Retained Logic
> [!TIP] Synthesis
> A complex problem is one that, at first glance, we don't know how to solve easily.
> - Computational thinking involves taking that complex problem and breaking it down into a series of small, more manageable problems (**decomposition**). Each of these smaller problems can then be looked at individually, considering how similar problems have been solved previously (**pattern recognition**) and focusing only on the important details, while ignoring irrelevant information (**abstraction**). Next, simple steps or rules to solve each of the smaller problems can be designed (**algorithms**). Finally, these simple steps or rules are used to program a computer to help solve the complex problem in the best way.
>- Critical thinking is an important skill that can help with computational thinking. It boils down to understanding concepts rather than just mastering technical details for using software, prioritizing comprehension over rote learning. It’s a core skill, not an extra burden on a curriculum checklist, and it uniquely involves humans, not computers, blending problem-solving and critical thinking. Critical thinking focuses on ideas, not tangible items, applying advanced thinking to devise solutions. Critical thinking is essential for everyone and is, comparable to foundational abilities like reading, writing, and arithmetic.
>- In technology, data are represented at different levels of abstraction to simplify user interaction and manage complex operations efficiently.
>- An algorithm is a sequence of steps/instructions that must be followed in a specific order to solve a problem. Algorithms make it possible to describe a solution to a problem by writing down the instructions that are required to solve the problem. Computer programs typically execute algorithms to perform certain tasks. Algorithms are most commonly written as either ***pseudocode*** or a ***flowchart***.
>- **Algorithm Execution Model Patterns : Sequential, Parallel, Recursive**
>- Computational thinking and adaptive design reuse are simply methods used to bootstrap and/or accelerate the design of business solutions by providing a comprehensive set of methods for developing software solutions to business problems.
>- Two heuristics are inherent to the design of business solutions and the creation of business solution architectures. These heuristics are known as **layering** and **componentization**.
>- Layering  involves creating distinct layers that abstract specific aspects of the overall architecture. This heuristic enables the separation of concerns between layers and improves modularity. Each layer comprises components, and a layer may consist of multiple components. This hierarchical structure helps organize and separate different functionalities or responsibilities within the architecture, making it easier to manage and understand. 
>- Commonly, business solution architectures are organized into three main layers: the **presentation, business logic, and data management layers**. 
>- The **presentation layer** is the user’s touchpoint, handling the user interface (UI) and delivering the user experience (UX), which is the overall experience that a person has when interacting with a product, service, or system. 
>- The **business logic layer** holds the business logic for the business solution or application, separating the UI/UX from the business-centric computations. This separation affords the flexibility to adjust business operations as needs evolve without disrupting other system components.  
>- The **data management layer** is responsible for interacting with persistent storage systems like databases and various data processing mechanisms. 
>- In a layered architecture, information and commands flow through each layer, enhancing the design’s abstraction level, which denotes the granularity or detail at which a system is represented.

---