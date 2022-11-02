import java.text.SimpleDateFormat

def releaseDate = new Date().format("yyyy-w")

pipeline {
    agent any


//     triggers {
// //         parameterizedCron('''
// //            9 15 * * * %RELEASE_BUILD=true
// //         ''')
//     }


    stages {
        stage('build') {

            steps {
                sh "./gradlew build -DRELEASE_VERSION=${releaseDate}"
            script {
                    echo sh(script: 'env|sort', returnStdout: true)
                    println "0000000000000"
                    def causes = currentBuild.getBuildCauses()
                    causes.each {
                    println "111111111111"
                        echo "$it"
                    println "111111111111"
                    }
                    println "------------"
                    def date = releaseDate
                    println "date is " + date
                    println "------------------------------------------------------------"

                    def str = "paf %s what"
                    println str % "YO"


                }
                sh "git tag -a ${releaseDate} -m \"Bump version to ${releaseDate}\""
                sh "git push origin ${releaseDate}"
                sh 'echo ========================'
                sh "echo ${releaseDate}"
                sh 'echo ========================'
                sh 'find . -name "*.jar"'
                sh "echo asd  ${env.RELEASE_BUILD}"
            }
        }
    }
}