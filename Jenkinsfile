stage('Docker Build') {
    steps {
        echo 'Building Docker image...'
        bat '"C:\\Users\\Harsh\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" build -t nodejs-jenkins-cicd:latest .'
    }
}

stage('Deploy') {
    steps {
        echo 'Deploying application...'
        bat '"C:\\Users\\Harsh\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" rm -f nodejs-jenkins-container || exit /b 0'
        bat '"C:\\Users\\Harsh\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" run -d -p 3001:3000 --name nodejs-jenkins-container nodejs-jenkins-cicd:latest'
    }
}