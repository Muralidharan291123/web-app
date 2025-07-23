pipeline {
    agent {
        label{
            chumma slv
        }
    }

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
        stage('artifact')
        {
            steps{
             nexusArtifactUploader artifacts: [[artifactId: 'myweb1', classifier: '', file: 'target/myweb1-8.6.5.war', type: '.war']], credentialsId: 'admin01', groupId: 'in.javahome', nexusUrl: '16.16.98.22:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'https://github.com/Muralidharan291123/web-app.git', version: '8.6.5'   
            }
        }
      
    }
    post{
        success{
            echo 'success da mapla'
        }
    }
}
