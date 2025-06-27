pipeline {
    agent any // This specifies that the pipeline can run on any available agent
    environment { // Define environment variables for the pipeline
        NPM_CONFIG_CACHE = '$[WORKSPACE]/.npm' // Path to npm cache directory
        NPM_CONFIG_USERCONFIG = '$[WORKSPACE]/.npmrc' // Path to npm configuration file
        NPM_CONFIG_LOGLEVEL = 'warn' // Set npm log level to warn
    }
    stages { // Define the stages of the pipeline
        stage('in-Hello') { // Stage for building the application  
          steps {
                sh 'echo "hola a todos desde el pipeline"' // Shell command to build the application
            }
        }
        stage('out-Hello') { // Stage for building the application
            steps {
                sh 'echo "Saliendo del saludo"' // Shell command to build the application
            }
        }
        stage('Build-and-test') { // Stage for building the application  
            agent {
                docker {
                    image 'node:22' // Use a Docker image with Node.js version 22
                    args '-u root:root' // Run the container as root user
                    reuseNode true // Reuse the node for this stage
                }
            }
            steps {
                sh 'npm ci' // Shell command to build the application
                sh 'npm test:cov' // Shell command to run tests
            }
        }
    }
}