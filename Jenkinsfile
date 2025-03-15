pipeline {
    agent any

    stages {
        stage('Clonar Repositorio') {
            steps {
                git url: 'https://github.com/MygithubJN/repo-prueba'
            }
        }
        
        stage('Mostrar Archivos Clonados') {
            steps {
                sh 'ls -al'
            }
        }
    }
}
