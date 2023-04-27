# kubernetes_lab3
Create 2 deployments in world namespace: in yaml
![Screenshot (1169)](https://user-images.githubusercontent.com/93229250/234781647-6d6161c6-6216-4922-b774-a87efa288711.png)

aisa with 2 replicas and image “husseingalal/africa:latest”
![Screenshot (1171)](https://user-images.githubusercontent.com/93229250/234781694-31520729-5b64-46c3-ba35-905064af39d5.png)

europe with 2 replicas and image “husseingalal/europe:latest”
![Screenshot (1170)](https://user-images.githubusercontent.com/93229250/234781739-ffdd0cc3-eba9-4909-811b-065004247220.png)

result:
![Screenshot (1173)](https://user-images.githubusercontent.com/93229250/234781880-67b9a840-391d-40cc-9cf2-6452f34218ac.png)

Using kubectl expose create ClusterIP Services for both Deployments for port 8888 and target port 80 . The Services should have the same name as the Deployments.
![Screenshot (1176)](https://user-images.githubusercontent.com/93229250/234782015-2979480a-8dc9-4e27-8583-991d931bbc7a.png)

Create a new Ingress resource called world for domain name world.universe.mine . The domain points to the K8s Node IP via /etc/hosts . The Ingress resource should have two routes pointing to the existing Services:
![Screenshot (1185)](https://user-images.githubusercontent.com/93229250/234782189-b1124314-cd45-4304-9030-c68250ff375d.png)
![Screenshot (1184)](https://user-images.githubusercontent.com/93229250/234782224-b788c632-7255-4164-9055-dbd2e31f1adf.png)


http://world.universe.mine/europe/
![Screenshot (1187)](https://user-images.githubusercontent.com/93229250/234782460-53dcb723-0db6-43b0-b559-99accd1fd5d8.png)

and

http://world.universe.mine/africa/
![Screenshot (1186)](https://user-images.githubusercontent.com/93229250/234782490-24b4fc82-fdee-4999-acc6-69c9096bac09.png)
