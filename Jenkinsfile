pipeline {

  agent any
  
  stages {
    
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }

    stage('Test') {
      steps {
           echo("Unit Testing is successfull...")
      }
    }

     stage('Deployment') {
      steps {
            bat 'mvn -U -V -e -B -DskipTests -Pdevelop deploy -DmuleDeploy'
      }
    }
  }
}
