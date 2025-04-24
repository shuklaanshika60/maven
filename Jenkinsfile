node {
    def mvnHome = tool 'MVN'
    
    stage('Checkout') {
        git branch: 'main', credentialsId: 'da3d7d85-1cbf-4292-b2c3-5c6f1f716de8', url: 'https://github.com/GAURAVETH/MEVAN_PROJECT.git'
    }
    
    stage('Validate') {
        bat "${mvnHome}\\bin\\mvn validate"
    }
    
    stage('Compile') {
        bat "${mvnHome}\\bin\\mvn compile"
    }

    stage('Test') {
        bat "${mvnHome}\\bin\\mvn test"
    }

    stage('Package') {
        bat "${mvnHome}\\bin\\mvn package"
    }

    stage('Install') {
        bat "${mvnHome}\\bin\\mvn install"
    }

    stage('Verify') {
        bat "${mvnHome}\\bin\\mvn verify"
    }

    stage('Site') {
        bat "${mvnHome}\\bin\\mvn site"
    }

    stage('Clean') {
        bat "${mvnHome}\\bin\\mvn clean"
    }
}
