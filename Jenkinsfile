node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {

        def customImage = docker.build("carneirolionel/docker-webapp")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
