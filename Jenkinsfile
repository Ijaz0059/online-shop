node{

    stage('SCM Checkout')
    {
        git credentialsId: '4cc785e9-441d-4818-a248-2bfb2148004d', url: 'https://github.com/Ijaz0059/online-shop.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'docker-compose build'
        sh 'docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u upasanatestdocker -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'docker login -u "ijaz0059" -p "B4u@0059" docker.io'
             //sh 'docker push upasanatestdocker/mysql'
             //sh 'docker push upasanatestdocker/job1_web1.0'
             sh 'docker push ijaz0059/ecommerce'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
