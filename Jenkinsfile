pipeline {
    agent any

    parameters {
        //choice(name: 'ambiente', choices: [Desarrollo], description: 'environment deploy')
        text(name: 'nombre', defaultValue: 'test', description: 'name')
    } 

    stages {
        stage('clone repo') {
            steps {
              withCredentials(usernamePassword(credentialsId :user-github ,passwordVariable: 'GIT_PASSWORD', usernameVariable: 'GIT_USERNAME', url: 'https://github.com/dverapi/lab_jenkins_jira.git/tree/develop'))
            }
        }

        stage('Saludo') {
            steps {
               sh "make SALUDO name=params.nombre"
            }
        }
    }
}