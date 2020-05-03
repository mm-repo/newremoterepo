pipeline {
agent any
stages{
    
    stage('compile stage'){
        step{ withMaven(maven :'maven_3.6.2'){
            sh 'mvn clean compile'
        }
    }
}

    stage('testing stage'){
        step { withMaven(maven :'maven_3.6.2'){
            sh 'mvn test'
        }
    }
}
    stage('deploy stage'){
        step{ withMaven(maven :'maven_3.6.2'){
            sh 'mvn deploy'
        }
    }
}
}
}
