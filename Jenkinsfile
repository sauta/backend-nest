pipeline {
    agent any // This specifies that the pipeline can run on any available agent
    stages { // Define the stages of the pipeline
        stage('Build') { // Stage for building the application  
            agent {}
            steps {
                sh 'echo hola a todos desde el pipeline' // Shell command to build the application
            }
            
        }
    }
        stages { // Define the stages of the pipeline
        stage ('Test') { // Stage for testing the application
            agent {}
            steps {
                sh 'echo hola a todos desde el pipeline' // Shell command to test the application
            }
        }
        stage ('Deploy') { // Stage for deploying the application
            agent {}
            steps {
                sh 'echo hola a todos desde el pipeline' // Shell command to deploy the application
            }
        }
        }
        }


