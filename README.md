# Final-Project-Assessment-for-Scalefocus-Academy
1. Installed prerequisites jenkins,kubernetes,helm.
2. Clonning the worpress chart to my repo
3. Fixing the valuse.yaml, replacing type: **LoadBalancer to type: ClusterIP**
4. Setting up helm (upgrading dependencies)
5. install wp using helm with this command: 
 **helm install wp charts/bitnami/wordpress**
6. Changing the pod port because some issues orccured with this command:
**kubectl port-forward --namespace default svc/wp-wordpress 3030:80**
7. Open the browser one localhost:3030 and I was greeted with this:

![wordpress page](https://github.com/DekoTheKing/Final-Project-Assessment-for-Scalefocus-Academy/assets/101192308/944456cf-101f-44e5-91d1-3569e05fab9c)

for some reason it bypassed the admin login page not sure why.

8. Next up is the jenkins pipeline 
For this task I needed to install the kubernetes CLU plugin

![plugin install](https://github.com/DekoTheKing/Final-Project-Assessment-for-Scalefocus-Academy/assets/101192308/b89969a5-6c0c-48a8-890f-77f8f717a403)

9. After the plugin is installed I countinued with the Jenkinsfile
I've set up jeninks pipeline to use github repo and made a pipline script unfortunately it didn't work at first but after many tries to modify the Jenkinsfile it worked

![it worked XD](https://github.com/DekoTheKing/Final-Project-Assessment-for-Scalefocus-Academy/assets/101192308/cbdcc53a-1d53-4448-b44c-0bc2a58ae9de)

After this I did a manual port forwarding with same command above
And here is the output of the final result.

![final wordpress](https://github.com/DekoTheKing/Final-Project-Assessment-for-Scalefocus-Academy/assets/101192308/15b32d7c-f605-412c-97dd-25709f20794e)
