# BIRT - An open source technology platform used to create data visualizations and reports that can be embedded into rich client and web applications.

# Install

## Direct

    docker run --name birt-viewer -v ./install/birt-viewer:/usr/local/tomcat/webapps/birt/report -d birt-viewer

## docker-compose.yml

    version: "2"
    
    services:
    
      birt-viewer:
        container_name: birt-viewer
        image: psimonov/birt-viewer
        volumes:
          - ./install/birt-viewer:/usr/local/tomcat/webapps/birt/report
        ports:
          - 8080:8080