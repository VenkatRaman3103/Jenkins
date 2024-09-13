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

    post {
        success {
            echo "Server is running successfully"
            mail to: "venkat.raman.3103@gmail.com",
                 subject: "Pipeline: ${env.JOB_NAME} - ${env.BUILD_NUMBER} Running Successfully",
                 body: "The Build succeeded. Please check."
        }
        failure {
            mail to: "venkat.raman.3103@gmail.com",
                 subject: "Failed Pipeline: ${env.JOB_NAME} - ${env.BUILD_NUMBER}",
                 body: "The Build failed. Please check."
        }
    }
}
