node{
    stage('code checkout'){
        git 'https://github.com/Vaibhav3101mankar/addressbook-demo.git'
    }
    
    stage('clean.. compile... test... package...'){
        sh 'mvn clean package'
    }       
    stage('deploy to tomcat'){
 deploy adapters: [tomcat9(credentialsId: 'v', path: '', url: 'http://18.234.147.186:8088/')], contextPath: 'Pipeline', war: '**/*.war'   }
}
