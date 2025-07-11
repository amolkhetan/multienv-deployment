# MultienvApp
This App is basically for displaying Dev and Prod Tickets.
It used flask for backend and react for frontend
Port details:
•	Frontend: 3000
•	Development Backend: 3001
•	Production Backend: 3002

URLs using local hoste
•	Development Environment: http://localhost:3000/dev
<img width="1909" height="351" alt="image" src="https://github.com/user-attachments/assets/23b02a31-4a8d-485e-8e2e-d9f4ec9a9ebc" />

•	Production Environment: http://localhost:3000/prod
<img width="1916" height="444" alt="image" src="https://github.com/user-attachments/assets/4b5da27e-1016-430e-97ce-ee65a24ae067" />

•	Frontend Dashboard: http://localhost:300
<img width="1911" height="373" alt="image" src="https://github.com/user-attachments/assets/9693513d-247b-4c7b-84bf-96f3d6fa963b" />



**1. Set Up on Local**
- Install Docker and docker compose, if not on installed already. It can be checked using command
  docker -version
  Also ensure that docker engine is running on your local.

  Note: Same can be done on EC2 by using launch instance.

  **2. Docker Configuration**
  3 docker files are created (1 for backend dev, one for backend prod and 1 for frontend)., refer repo to check dockerfiles.
  1 docker compose is created for 3 docker files created earlier.

  Environment seciton is added for backend dev and prod to add mongodb uri like below:
  environment:
      - MONGO_URI=mongodb+srv://amolkhetan:fhcj60zmtKUsdXcZ@amol-cluster.smlmwf1.mongodb.net/proddb
  
  **3. Application Deployment**
  - build image using "docker compose build"
    <img width="940" height="494" alt="image" src="https://github.com/user-attachments/assets/de59dbbd-f65f-467d-a71d-e308e87bca62" />

  - Run is using "docker compose up"
    <img width="940" height="528" alt="image" src="https://github.com/user-attachments/assets/880ebee1-2cc9-48ce-9f53-43bfcb205be0" />

  - Dev Backend
    <img width="1908" height="679" alt="image" src="https://github.com/user-attachments/assets/a386d38a-d476-4d44-ac59-0cb075dc7a96" />

  - Prod Backend
    <img width="1906" height="681" alt="image" src="https://github.com/user-attachments/assets/4e4e97e2-d170-4ac2-9e0c-dce698b201fb" />

  - frontend
   <img width="1919" height="638" alt="image" src="https://github.com/user-attachments/assets/1975e7bb-b56d-4cb3-8aa2-1c9289c03f74" />


   **4. Issue Faced**
   - while running container faced 2 issues:
     1. mondo db uri was missing for backend
     Fixed: by adding environment section in docker compose
     3. apiurl was missing for frontend
     Fixed: Ticket.js to use the url correctly



