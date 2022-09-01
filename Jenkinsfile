node {

    checkout scm

     
        
        withCredentials([usernamePassword( credentialsId: 'docker-hub-credentials', usernameVariable: 'USER', passwordVariable: 'PASSWORD')]) {
        def registry_url = "registry.hub.docker.com/"
        bat "docker login -u $USER -p $PASSWORD ${registry_url}"
            docker.withRegistry("http://${registry_url}", "docker-hub-credentials"){
                def customImage = docker.build("carneirolionel/docker-webapp")
            // Push your image now
        
        /* Push the container to the custom Registry */
        customImage.push()
    }
        }
}
