# CST8915 Lab 3: CST8915 Full-stack Cloud-native Development: Deploying the Algonquin Pet Store on Azure

**Student Name**: Eric Tieu
**Student ID**: 041273376
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Fall 2026

---

## Demo Video

🎥 [Watch Demo Video]([https://www.youtube.com/watch?v=3-h5xMdKDA4](https://www.youtube.com/watch?v=WV9pk__gEtY))

---

## Technical Explanations

### Order Service [Link](https://github.com/tieu0014/order-service)

### Product Service [Link](https://github.com/tieu0014/product-service)

### Store Front [Link](https://github.com/tieu0014/store-front)

### Environment Variables
Why is it important to use environment variables instead of hard-coding configurations in your application?<br>

"It ensures separation between the code and the configuration for better portability and security"

### Separate Repositories
Why is it important to have separate repositories for each microservice? How does this help maintain independence and scalability of each service?<br>

"Each service can be deployed separately without having to deploy the entire system", "changes in one service will have minimal or no impact on other services". Possibly multiple instances of of the microservice can be deployed at a time, allowing it to scale with the number of instances.
