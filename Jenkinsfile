pipeline {
    agent any

    parameters {
        string(name: 'nombre', defaultValue: '', description: 'name')
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
               sh "echo 'hola mundo ${params.nombre}'"
            }
        }
    }
}