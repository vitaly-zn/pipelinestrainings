properties {[
        parameters {[
                [$class: 'WHideParameterDefinition', name: 'USER_NAME', defaultValue: 'me123', description: ''],
                // Specifies the location, relative in the workspace,
                // where the uploaded file will be placed (for example, like "jaxb-ri/data.zip")
                file(name: 'myFile', description: 'Description for my file'),
                string(name: 'myString', defaultValue: '', description: 'Description for my string', trim: true)
        ]}
]}

pipeline {
    agent {
        node {
            label 'built-in'
        }
    }
    stages {
        stage('Test') {
            steps {
                script {
                    println 'All available parameters:'
                    println "USER_NAME=${params.USER_NAME}"
                    println "file=${params.myFile}"
                    println "string=${params.myString}"
                }
            }
        }
    }
}
