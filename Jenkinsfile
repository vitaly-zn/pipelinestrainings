pipeline {
    agent any
    
    parameters {
        file(name: 'myFile', description: 'JSON file to use in build')
    }
    
    
    stages {
        
        stage('Checkout') {
            steps {
                script {
                    def isFileExists = fileExists('myFile')
                    println "SelectedFile=${myFile}"
                    println "isFileExists=${isFileExists}"
                }
            }
        }

        stage('Test') {
            steps {
                echo "node name: $NODE_NAME"
                
                echo "what myFile"
                sh "pwd"
                sh "ls -lah"
                sh "cat myFile" 
            }
        }
    }
}
