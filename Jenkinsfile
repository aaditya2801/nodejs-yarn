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
                sh 'echo if [ ! -d "gradle" ] > scirpt.sh' 
                sh 'then git clone https://github.com/gradle/gradle-site-plugin.git gradle >> script.sh'
                sh 'fi >> script.sh'
            }
         }
     }
}
