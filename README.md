
<div align="center">
<img alt="biketag-vue logo" src="https://raw.githubusercontent.com/keneucker/biketag-website/production/public/img/Tag-Logo-Stacked-V2-medium.png" height="auto" width="200" style="border-radius:25%;">
</div>

# Biketag Monorepo

## Introduction

Welcome to the BikeTag Monorepo, the complete platform of software that runs biketag.org. This project brings together various software projects like biketag-api and biketag-vue, alongside the applications and websites that use those previously developed packages.

The BikeTag Project is not just about code; it's about community. Whether you're a developer looking to contribute to the project, a player interested in the mechanics of the game, or simply someone keen on being part of a vibrant, bike-loving community, this monorepo is your gateway. Here, you can dive into the development process, engage in discussions, and help shape the future of BikeTag. We welcome your ideas, feedback, and contributions through GitHub issues and discussions, making this a truly collaborative and evolving project for everyone passionate about biking and gaming.

## BikeTag Platform (v3)

### Apps

#### [biketag-app](https://github.com/keneucker/biketag-app)

The BikeTag App is the central hub for players to engage with the BikeTag game in their respective cities. Available as both a mobile app and a web platform via [biketag.org](https://biketag.org/), it offers an intuitive and accessible way for players to join games, submit their tags, and interact with the community. This app is the face of BikeTag, providing a seamless and enjoyable IRL gaming experience.

#### [biketag-games](https://github.com/keneucker/biketag-games)

biketag-games is the backbone of the BikeTag game data. It is a [sanity.io](https://www.sanity.io/) schema and studio project that manages all game-related data, including locations, tags, and game rules. This project ensures that the game data is structured, consistent, and easily accessible, forming the foundation upon which the BikeTag games operate.

The future roadmap for this project is to have it contained within the biketag-admin as self contained components. Please consider helping out with this project if you have an interest or experience in working with Sanity.io and the BikeTag Project.

#### [biketag-administration](https://github.com/keneucker/biketag-administration)

biketag-administration is akin to the control room for BikeTag. It's a [sanity.io](https://www.sanity.io/) schema and studio project focused on the administrative aspects of the BikeTag ecosystem. This includes managing user roles, overseeing game settings, and ensuring the smooth operation of the platform. It's essential for maintaining the integrity and functionality of the BikeTag games.

The future roadmap for this project is to have it contained within the biketag-admin as self contained components. Please consider helping out with this project if you have an interest or experience in working with Sanity.io and the BikeTag Project.

### Packages

#### [biketag-api](https://github.com/keneucker/biketag-api) (formerly `biketag` on npm)

The biketag-api, previously known as `biketag` on npm, is the API layer that enables interaction with and creation of new BikeTag game data. It's the engine under the hood, processing game actions, storing data, and ensuring that the different components of the BikeTag ecosystem communicate effectively. This API is crucial for developers looking to build on or integrate with the BikeTag platform.

The future roadmap for this project is to implement an AWS source adapter for storing BikeTag Game data Images on AWS. Please consider helping out with this project if you have an interest or experience in working with AWS and the BikeTag Project.

#### [biketag-vue](https://github.com/keneucker/biketag-vue)

biketag-vue is a comprehensive Vue.js component library and Pinia store tailored for BikeTag applications. It provides a set of reusable Vue components and state management solutions, streamlining the development of BikeTag's user interfaces. This package is invaluable for developers working on Vue.js-based BikeTag applications, offering consistency and efficiency in UI development.

The future roadmap for this project is to convert all components to stateless tailwind styled composables that are fully classed using the BEM css naming convention for easy extensibility.

#### [biketag-admin](https://github.com/keneucker/biketag-admin)

Similar to biketag-vue, biketag-admin is a Vue.js component library and Pinia store, but it's specifically designed for BikeTag's administrative interfaces. It facilitates the creation of intuitive and effective admin panels and tools, ensuring that administrators can manage the platform effectively. This package is essential for building the administrative side of the BikeTag ecosystem, ensuring a smooth and manageable operation.

This project is actively being redeveloped from code that is currently in the biketag-vue project.


## Getting Started with the BikeTag Monorepo

Welcome to the BikeTag Monorepo, a centralized codebase using TurboRepo to manage a constellation of interconnected projects related to the BikeTag game. This guide will walk you through the initial steps of setting up and understanding the monorepo structure, powered by TurboRepo.

### Understanding TurboRepo

TurboRepo is a high-performance build system specifically designed for JavaScript and TypeScript monorepos. It enhances the development experience in a monorepo by offering features like:

-   **Efficient Caching**: TurboRepo caches the output of tasks, reducing build times by avoiding redundant work.
-   **Task Orchestration**: It intelligently runs tasks across various projects in the monorepo, ensuring dependencies are respected.
-   **Optimized Builds**: TurboRepo optimizes build processes by parallelizing tasks wherever possible.

TurboRepo is crucial in the BikeTag Monorepo for managing dependencies across projects and streamlining the development process. For detailed information on TurboRepo and its capabilities, you can refer to TurboRepo documentation.

### Setting Up the Monorepo

#### 1. Clone the Repository

Start by cloning the BikeTag Monorepo to your local machine using the following commands:

bashCopy code

`git clone https://github.com/KenEucker/biketag.git
cd biketag` 

#### 2. Install Dependencies and run the build

`npm install` then `npm run build`

#### 3. Exploring Scripts

The `package.json` file in the monorepo contains scripts that are essential for building, testing, and running the projects. Here are some key scripts:

-   **build**: Runs `turbo run build`, which compiles all the projects in the monorepo. TurboRepo ensures that this build process is efficient by utilizing its caching and task orchestration capabilities. For more on the build process in TurboRepo, see their build command documentation.
    
-   **dev**: Starts the development server for the projects. It's typically used for local development and testing.
    
-   **test**: Executes `turbo run test`, running tests across all projects in the monorepo. TurboRepo ensures tests are run in an optimized manner, improving the speed and reliability of testing. Check the test command documentation for more details.
    
-   **lint**: Checks for linting errors across the projects, ensuring code quality and consistency.
    

These scripts are integral to managing the monorepo's workflow and ensuring that all projects within it are functioning correctly and cohesively.


## Documentation

The BikeTag Monorepo is rich with various projects, each having its own set of documentation. This section aims to guide you through the available resources to help you understand and contribute effectively to the BikeTag projects.

### Overview

Good documentation is essential for any software project. It helps new and existing contributors understand the architecture, design decisions, and how to get started with development. In the BikeTag Monorepo, each project's documentation serves as an in-depth guide covering its specific functionalities, APIs, and usage instructions. When making changes to the codebases in each project, it is requested that you update the documentation to reflect any updates in functionality or configuration.

### Project-Specific Documentation

#### biketag-app

-   **Description**: This is the main application for players of the BikeTag game. It allows participation in games, submission of tags, and interaction with other players.
-   **Documentation**: Detailed documentation can be found within the project directory. It includes setup instructions, feature descriptions, and guidelines for contributing to the app development.

#### biketag-api

-   **Description**: The API layer for interacting with and creating new BikeTag game data. It's integral for developers building on or integrating with the BikeTag platform.
-   **Documentation**: The API documentation provides an overview of the endpoints, data structures, and authentication mechanisms. It's essential for understanding how to interact with the BikeTag backend services.

#### biketag-vue

-   **Description**: A Vue.js component library and Pinia store tailored for BikeTag applications, offering a set of reusable components and state management solutions.
-   **Documentation**: Includes details on the available components, their props, events, and usage examples. It's a valuable resource for developers working with Vue.js in the BikeTag ecosystem.

#### Other Projects

-   Each additional project in the monorepo, like `biketag-games` and `biketag-administration`, comes with its own README and documentation, detailing its purpose, setup, and how to contribute.

### General Guidelines

-   **Navigating Documentation**: Check the `README.md` file in each project directory for an introduction and links to more detailed documentation.
-   **Contribution Guides**: If you're interested in contributing, look for a `CONTRIBUTING.md` file in the project directories, which will provide guidelines on how to contribute effectively.
-   **Seeking Help**: Use GitHub issues for questions or problems related to a specific project. This can also be a good way to find additional documentation or resources shared by the community.

## GitHub Workflow for Contributing to BikeTag Projects

1. **Fork _this_ Repository** OR **Fork _that_ Repository** 
   - Click on the 'Fork' button to create a copy under your account of this repository to make changes to the monorepo configuration only. Otherwise, you can simply download the contents of this repo and for the individual project you will be submitting changes to. If you're working on the biketag-app project, you would fork that and submit your changes to that repo directly.

2. **Clone the Forked Repository**
   - Clone the forked repository to your local machine:
     ```bash
     git clone https://github.com/your-username/biketag-[repo].git
     ```

3. **Switch to the `develop` Branch**
   - Ensure you're working on the most recent `develop` branch:
     ```bash
     git checkout develop
     ```

4. **Make Your Changes**
   - Modify the code as needed for your contribution.

5. **Commit and Push Changes**
   - Commit your changes with a clear message.
   - Push the changes to your fork:
     ```bash
     git push origin develop
     ```

6. **Create a Pull Request**
   - Go to your fork on GitHub.
   - Click 'New Pull Request'.
   - Ensure the base repository and branch match the original repository's `develop` branch.
   - Submit the pull request for review.

  

## Coding Conventions

  Prettier is ran and applied automatically as part of a precommit hook, so you don't have to worry about semicolons or trailing commas. Other than that, there are no requirements for how you contribute your code to the BikeTag Project other than following the nature of the code of conduct in your naming and comments. 

  Contributions you make will go through a review process and the final code that makes it into the codebase is the one that we're all going to be happy with. Thanks!

## Code of Conduct

1.  **Purpose**: It sets expectations for contributions, focusing on respectful and safe interactions within the BikeTag community, both online and at official events.
    
2.  **Core Values**: Highlights inclusivity, community-driven initiatives, and open collaboration as foundational principles.
    
3.  **Expected Behavior**: Describes the desired conduct of participants to foster a positive community.
    
4.  **Unacceptable Behavior**: Defines behaviors that are not tolerated, ensuring a respectful environment.
    
5.  **Playing BikeTag**: Guidelines specific to playing BikeTag Games using the BikeTag App or on the website biketag.org.
    
6.  **Scope**: Outlines the extent and applicability of the Code of Conduct.
    
7.  **Consequences of Unacceptable Behavior**: Details the actions that will be taken in response to violations, including correction, warning, temporary ban, and permanent ban.
    
8.  **Reporting Guidelines**: Provides instructions on how to report unacceptable behavior.
    
9.  **Contact Info**: Offers contact information for reporting or inquiries related to the Code of Conduct.
    

This Code of Conduct is essential for maintaining a respectful, inclusive, and collaborative environment in the BikeTag Project community.

## License

This monorepo project and all BikeTag software projects underneath it are licensed under the GNU AFFERO GENERAL PUBLIC LICENSE.
