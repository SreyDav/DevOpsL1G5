node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'sonar-jenkins';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-jenkins"
    }
  }
}
