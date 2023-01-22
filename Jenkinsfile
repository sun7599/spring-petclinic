pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''./mvnw sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.host.url=http://172.31.26.221:9000 \\
  -Dsonar.login=sqp_b023cc27dc21f44b75336d6f5b52910a817a77a7'''
      }
    }

  }
}