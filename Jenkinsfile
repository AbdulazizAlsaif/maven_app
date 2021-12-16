pipeline { 
    agent any 
    stages {
        stage('Clone maven app repo') { 
            steps {  
                sh "mvn clean"
            }
        }
        stage('Test'){
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
