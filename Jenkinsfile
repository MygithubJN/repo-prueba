pipeline {
    agent any

    stages {
        stage('Clonar Repositorio') {
            steps {
                git url: 'https://github.com/tu-usuario/repo-prueba.git'
            }
        }
        
        stage('Mostrar Archivos Clonados') {
            steps {
                sh 'ls -al'
            }
        }
    }
}
