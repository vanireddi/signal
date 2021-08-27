pipeline {
    agent any

    stages {
        stage('vn') {
            steps {
                git 'https://github.com/vanireddi/signal.git'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn clean package'
            }
        }
        stage('artifact push to nexus'){
            steps{
            sh 'mvn -s./settings.xml deploy'  
            }
            
        }
    }
}
