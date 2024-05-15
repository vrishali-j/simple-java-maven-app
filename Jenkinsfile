pipeline {
      agent any
      stages {
        stage('Build') { 
            steps {
                withEnv(['PATH=$PATH:/opt/maven/bin']) 
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }

}
