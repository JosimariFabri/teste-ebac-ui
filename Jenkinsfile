pipeline {
    agent any

    stages {
        stage('Clonar repostório') {
            steps {
               git branch: 'main', url: 'https://github.com/JosimariFabri/teste-ebac-ui.git'
            }
        }
        stage('Instalar dependencias') {
            steps {
               bat 'npm install'
            }
        }
        stage('Executar testes') {
            steps {
               bat '''set NO_COLOR=1
npm run cy:run'''
            }
        }
 
    }
}