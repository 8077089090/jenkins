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
environment {
DEMO_URL = "google.com"
}
stages{
stage('one') {
environment {
DEMO_URL = "yahoo.com"
}
steps {
sh  'echo ${DEMO_URL}'
}
}
}
}