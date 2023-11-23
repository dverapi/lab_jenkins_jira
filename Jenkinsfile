def repository
def token

pipeline {
    agent any

    environment {
        repository=${REPO}
        token=${TOKEN}
    }

    parameters {
        string(name: 'nombre', defaultValue: 'test', description: 'name')
    } 

    stages {

        stage ('clone repo'){
            steps{
                git branch: 'develop', url: 'https://${token}@${repository}'
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