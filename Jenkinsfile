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
                sh 'wget https://services.gradle.org/distributions/gradle-5.0-bin.zip /etc'
                sh 'unzip /etc/gradle-5.0-bin.zip'
	        sh 'mv /etc/gradle-5.0 gradle'
                sh 'export GRADLE_HOME=/etc/gradle'
                sh 'export PATH=${GRADLE_HOME}/bin:${PATH}'
               }
          }
     }
 }
