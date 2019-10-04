podTemplate(label: 'slavek8s', 
    containers: [
        containerTemplate(
            name: 'golang',
            image: 'golang',
            ttyEnabled: true,
            command: 'cat'
        )
    ]
) {
    node ('slavek8s') {

        stage 'Switch to Utility Container'
        container('golang') {

          sh ("go version")

        }
    }
}
