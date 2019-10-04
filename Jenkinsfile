podTemplate(label: 'slave', 
    containers: [
        containerTemplate(
            name: 'golang',
            image: 'golang',
            ttyEnabled: true,
            command: 'cat'
        )
    ]
) {
    node ('slave') {

        stage 'Switch to Utility Container'
        container('golang') {

          sh ("sleep 20m")

        }
    }
}
