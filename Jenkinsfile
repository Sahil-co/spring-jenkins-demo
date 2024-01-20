pipeline {
    agent any
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }
    stages {
        // implicit checkout stage

        stage('Build') {
            steps {
                sh "mvn clean package"
            }
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
