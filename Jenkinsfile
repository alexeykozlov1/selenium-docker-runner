pipeline{
    agent any
    stages{
    
        stage("Pull lates image"){
            steps{
                sh "docker pull alexeykozlov1988/selenium-grid-docker"
}
}
        stage("Start Grid"){
            steps{
            sh "docker-compose up -d --scale chrome=20 firefox"
}
}
        stage("Run Test"){
            steps{
            sh "docker-compose up testScope1"
}
}
}

    post{
        always{
            archiveArtifacts artifacts: 'output/**'
            sh "docker-compose down"
}
    
}

}
