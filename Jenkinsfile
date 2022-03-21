pipleine {
    agent any
    tools{
        maven "maven.8"
        jdk
    }
    stages {
        stage ("checkout"){
            steps {
                sh "git clone"
                echo ""
            }
        }
        stage ("build"){
            steps {
                sh "mvn clean install"
            }
        }
        stage ("test"){
            steps {
                sh "mvn test"
            }
        }
        post {
             {
                junit "**/surefireplugin/*.xml"
            }
        }
    }
}
