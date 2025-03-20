# The World Avatar (TWA) Material and Product Passport (MPP)
The structure of this passport aligns with the OntoMatPassport ontology, developed in the JIDEP project, to represent material and product passports.

## Setup
### Stack-manager
#### Secrets
In the [stack-manager secrets](stack-manager/inputs/secrets/) directory, include the secrets file required by stack-manager, following instructions in the [stack-manager repository](https://github.com/TheWorldAvatar/stack/tree/main/stack-manager), which are the four files below: 
- `postgis_password`
- `geoserver_password`
- `mapbox_api_key`
- `mapbox_username`

#### Configuration
In [ui-settings.json](stack-manager/inputs/data/vis-resources/config/ui-settings.json), replace `localhost` with `IPv4 Address` which can be found by running in cmd:
```cmd
ipconfig
```

### Stack-data-uploader
Download and place the required ontology rdf files into the stack-data-uploader's [`inputs/data/kg/ontology`](stack-data-uploader/inputs/data/kg/ontology/) directory, following instructions [here](stack-data-uploader/inputs/data/kg/ontology/README.md).

## Deployment 
### Starting the stack-manager
To deploy the Material and Product Passport (MPP) tech stack, a default stack-name `mpp` is pre-configured.

In the [stack-manager](stack-manager) directory, run the command below to spin up the tech stack,
```
./stack.sh start mpp
```

### Uploading data
Once the stack-manager is fully spin up. In the [stack-data-uploader](stack-data-uploader) directory, run the command to upload data:
```
./stack.sh start mpp
```

## Visualisation
The visualisation can be accessed at this endpoint
```
http://localhost:3838/visualisation/
```