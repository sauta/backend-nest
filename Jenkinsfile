pipeline {
    agent any // This specifies that the pipeline can run on any available agent
    stages { // Define the stages of the pipeline
        stage('Hello') { // Stage for building the application  
          steps {
                sh 'echo "hola a todos desde el pipeline"' // Shell command to build the application
            }
        }
        stage('Hello') { // Stage for building the application
            steps {
                sh 'echo "Saliendo del saludo"' // Shell command to build the application
            }
        }
        stage('Build') { // Stage for building the application  
            agent {
                docker {
                    image 'node:22' // Use a Docker image with Node.js version 22
                    reuseNode true // Reuse the node for this stage
                }
            }
            steps {
                sh 'npm ci' // Shell command to build the application
            }
        }
    }
}