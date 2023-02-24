pipeline {
    agent any
    environment {
        name = 'sandeep'
    }
    parameters {
        string(name: 'Person', defaultValue: 'Sandeep', description: 'who are you')
        booleanParam(name: 'isMale', defaultValue: 'Yes', description: '')
        choice(name: 'city', choices: ['jaipur','Hyderabad','pune','BLR'],description: "")
        
    }
    stages {
        stage('Run A Command') {
            steps {
                sh '''
                date
                ls
                pwd
                cal 2023
                '''
            }
        }
        stage('Environment Variables') {
            environment {
                username = 'naveen'
            }
            steps {
                sh 'echo "${BUILD_ID}"'
                sh 'echo "${name}"'
                sh 'echo "${username}"'
            }
        }
         stage('Parmeters') {
            steps {
                sh 'echo "${name}"'
                sh 'echo "${person}"'
            }
        }
        stage('Deploy on test') {
            steps {
                echo 'Deploy on test'
            }
        }
        stage('continue') {
            input {
                message "should we continue?"
                ok "yes we should"
            }
            steps {
                echo 'Deploy on test'
            }
        }
        stage('Deploy on prod') {
            steps {
                echo 'Deploy on prod'
            }
        }
    }
    post{
        always{
            echo ' i Will always say hello again'
        }
        failure {
            echo 'failure'
        }
        success {
            echo 'Success'
        }
    }
}
