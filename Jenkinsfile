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
                sh 'if [ ! -d "gradle" ] ; then git clone https://github.com/gradle/gradle-site-plugin.git gradle; fi'
            }
         }
     }
}
