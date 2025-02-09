
pipeline {
    agent any
    environment {
      CF_API_ENDPOINT = "https://api.cf.us10-001.hana.ondemand.com"
      CF_ORG = "facd30cetrial"
      CF_SPACE = "dev"
    }
    stages {
        // ... other stages ...
        stage('Deploy') {
            steps {
                sh './piper mavenExecute'
                sh './piper artifactPrepareVersion'
                sh './piper deployToCF'
            }
        }
    }
}
