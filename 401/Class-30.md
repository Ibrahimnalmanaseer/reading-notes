# Component-Based Architecture

## What is a Component?

A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.

can be defined as a unit of composition with a contractually specified interface and explicit context dependencies only.


### Views of a Component

**Object-oriented view**

A component is viewed as a set of one or more cooperating classes. Each problem domain class (analysis) and infrastructure class (design) are explained to identify all attributes and operations that apply to its implementation. It also involves defining the interfaces that enable classes to communicate and cooperate.

**Conventional view**
It is viewed as a functional element or a module of a program that integrates the processing logic.

## Characteristics of Components

- Reusability − Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.

- Replaceable − Components may be freely substituted with other similar components.

- Not context specific − Components are designed to operate in different environments and contexts.

- Extensible − A component can be extended from existing components to provide new behavior.

- Encapsulated − A A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.

- Independent − Components are designed to have minimal dependencies on other components.


## Principles of Component−Based Design

- The software system is decomposed into reusable, cohesive, and encapsulated component units.

- Each component has its own interface that specifies required ports and provided ports; each component hides its detailed implementation.

- A component should be extended without the need to make internal code or design modifications to the existing parts of the component.

- Depend on abstractions component do not depend on other concrete components, which increase difficulty in expendability.

![principles_of_component_based_design](https://user-images.githubusercontent.com/62019258/209584897-b97a0ca7-75d8-4cb8-837f-541136fdba91.png)


