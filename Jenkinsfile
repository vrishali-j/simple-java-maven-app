pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven 3.9.6"
    }

    stages {
        stage('mavenBuild') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/vrishali-j/simple-java-maven-app.git'

                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean package"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
    }
    stage('gradlePreparation') { // for display purposes
       steps{
        // Get  code from a GitHub repository
        //git 'https://github.com/vrishali-j/demo.git'
        git branch: 'main',
        //credentialsId: '12345-1234-4696-af25-123455',
        url: 'https://github.com/vrishali-j/demo.git'
      }
     }
     stage('gradleBuild') {
        steps{
            sh 'chmod +x gradlew'
            sh './gradlew clean build'
            sh 'docker ps'
        }
     }
    }
}
