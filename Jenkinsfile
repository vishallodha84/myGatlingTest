pipeline {
    agent any
    stages {
        stage("Run Gatling") {
            steps {
                 withMaven(maven: 'maven-3') {
                    sh 'mvn gatling:test'
                 }
            }
            post {
                always {
                    gatlingArchive()
                }
            }
        }
    }
}