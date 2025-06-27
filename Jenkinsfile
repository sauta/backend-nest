pipeline {
    agent any // This specifies that the pipeline can run on any available agent
    stages { // Define the stages of the pipeline
        stage('Build') { // Stage for building the application  
            steps {
                sh 'echo hola a todos desde el pipeline' // Shell command to build the application
            },
        stage('Compile') { // Stage for compiling the application
            steps {
                echo 'Compiling...'
            }
        }
        stage('Test') { // Stage for testing the application
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') { // Stage for deploying the application
            steps {
                echo 'Deploying...' 
            }
        }
    }
    }
   }
