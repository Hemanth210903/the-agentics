# CrewAI Build Report

**Name:** Hemanth Sai Bellam  
**Topic I used:** Retrieval-Augmented Generation (RAG)

## 1. What I changed

I changed the Writer agent's backstory in `main.py`. In the original version, the Writer followed the instructions already provided by the starter kit. For my second run, I changed the backstory so the Writer would explain difficult ideas to a 10-year-old student using simple words, familiar examples, and short sentences. I chose this change because I wanted to see how changing an agent's instructions could affect the final output without changing the topic or the overall workflow. I kept the topic, retrieval-augmented generation, the same in both runs so I could compare the results. This was a small change, but it was intended to make the explanation easier for a beginner to understand.

## 2. How CrewAI works

CrewAI organizes work using agents, tasks, and a crew. An agent has a role, a goal, and a backstory that guide how it approaches its work. A task tells an agent what it needs to accomplish and describes the expected output. The crew brings the agents and tasks together into a workflow.

In my project, the research agent works on gathering and organizing information about retrieval-augmented generation. The Writer then uses the task instructions and research results to create the explanation. The model generates the content based on its learned information and the instructions it receives. When I changed the Writer's backstory, I changed the guidance for how the Writer should communicate. This can affect the vocabulary, examples, and level of detail in the final explanation. I kept the topic the same so that I could focus on the effect of this instruction change. The two output files provide evidence for comparing the original and changed behavior.

## 3. Evidence

I saved the original terminal output in `run1_original.txt` and the original explanation in `explainer_run1.md`. I saved the changed terminal output in `run2_changed.txt` and the new explanation in `explainer_run2.md`. I will compare the two explanations to see whether the second version uses simpler words, shorter sentences, and more familiar examples. One thing I noticed during the process was: **[describe a real issue or surprise from your runs, such as a temporary model error or retry, if it happened].** I addressed it by **[explain what you actually did].**

## 4. Choosing a framework

I would choose CrewAI for a project where several specialized agents need to complete different parts of a task. Its agent, task, and crew structure makes it straightforward to assign research and writing responsibilities. For example, a project that creates a report could use one agent to research a topic and another to turn the research into a readable explanation.

LangGraph is another framework I practiced. Compared with CrewAI, LangGraph is useful when I need more explicit control over the steps and transitions in a workflow. It can be a good choice when a process needs conditional paths, state management, or repeated steps. CrewAI felt suitable for this assignment because the workflow was organized around agents with clear roles and tasks. LangGraph can require more work to define the graph and state, while CrewAI offers a direct way to organize role-based collaboration. I would choose between them based on whether the project needs a simple team of agents or more detailed control over the workflow.

## 5. Verification and AI use

I checked that the CrewAI program ran and produced an explanation file for each run. I also planned to compare `explainer_run1.md` and `explainer_run2.md` to check whether the changed instructions affected the writing style. The generated text comes from the language model's learned information, and the starter kit does not browse the web to verify facts. Therefore, a successful run does not guarantee that every statement is correct; important technical claims should be checked against reliable documentation. I used ChatGPT to help me understand the assignment steps, make the Writer backstory change, and prepare this report draft. I will review the report against my actual code and output files before submitting it.