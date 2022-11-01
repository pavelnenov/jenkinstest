import java.text.SimpleDateFormat


pipeline {
    agent any
    stages {
        stage('build') {
            steps {
//                 sh './gradlew assemble'
                println "------------"
                println getDate()
                def currentDate = getDate()
                println "------------"
                sh 'echo ========================'
                sh "echo ${currentDate}"
                sh 'echo ========================'
            }
        }
    }
}

def getDate() {
    def date = new Date().format("yyyy-w")
    return date
}