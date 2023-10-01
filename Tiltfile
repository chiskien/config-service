custom_build(
    ref = 'config-service',
    command = 'mvn spring-boot:build-image -D imageName=${EXPECTED_REF}',
    
    deps= ['src', 'pom.xml']
)
 
k8s_yaml(['kubernetes/deployment.yml', 'kubernetes/service.yml'])

k8s_resource('config-service', port_forwards=['8888'])