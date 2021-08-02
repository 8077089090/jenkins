///pipeline {
//agent {
//node { label 'workstation'}
 //label 'JAVA'
//  }
///agent any
 ///  stages {
///stage('Master Node') {
///agent {
///label 'MASTER'
///}
///steps {
///sh 'echo hello'
///}
///}
///stage ('Agent Node') {
///agent {
///label 'JAVA'
///}
///steps {
///sh 'echo world'
///}
///}
///}
///post {
///always {
///sh 'echo post steps'
///}
///}
///}

pipeline {
agent any
tools {
    maven 'maven'
    }
options { disableConcurrentBuilds() }
environment {
DEMO_URL = "google.com"
}
parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
        }
stages{
stage('one') {
environment {
DEMO_URL = "yahoo.com"
}
steps {
sh  'echo ${DEMO_URL}'
echo "PERSON = ${PERSON}"
}
}
stage('compile') {
input {
                message "Should we continue?"
                ok "Yes, we should."
                //submitter "alice,bob"
               // parameters {
              //      string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
             //   }
            }
steps {
sh 'mvn clean'
}
}
}
}