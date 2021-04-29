pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }

        stage('Test') {
           steps {
            echo 'Testing'
           }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }

        stage('Clean') {
            steps {
//                 cleanWs(
//                     cleanWhenAborted: true,
//                     cleanWhenFailure: true,
//                     cleanWhenNotBuilt: true,
//                     cleanWhenSuccess: true,
//                     cleanWhenUnstable: true,
//                     cleanupMatrixParent: true,
//                     disableDeferredWipeout: true,
//                     deleteDirs: true
//                 )
                    sh("ls -al ${env.WORKSPACE}")
                    sh("cd ..")
                    deleteDir()  // clean up current work directory
                    sh("ls -al ${env.WORKSPACE}")
            }
        }
    }
}