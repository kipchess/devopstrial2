node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t devexam:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'kipchess' -p '8191@chess' "
sh "docker tag devexam:latest kipchess/devexam:latest"
sh "docker push kipchess/devexam:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
