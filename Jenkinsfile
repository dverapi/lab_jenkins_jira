pipeline {
    agent any

    parameters {
        string(name: 'nombre', defaultValue: 'test', description: 'name')
    } 

    stages {

        stage ('clone repo'){
            steps{
                //git branch: 'develop', url: "https://${TOKEN}@${REPOSITORY}"
                git branch: 'develop', url: 'https://ghp_LX6Jea1jQp1XMWWWUqTGVxd1P$jksYC0HCo5x@github.com/dverapi/lab_jenkins_jira.git'
            }
        }

        stage('Saludo') {
            steps {
               sh "echo 'hola mundo ${params.nombre}'"
               //sh "make SALUDO name=params.nombre"
            }
        }
    }
}