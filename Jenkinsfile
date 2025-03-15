pipeline {
    agent any

    stages {
        stage('Obtener estado de contenedores Docker') {
            steps {
                script {
                    // Ejecutamos el comando `docker ps` para listar los contenedores en ejecución
                    def dockerStatus = sh(script: 'docker ps', returnStdout: true).trim()
                    // Imprimimos el estado de los contenedores
                    echo "Estado de los contenedores Docker locales:"
                    echo dockerStatus
                }
            }
        }
    }
}

