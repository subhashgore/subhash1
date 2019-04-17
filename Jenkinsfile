pipeline {
    agent {
        
       lable  "slave"
    
    } 
    stages {
        stage('checkout from GIT') { 
            steps {
                
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '324f3bf3-f69a-402e-96a1-87367fb9fde0', url: 'https://github.com/subhashgore/subhash1.git']]])
               
            }
        }
        stage('Test') { 
            steps {
                echo " hello from test "
                sh "mvn clean"
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn deploy"
            }
        }
    }
}
