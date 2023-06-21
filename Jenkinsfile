pipeline{

    agent any


    tools{
       maven 'maven'
    }
    

    stages{
        stage('build'){
            steps{
                echo 'this is build the app job'
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                echo 'this is test the app job'
                sh 'mvn test'
            }
        }
        stage('package'){
            steps{
                echo 'this is package the app job'
                sh 'mvn package'
            }
        }
    }
    
    post{
        always{
            echo 'This pipeline has completed...'
        }
        
    }
    
}


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
