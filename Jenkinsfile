pipeline{
agent {
label "slave2"
}
tools{
maven "m1"
}

stages{
stage('Build'){
steps{
echo 'Build started......................'
sh 'mvn clean install -DskipTests'
}
}
stage('Test'){
steps{
echo 'Testing.........................'
sh 'mvn test'
}
post{
always{
junit 'target/surefire-reports/*.xml'
archiveArtifacts 'target/*.jar'
}
}
}
stage('Run'){
steps{
echo 'Running.....................'
}
}


}
