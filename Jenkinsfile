pipeline {
    agent any

    parameters {
        //choice(name: 'ambiente', choices: [Desarrollo], description: 'environment deploy')
        string(name: 'nombre', defaultValue: 'test', description: 'name')
    } 

    stages {

        stage('Saludo') {
            steps {
               sh "echo 'hola mundo ${params.nombre}'"
               //sh "make SALUDO name=params.nombre"
            }
        }
    }
}