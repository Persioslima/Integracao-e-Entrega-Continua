
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Persioslima/Integracao-e-Entrega-Continua.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                script {
                    // Executa o npm install
                    sh 'npm install'
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    // Executa os testes definidos no package.json
                    sh 'npm test'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Aqui você pode adicionar o comando para o deploy
                    echo 'Fazendo o deploy...'
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline executada com sucesso!'
        }
        failure {
            echo 'Pipeline falhou!'
        }
    }
}
