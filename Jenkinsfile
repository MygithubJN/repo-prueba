pipeline {
    agent any

<<<<<<< HEAD
    environment {
        // Configuración del repositorio Git
        GIT_REPO_URL = 'https://github.com/MygithubJN/repo-prueba'  // Cambia esto a la URL de tu repositorio Git
        GIT_CREDENTIALS = 'GitHub-New-Credentials'  // Nombre de las credenciales de Git en Jenkins (si las usas)
    }

    stages {
        stage('Clonar Repositorio') {
            steps {
                script {
                    // Clonamos el repositorio
                    git url: "$GIT_REPO_URL", credentialsId: "$GIT_CREDENTIALS", branch: 'main'
                }
            }
        }

        stage('Guardar docker-compose.yml actualizado') {
            steps {
                script {
                    // Hacemos un `git add` del archivo docker-compose.yml
                    sh 'git add docker-compose.yml'

                    // Realizamos el commit de los cambios (si hay alguno)
                    sh 'git commit -m "Actualización de docker-compose.yml con configuraciones actuales" || echo "No hay cambios"'

                    // Hacemos el push para guardar los cambios en el repositorio remoto
                    sh 'git push origin main'
                }
            }
        }
    }

    post {
        always {
            // Limpiar si es necesario o realizar otras acciones post-pipeline
            echo 'Pipeline completado.'
        }
    }
}
=======
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

>>>>>>> 038c859 (Agregado Jenkinsfile con pipeline de Docker)
