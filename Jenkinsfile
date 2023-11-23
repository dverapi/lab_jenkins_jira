pipeline {
    agent any

    parameters {
        string(name: 'nombre', defaultValue: 'test', description: 'name')
    } 

    stages {

        stage ('clone repo'){
            steps{
                git branch: 'develop', url: "https://${TOKEN}@${REPOSITORY}"
            }
        }

        stage('Saludo') {
            steps {
               sh "pwd"
               input ('¿Continuar con el saludo?') 
               //sh "echo 'hola mundo ${params.nombre}'"
               sh "make SALUDO name=params.nombre"
            }
        }
    }
}