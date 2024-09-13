pipeline{
    agent any

    stages{
        stage("Hello world"){
            steps{
                echo "Hello world"
            }
        }

        stage("Run the Server"){
            steps{
                sh "npm start"        
            }
        }
    }

    post{
        success {
            echo "Server is running successfully"
        }
        failure {
            mail to : "venkat.raman.3103@gmail.com"
            subject : "Failed Pipeline : ${env.JOB_NAME} - ${env.BUILD_NUMBER}",
            body : "The Build failed. please check"
        }
    }
}