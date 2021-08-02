pipeline {
agent {
//node { label 'workstation'}
  label 'JAVA'
   }
   stages {
stage('Master Node') {
steps {
sh 'echo hello'
}
}
stage ('Agent Node') {
steps {
sh 'echo world'
}
}
}
}