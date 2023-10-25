# Martian Robot Society Hierarchy 🤖️🚀

In the year 3142, robots established a complex hierarchical society on Mars, and this project involves modelling their organization using tree data structures. This README will provide an overview of the project, its components, functionality, and how to use them.

## Introduction

In this futuristic Martian society, every robot is considered a citizen of Mars and plays a specific role. Robots in this society are organized into a hierarchical structure with distinct roles and responsibilities. This hierarchy is represented using a tree data structure, where each node in the tree represents a citizen. Citizens have relationships with each other, where one citizen can be a superior to others, and some citizens serve as leaders of specific districts within the society.

## Components

The project consists of three main classes in the `society_hierarchy.py` file:

### Citizen

The `Citizen` class represents a citizen in the Martian Robot Society. Each citizen has various characteristics:

- Citizen ID number: A unique identifier for each citizen.
- Manufacturer: The name of the company that manufactured the robot.
- Model year: The year in which the robot was manufactured.
- Job: The role or job of the citizen within the society.
- Rating: A measure of how good of a citizen they are, represented as an integer from 0 to 100.

Each citizen can also have one superior and any number of subordinates, both direct and indirect. Direct subordinates work directly under the citizen, while indirect subordinates are subordinates of subordinates.

### DistrictLeader

`DistrictLeader` is a subclass of `Citizen` with the additional responsibility of leading a district. District leaders are similar to regular citizens but also keep track of the district they lead. All subordinates (both direct and indirect) of a district leader are considered part of that district. A citizen can belong to multiple districts, but the term "immediate district" refers to the one at the lowest level in the tree.

### Society

The `Society` class represents the entire Martian Robot Society and is responsible for managing the hierarchical structure. It tracks the head of the entire society (the root of the hierarchy) and provides operations for managing citizens within the society. This includes adding new citizens, removing citizens, or finding citizens based on their ID numbers.

## Features

The Martian Robot Society Hierarchy project offers a wide array of features and functionalities for modeling and managing the hierarchical organization. Here are the key features:

### 📋 Citizen Management 

- **Add and Remove Subordinates**: Citizens can add or remove subordinates, defining their position within the hierarchy.

- **Change Superior**: Citizens can change their superior, allowing for a flexible hierarchical structure.

- **Retrieve Citizens**: Easily retrieve citizens by their unique ID numbers.

### 🔍 Hierarchy Exploration 

- **Get Subordinates**: Access both direct and indirect subordinates of a citizen.

- **Society Head**: Find the head of the entire society, serving as the root of the hierarchy.

- **Find Common Superior**: Determine the closest common superior of two citizens based on their IDs.

### 🚥 Society Management 

- **Citizen Lookup**: Retrieve specific citizens based on their unique IDs.

- **Get All Citizens**: Obtain a comprehensive list of all citizens within the society.

- **Add New Citizens**: Add new citizens to the society, maintaining the hierarchical structure.

- **Job-Based Citizen Retrieval**: Identify citizens based on their specific job roles within the society.

### 🦾 District Leadership 

- **District Leader**: Introduce DistrictLeaders who manage specific districts, which can be geographical or domain-based.

- **List District Citizens**: Obtain a list of all citizens within a district led by a DistrictLeader, including subordinates.

- **District Name Handling**: Determine and rename the name of the district led by a DistrictLeader.

- **Role Transition**: Change the role of citizens between DistrictLeader and ordinary citizen as their responsibilities evolve.

### 🎭 Promotion and Deletion 

- **Promote Citizens**: Promote ordinary citizens based on their ratings, including swapping positions with superiors if necessary.

- **Citizen Deletion**: Safely remove citizens from the society while preserving the hierarchical structure.
