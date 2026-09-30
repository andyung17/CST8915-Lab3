# CST8915 Lab 3: Deploying the Algonquin Pet Store on Azure

**Student Name**: Andy Ung <br/>
**Student ID**: 041299387 <br/>
**Course**: CST8915 Full-stack Cloud-native Development <br/>
**Semester**: Fall 2026 <br/>

---

## Demo Video

🎥 [Watch Demo Video](https://youtu.be/Nq5pd__w24s)

---

## Connected Repos (Lab2)

```order-service``` - [Repo](https://github.com/andyung17/order-service-lab2-demo)
<br/>```product-service``` - [Repo](https://github.com/andyung17/product-service-lab2-demo)
<br/>```store-front``` -  [Repo](https://github.com/andyung17/store-front-lab2-demo)
<br/>```rabbitmq``` - [Repo](https://github.com/andyung17/RabbitMQ-lab2-demo)

---

## New Modified Repos (Lab3)
```product-service``` - [Repo](https://github.com/andyung17/product-service-lab3-demo)
<br/>```store-front``` -  [Repo](https://github.com/andyung17/store-front-lab2-demo)

---

## Reflection Questions

1. What challenges did you encounter when configuring environment variables in the GitHub Actions workflow?

Did not encounter any issues with configuring the environment variables. Instead of deploying through static web apps, used App Services and the process was smooth.

2. How does deploying microservices on Azure Web App Service differ from running them locally?

When deploying microservices to Azure Web App Service, this allows us to use the 4th Factor: Backing Services. This enables us to swap between instances of a service if need be. Deploying the microservices allows on-demand access to the services through `http` endpoints. Running them locally means only IOT devices within the same network can interact with it. Once deployed, theres a lot more flexibility in scaling the application horizontally compared to locally (realistically can only vertically scale).

3. Why is it important to use environment variables for configurations in a cloud environment?

It is important to keep configurations in environment variables to follow Factor 3: Configurations. This gives the code and configuration better portability and security. This even makes it possible to have the 4th factor of backing services as without code changes, an app can swap different services. While code remains on privately owned public hosted code repositories ensure that any leaks or security compromises does not leave the system at risk.

---

## Challenges and Learnings (Optional)

## Acknowledgments
- https://fastapi.tiangolo.com/tutorial/cors/#use-corsmiddleware
- For the process of setting up the `deploy.yml` I had AI help to create the file for deployment