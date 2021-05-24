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
                sh 'echo if [ ! -d "gradle" ] > script.sh' 
                sh 'echo then git clone https://github.com/gradle/gradle-site-plugin.git gradle >> script.sh'
                sh 'echo fi >> script.sh'
                sh 'chmod +x script.sh'
                sh './script.sh'
                sh './gradle/gradlew -v'
            }
         }
     }
}
