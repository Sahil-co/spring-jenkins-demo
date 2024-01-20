pipeline {
    agent any
    stages {
        // implicit checkout stage

        stage('Build') {
            steps {
                mvn clean and install
            }
        }
    }
    // post after stages, for entire pipeline, is also an implicit step albeit with explicit config here, unlike implicit checkout stage
    post {
        always {
            junit '**/target/surefire-reports/TEST-*.xml'
            archiveArtifacts 'target/*.jar'
        }
    }
}