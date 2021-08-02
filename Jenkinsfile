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

pipiline {
agent any
environment {
DEMO_URL = "google.com"
}
stages{
stage('one') {
steps {
sh  'echo ${DEMO_URL}'
}
}
}
}