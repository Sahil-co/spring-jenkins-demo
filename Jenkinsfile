pipeline {
    agent any
    stages {
        stage('Back-end') {
          agent {
            docker { image 'maven:3.9.5' }
          }
          steps {
            sh 'mvn clean package'
          }
        }
    // post after stages, for entire pipeline, is also an implicit step albeit with explicit config here, unlike implicit checkout stage
    // post {
    //     always {
    //         junit '**/target/surefire-reports/TEST-*.xml'
    //         archiveArtifacts 'target/*.jar'
    //     }
    }
}
