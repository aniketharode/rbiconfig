pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'mvn clean install -DskipTests'
            }
        }
        
         stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
         stage('Push'){
            steps{
                sh 'docker login -u aniketharode -p Google@98'
                sh 'docker push aniketharode/rbiconfig-server:0.0.1-SNAPSHOT'
            }
        }
        
        stage('Docker compose'){
            steps{
                sh 'pwd'
                sh 'cd /root/'
                sh 'pwd'
                sh 'docker-compose up -d'
            }
        }
    }
}
