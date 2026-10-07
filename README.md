# CST8915 Lab 3: CST8915 Full-stack Cloud-native Development: Deploying the Algonquin Pet Store on Azure

**Student Name**: Eric Tieu
**Student ID**: 041273376
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Fall 2026

---

## Demo Video

🎥 [Watch Demo Video](https://www.youtube.com/watch?v=Yxy6zaefhoM)

---
### Notes
Static Web App regions were not available for my student subscription. I used the previous method (Lab 2) to host the store front on a VM. Environment variables are shown in the VS Code window in the video since I couldn't `Show environment variables declared in the GitHub Actions workflow for the store-front.`

### Order Service [Link](https://github.com/tieu0014/order-service)

### Product Service [Link](https://github.com/tieu0014/product-service)

### Store Front [Link](https://github.com/tieu0014/store-front)

### What challenges did you encounter when configuring environment variables in the GitHub Actions workflow?
No challenges were encountered since static web apps were not available with my available regions. I successfully deployed the store front on a `Node - 24-lts` runtime web app, but content only showed the default page for web apps. I attempted to fix this issue by adding the startup command `pm2 serve /home/site/wwwroot --no-daemon --spa` to the workflow as per [this](https://stackoverflow.com/questions/67185936/vue-js-does-not-start-in-azure-app-service) proposed solution, but this only showed all the files for the web app, not the hosted page. Adding [this](https://stackoverflow.com/questions/66924180/application-is-not-loading-when-deployed-via-azure-app-service/66947617#66947617) `npx serve -s` proposed solution lead to a 404 error.

### How does deploying microservices on Azure Web App Service differ from running them locally?
Each service runs on its own virtual environment. In Lab 1 we ran all the services coupled as one codebase on the same virtual environment. If a component failed in the Lab 1 environment the entire app would crash, unlike Lab 2, and Lab 3. Because we deployed them as separate microservices we needed to communicate using URLs utilizing environment variables.

### Why is it important to use environment variables for configurations in a cloud environment?
If we didn't use environment variables each time a microservice is run we would have to manually change the connection strings. On a large scale this would be an issue especially for rapid elasticity when machines are being deployed and decommissioned rapidly.
