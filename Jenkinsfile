pipeline { 
    agent any 
    stages {
        stage('Clone maven app repo') { 
            steps { 
                sh "rm -rf maven_app"
                sh 'git clone https://github.com/AbdulazizAlsaif/maven_app.git' 
                sh "mvn clean -f maven_app"
            }
        }
        stage('Test'){
            steps {
                sh 'mvn test -f maven_app'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn package -f maven_app'
            }
        }
    }
}
