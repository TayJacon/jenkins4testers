pipeline {
    agent {
        docker {
            image "ruby:alpine"
        }
    }
    stages {
        stages("Build") {
            steps {
                sh "chmod +x build/alpine.sh"
                sh "./build/alpine.sh"
                sh "bundle install"
        }
        stages("Tests") {
                steps { sh "bundle exec cucumber -p ci"}
            }
        }
    }
}