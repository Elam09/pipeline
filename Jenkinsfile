pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
    stage('Clone') {
         steps {
            checkout([$class: 'GitSCM',
                branches: [[name: '*/master' ]],
                extensions: scm.extensions,
                userRemoteConfigs: [[
                    url: 'https://github.com/Elam09/pipeline.git',
                    credentialsId: '69991f0e-2516-4f07-841b-99ab191c960b'
                ]]
            ])

            //List all directories
            sh "ls -lart ./*"
         }
      }
}

