pipeline {
    agent any

    stages {
        stage('Clonar Repositorio') {
            steps {
                // Clonamos el repositorio y especificamos la rama "main" (ajustar si la rama es diferente)
                git branch: 'main', url: 'https://github.com/MygithubJN/repo-prueba', credentialsId: 'GitHub-Credencial'
            }
        }
        
        stage('Mostrar Archivos Clonados') {
            steps {
                // Listamos los archivos del directorio para asegurarnos de que el repositorio se clonó correctamente
                sh 'ls -al'
            }
        }
    }
}
