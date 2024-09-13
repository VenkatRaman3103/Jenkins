pipeline {
    agent any

    stages {
        stage("Hello world") {
            steps {
                echo "Hello world"
            }
        }

        stage("Install dependencies") {
            steps {
                sh "npm install"
            }
        }

        stage("Run the Server") {
            steps {
                sh "npm start"
            }
        }
    }
    
}
