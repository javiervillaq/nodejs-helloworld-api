pipeline {
    agent any
    tools {
        nodejs 'nodejs21'
    }
    environment {
        // semodifica el path para incluir la instalación de Node.js configurada en Tool Configuration
        NODE_HOME = tool name: 'nodejs21'
        PATH = "${NODE_HOME}/bin:${env.PATH}"
    }
    stages {
        stage('Build') {
            steps {
                echo "Ejecutar npm install" 
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo "Ejecutar npm test push" 
                sh 'npm test'
            }
        }
    }
}