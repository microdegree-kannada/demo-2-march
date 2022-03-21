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
		echo "this is from feature-1"
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
