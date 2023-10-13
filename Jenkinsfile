pipeline{
 
    agent any
    tools{
        maven "mvn"
    }

    stages
        stage ("Pull code  from VCS repo"){
            steps{
                script{
                    git "https://github.com/Haykelyazidi/Gestion.git"
                }
            }
        }
        stage ("MAVEN build"){
            steps{
                script{
                    sh 'mvn clean package'
                }
            }
        }
        stage("RUN SELENIUM TEST"){
            steps{
                script{
                    sh 'mvn clean test'
                }
            }
        }


}
