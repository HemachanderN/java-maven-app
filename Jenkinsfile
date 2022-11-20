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

}
}
stage('Test'){
steps{
echo 'Testing.........................'

}
post{
always{
echo 'Post Actions.........................'
}
}
}
stage('Run'){
steps{
echo 'Running.....................'
}
}


}
