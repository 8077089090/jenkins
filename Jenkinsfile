pipeline {
//agent {
//node { label 'workstation'}
 //label 'JAVA'
//  }
agent none
   stages {
stage('Master Node') {
agent {
label 'MASTER'
}
steps {
sh 'echo hello'
}
}
stage ('Agent Node') {
agent {
label 'JAVA'
}
steps {
sh 'echo world'
}
}
}
post {
agent any
always {
sh 'echo post steps'
}
}
}