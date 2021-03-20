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
}

    post{
        always{
            archiveArtifacts artifacts: '/Users/alexeykozlov/Documents/draft/target/output/**'
            sh "docker-compose down"
}
    
}

}
