node('ci-community') {
  
  agent any
  tools {
    maven 'Maven 3.0.5'
  }

  stages {
    stage ('Initialize') {
      env.PATH = "${tool 'apache-maven-3.0.5'}/bin:${env.PATH}"
    }

    stage ('Build') {
        steps {
            sh 'mvn -Dmaven.test.failure.ignore=true deploy' 
        }
    }
  }

}
