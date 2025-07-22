pipeline {
    agent any

    stages {
        stage('Code') {
            steps {
              git 'https://github.com/Muralidharan291123/web-app.git'
            }
        }
        stage('code-build') {
            steps {
                 sh "mvn clean package"
            }
        }
      
    }
}
