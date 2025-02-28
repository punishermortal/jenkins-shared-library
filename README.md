# Jenkins Shared Library

Welcome to the Jenkins Shared Library repository! This library provides reusable, modular, and maintainable pipeline steps and functions that can be shared across Jenkins pipelines, making your CI/CD automation more efficient and scalable.
📦 Features

    Reusable Functions: Simplify common pipeline tasks like building, testing, and deploying.
    Support for Declarative and Scripted Pipelines: Flexibility for different types of Jenkins pipelines.
    Integration with External Tools: Easily integrate with external APIs and tools.
    Customizable: Adapt functions and steps to meet the unique needs of your projects.
    Version-Controlled: Manage changes to pipeline logic and keep everything organized.

📂 Directory Structure
    .
    ├── vars/
    │   ├── exampleFunction.groovy     # Example of a shared function
    │   └── anotherFunction.groovy     # Another shared function
    ├── resources/
    │   └── config.yaml                # Configuration files for pipelines
    └── README.md                      # This file
        vars/: Contains global functions accessible in your pipelines.
        resources/: Stores configuration files or templates used by the pipeline.

🚀 Getting Started

    Clone this repository to your Jenkins instance:
            https://github.com/punishermortal/jenkins-shared-library.git

    Configure Jenkins to use the shared library:

        Go to Manage Jenkins > Configure System.
        Scroll to Global Pipeline Libraries.
        Add a new library:
            Name: shared-library
            Source Code Management: Git
            Repository URL: <repository-url>

    Use the shared library in your pipeline:
        @Library('shared-library') _
        exampleFunction()

📖 Usage

To use a function from this shared library in your pipeline, simply reference the library and call the desired function:

        @Library('shared-library') _
        pipeline {
            agent any
            stages {
                stage('Build') {
                    steps {
                        script {
                            exampleFunction() // Call a shared function
                        }
                    }
                }
            }
        }

🤝 Contributing

Contributions are welcome! Feel free to fork this repository, create a new branch, and submit a pull request.

    Fork the repository
    Create a new feature branch (git checkout -b feature/new-function)
    Commit your changes (git commit -am 'Add new function')
    Push to the branch (git push origin feature/new-function)
    Open a pull request

📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
