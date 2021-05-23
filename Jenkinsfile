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
                sh 'sudo su -'
                sh 'wget https://services.gradle.org/distributions/gradle-6.2-bin.zip -P /tmp'
                sh 'unzip -d /opt/gradle /tmp/gradle-6.2-bin.zip'
                sh 'export GRADLE_HOME=/opt/gradle/gradle-6.2'
                sh 'export PATH=${GRADLE_HOME}/bin:${PATH}'
                sh '/opt/gradle/gradle-5.0/bin/gradle -v'
             }
         }
     }
}
