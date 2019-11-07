pipeline {
    agent {
        docker {
            image "ruby"
        }
    }
    stages {
        stages("Build") {
            steps {
                sh "bundle install"
        }
        stages("Tests") {
                steps { sh "bundle exec cucumber -p ci"}
            }
        }
    }
}