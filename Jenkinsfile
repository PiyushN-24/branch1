pipeline {
        agent any
        stages {
            stage('Checkout') {
                steps {
                        checkout scm
                      }}
                stage('Build') {
                   steps {
                          sh '/home/swapnil/Documents/DevOps-Software/apache-maven-3.9.4/bin/mvn install'
                         }}
                stage('Deployment'){
                    steps {
                        script {
                         if (env.BRANCH_NAME == 'master')
                        {
                        echo 'Hello from MASTER branch'
                        }
                        else if (env.BRANCH_NAME == 'dev')
                        {
                        echo 'Hello from DEV branch'
                        }
                        else {
                        sh "echo 'Hello from ${env.BRANCH_NAME} branch!'"
                        }
                        }
}
}
}    
}
