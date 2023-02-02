command
--------
kubectl taint node node-1 key=value:NoSchedule - this command used to give taint for node

if you creating any pod now it will not schedule/ place on that purticular node 



to remove taint or untaint
---------------------------
kubectl taint node nod-name key=value:tainteffect-

or 

kubectl taint node ip-172-31-18-186.ap-south-1.compute.internal key=value:NoSchedule-


check tainted or not
-----------------------
kubectl describe node node-name

beneth u will be able to find taint


services:
--------
kubernetes support 4 main services
- cluster ip - which going to allocate internal ipaddress, this service will be common interface for all pods wich pertained to that.
- nodeport - by using this service we can access the application from ouside as well
- loadbalancer - this will be give unified access link, this will be distribute load between nodes.
- externalname - connect application with external service. for eg: we have service, which using db from ouside of kubecluster
                                                                eg: connect between tow namespace service.

