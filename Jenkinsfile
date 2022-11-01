import java.text.SimpleDateFormat

def releaseDate = new Date().format("yyyy-w")

pipeline {
    agent any

//     environment {
//                 VERSION = "${releaseDate}"
//             }

    stages {
        stage('build') {
            steps {
                sh "./gradlew assemble -DVERSION=${releaseDate}"
            script {
                    println "------------"
                    def date = releaseDate
                    println "date is " + date
                    println "------------"
                }
//                 sh "git tag -a ${getDate()} -m \"Bump version to ${getDate()}\""
//                 sh "git push origin ${getDate()}"
                sh 'echo ========================'
                sh "echo ${releaseDate}"
                sh 'echo ========================'
                sh 'find . -name "*.jar"'
            }
        }
    }
}