pipeline {
    agent any
    stages {
        stage('Back-end') {
          agent {
            docker { image 'maven:3.8.1-adoptopenjdk-11' }
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
    // }
}
