pipeline 
{
    agent any
    tools {
        maven "Maven3"
        }
    stages {
        stage('snyk dependency scan') {
      tools {
        snyk 'Snyk_Test'
      }	
      steps {
        snykSecurity(
          organisation: 'anmol.seth',
          severity: 'low',
          snykInstallation: 'Snyk_Test',
          snykTokenId: 'Snyk-Jenkins',
          failOnIssues: 'true'
        )		
      }
    }
    stage ('Compile Stage') {

            steps {
                    sh 'mvn clean compile'
            }
        }
    
}
}
