#ESB Modules

This example read the file that is generated by the Python socket in the Socket Sample present in python-server folder from here: https://github.com/edgars/wso2-hacks/tree/master/python-server

We added a Proxy that is a File System Reader, and we print in the console the payload using JavaScript:

[See the source here!](src/main/synapse-config/proxy-services/TransactionsFileListenerProxy.xml)

## For that example works!

You have to enable the VFS Transport receiver and sender. (CARBON_HOME/repository/conf/axis/axis2.xml):
```
    <transportReceiver name="vfs" class="org.apache.synapse.transport.vfs.VFSTransportListener"/>
    
    ...
    
    <transportSender name="vfs" class="org.apache.synapse.transport.vfs.VFSTransportSender"/>
```

You have to change your directory accordingly your local machine :)