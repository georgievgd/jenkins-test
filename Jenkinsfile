def label = "python_agent"
//def label = "test"

parameters {
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')

    file(name: "FILE", description: "Choose a file to upload")
}

timestamps {
      logstash {
        node(label) {

            stage('Source') {
                checkout scm
            }

            stage('Build') {
                sh "sleep 1s;"
                sh "whoami;pwd;ls -al;"
            }

            stage('Check Styles') {
                sh "sleep 1s;"
            }
            
            stage('Test') {
                sh "sleep 1s;"
                try {
                    sh "python --version"
                }
                catch (exc) {
                    echo 'Something failed, I should sound the klaxons!'
                }
            }
            
            stage('Documentation') {
                sh "sleep 1s;"
            }

            stage('Deploy') {
                sh "sleep 1s;"
            }
        }
    }
}
