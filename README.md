# Codeflow-_-The-visusualizing-repository

Abstract
The rapid evolution of software engineering has given rise to increasingly complex 
codebases, often posing challenges in understanding the underlying logic, structure, and 
performance characteristics of large-scale systems. The process of navigating unfamiliar 
repositories, identifying functional components, and comprehending their operational 
behavior consumes a significant portion of a developer’s time. To address these concerns, 
this project introduces CodeFlo, an intelligent codebase visualization and performance 
analysis system that integrates traditional program analysis techniques with the reasoning 
capabilities of Large Language Models (LLMs). This system ingests open-source 
repositories, extracts code structure, visualizes control flow and method hierarchies, and uses 
an LLM-powered backend to evaluate time complexity, summarize code and imports, and 
detect potentially infinite loops. By combining static code parsing with LLM-enhanced 
semantic reasoning, CodeFlo bridges the gap between raw code and intuitive comprehension, 
enabling developers and researchers to accelerate onboarding, auditing, and optimization of 
software systems. 

Introduction 
The landscape of modern software development is characterized by a continual increase in 
repository size, code interdependencies, and modular complexity. With the proliferation of 
open-source contributions, developers often face the daunting task of understanding new or 
legacy codebases, which are rarely accompanied by comprehensive documentation. In such 
cases, the need for effective visualization tools and automated analytical techniques becomes 
essential. 
CodeFlo is a research and engineering effort aimed at streamlining codebase analysis by 
combining traditional parsing with generative reasoning offered by LLMs. The system is 
designed to assist developers in visualizing code structure through flow diagrams, understanding 
method-level operations, and identifying performance bottlenecks early in the development 
cycle. Unlike traditional parsers that rely solely on syntax trees and token analysis, CodeFlo 
leverages the Gemini LLM API to infer time complexity, summarize code and imports, and 
predict the likelihood of infinite loops within logical constructs. 
This project focuses on Java-based backend development and integrates technologies such as 
PostgreSQL, GitHub API, Java Swing GUI, and Gemini LLMs for semantic insights. The system 
presents a unique hybrid of conventional static analysis and intelligent reasoning, offering a 
scalable approach to intelligent code analysis and visual debugging.

Technology Used
The system architecture of CodeFlo is modular and extensible, combining traditional software 
engineering tools with modern AI services. 
The backend is built using Java and structured into packages that handle GitHub ingestion, 
database interaction, graphical rendering, and LLM-based reasoning. GitHub repositories are 
accessed using the kohsuke.github API, which enables seamless extraction of repository 
metadata and content. The extracted code files are parsed to retrieve their method structures, 
class hierarchies, and logical control flows. 
The storage layer uses PostgreSQL, with schema designs that normalize repositories, files, 
methods, and visualizations. The DatabaseManager class manages all queries, including table 
creation, insertion, and retrieval. 
To visualize the extracted code structure, Java Swing and AWT are employed for their 
lightweight, platform-independent GUI capabilities. The GUI renders block diagrams and 
flowcharts that represent classes, functions, and logical branches in the code. These diagrams aid 
users in visually traversing large codebases and understanding interdependencies. 
The LLM integration leverages the Gemini API, allowing dynamic prompting of code content. 
After parsing, relevant method-level or class-level code blocks are sent to Gemini with a 
structured prompt that requests three core outputs: time complexity analysis, semantic 
summarization, and loop termination prediction. The API responses are parsed and displayed in 
the GUI, stored in the database, and can also be exported. 
All communication with the Gemini API is handled asynchronously to avoid UI lag, and the 
entire codebase adheres to modular design principles to allow future extensibility, such as 
support for other LLMs or advanced static analyzers.

System Architecture
![image](https://github.com/user-attachments/assets/7e9e5f16-c3d0-45b0-b9c0-9c1341ac9340)

Database Architecture
![image](https://github.com/user-attachments/assets/0278b161-4518-4b58-902b-2bcf0a5bc048)



