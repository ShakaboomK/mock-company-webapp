pipeline {
  /*
   * TODO: Implement pipeline stages/steps
   *   See documentation: https://www.jenkins.io/doc/book/pipeline/syntax/#stages
   */
   agent any

   stages{
    stage('Build'){
      steps{
        echo 'Building the application...'
        sh './gradlew assemble'
      }
    }
    stage('Test'){
      steps{
        echo 'Running tests...'
        sh './gradlew test'
      }
    }
   }
   post{
    success{
      echo 'Build and test stages completed sucessfully!'

    }
    failure{
      echo 'Build and test stages failed!, please check the logs.'
    }
   }
}
