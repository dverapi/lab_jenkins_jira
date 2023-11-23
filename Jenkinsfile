pipeline {
    agent any

    parameters {
        //choice(name: 'ambiente', choices: [Desarrollo], description: 'environment deploy')
        text(name: 'nombre', defaultValue: 'test', description: 'name')
    } 

    stages {

        stage('Saludo') {
            steps {
               sh 'echo "hola mundo ${parameters.nombre}"'
               //sh "make SALUDO name=params.nombre"
            }
        }
    }
}