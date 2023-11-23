pipeline {
    agent any

    parameters {
        string(name: 'nombre', defaultValue: 'test', description: 'name')
    } 

    stages {

        stage ('clone repo'){
            steps{
                sh "echo ${TOKEN} //////////// ${REPOSITORY}"
                

                git branch: 'develop', url: 'https://${TOKEN}@${REPOSITORY}'
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