pipeline{
    agent any
    stages{
        stage("Start Grid"){
            steps{
            sh "docker-compose up -d chrome firefox"
}
}
        stage("Run Test"){
            steps{
            sh "docker-compose up search-module test-form"
}
}
        stage("bring grid down"){
            steps{
                sh "docker-compose down"
}
}
}
}
