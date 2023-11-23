pipeline {
    agent any

    parameters {
        string(name: 'nombre', defaultValue: 'test', description: 'name')
    } 

    stages {

        stage ('clone repo'){
            steps{
                git branch: 'develop', url: "https://${TOKEN}@${REPOSITORY}"
                //git branch: 'develop', url: 'https://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@github.com/dverapi/lab_jenkins_jira.git'
            }
        }

        stage('Saludo') {
            steps {
               input ('esto es un test') 
               sh "echo 'hola mundo ${params.nombre}'"
               //sh "make SALUDO name=params.nombre"
            }
        }
    }
}