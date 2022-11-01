import java.text.SimpleDateFormat


pipeline {
    agent any
    stages {
        stage('build') {
            steps {
//                 sh './gradlew assemble'
            script {
                    println "------------"
                    def date = getDate()
                    prinln "date is " + date
                    println "------------"
                }
//                 sh "git tag -a ${getDate()} -m \"Bump version to ${getDate()}\""
//                 sh "git push origin ${getDate()}"
//                 sh "echo ${getDate()}"
//                 sh 'echo ========================'
            }
        }
    }
}

def getDate() {
    def date = new Date().format("yyyy-w")
    return date
}