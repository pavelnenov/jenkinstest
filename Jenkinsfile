import java.text.SimpleDateFormat


pipeline {
    agent any
    stages {
        stage('build') {
            steps {
//                 sh './gradlew assemble'
                println "------------"
                println getDate()
                println "------------"
                sh 'echo ========================'
                sh "echo ${getDate()}"
                sh 'echo ========================'
            }
        }
    }
}

def getDate() {
    def date = new Date().format("yyyy-w")
    return date
}