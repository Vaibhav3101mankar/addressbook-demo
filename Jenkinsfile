node{
    stage('code checkout'){
        git 'https://github.com/Vaibhav3101mankar/addressbook-demo.git'
    }
    
    stage('clean.. compile... test... package...'){
        sh 'mvn clean package'
    }
    
    stage('deploy to tomcat'){
        deploy adapters: [tomcat9(credentialsId: 'tomcat-creds', path: '', url: 'http://44.207.5.0:8085/')], contextPath: 'addressbook', war: '**/*.war'
    }
}
