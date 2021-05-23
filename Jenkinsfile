pipeline {
    agent any
    stages {
        stage('run frontend') {
            steps {
                echo 'executing yarn' 
                nodejs('Node-10.17') {
                    sh 'yarn install'              
                  }
            }
        }
        stage('run backend') {
            steps {
                echo 'executing gradle'
                sh 'wget https://services.gradle.org/distributions/gradle-5.0-bin.zip gradle'
                sh 'unzip gradle-5.0-bin.zip'
	        sh 'mv gradle-5.0 gradle'
                sh 'export GRADLE_HOME=/opt/gradle/gradle-5.0'
                sh 'export PATH=${GRADLE_HOME}/bin:${PATH}'
                sh 'gradle -v'
               }
          }
     }
 }
