# My HTML Website Deployment Project 🚀

Welcome to my **HTML website deployment project**, where I combined **Docker, Nginx, GitHub Actions CI/CD, and AWS** to bring a fully functional website online in a professional and automated way.

---

## Project Overview 🌐

This project demonstrates a complete **DevOps workflow** for deploying a static website:

1. Code is stored in **GitHub**.
2. Docker is used to containerize the website.
3. GitHub Actions handles CI/CD to automate the deployment.
4. The website is deployed on an **AWS Ubuntu server** using Docker containers.
5. Users can access the live website via the server's public IP.

---

## Key Features ✨

- **Containerized deployment** using Docker  
- **Automated CI/CD** pipeline with GitHub Actions  
- **Nginx server** serving the website inside a container  
- **AWS integration** for scalable deployment  
- Simple, lightweight **HTML/CSS website**  

---

## CI/CD Pipeline Overview 🔄

```text
GitHub → Docker → AWS → Live Website
````

1. **GitHub**: Commit and push your website code.
2. **Docker**: Build the website image.
3. **GitHub Actions**: Automatically push Docker image to Docker Hub and deploy to AWS.
4. **AWS Server**: Pulls the latest Docker image and runs the container.
5. **Live Website**: Accessible to the world!

---

## Steps I Followed 🛠️

1. **Prepare HTML Website**

   * Created `index.html`, `style.css`, and images.

2. **Create Dockerfile**

   * Used official `nginx:alpine` base image.
   * Copied website files to `/usr/share/nginx/html`.

3. **Build & Test Locally**

   ```bash
   docker build -t my-website .
   docker run -d -p 2020:80 my-website
   curl http://localhost:2020
   ```

4. **Push to Docker Hub**

   ```bash
   docker tag my-website:latest <dockerhub-username>/my-website:latest
   docker push <dockerhub-username>/my-website:latest
   ```

5. **Setup AWS Ubuntu Server**

   * Installed Docker & Docker Compose
   * Exposed port 80 for HTTP

6. **Automate Deployment with GitHub Actions**

   * CI/CD workflow builds, pushes Docker image, and deploys to AWS automatically.

---

## Directory Structure 📂

```
html-website-project/
├── Dockerfile
├── index.html
├── style.css
├── images/
└── .github/workflows/ci-cd.yml
```

---

## Live Demo 🔗

Once the CI/CD pipeline runs, the website is live at:

```
http://<AWS_PUBLIC_IP>:2020
```

---

## Technologies Used 🖥️

* **HTML & CSS** – front-end
* **Nginx** – web server
* **Docker** – containerization
* **GitHub Actions** – CI/CD
* **AWS Ubuntu Server** – deployment
* **Docker Hub** – container registry

---

## Lessons Learned 🎯

* Setting up **CI/CD** drastically reduces deployment time.
* Using **Docker + Nginx** ensures consistency across environments.
* Automating deployment improves reliability and scalability.
* Understanding **AWS networking** (security groups, public IPs, ports) is crucial.

---

## Visual Pipeline Diagram 🖼️

Optional: Add a simple visual diagram of the pipeline here.

---

## Conclusion 🏁

This project represents a **real-world DevOps workflow**, combining coding, containerization, CI/CD, and cloud deployment. It's a **fully automated website deployment pipeline**, and the skills learned here are **directly applicable in professional DevOps roles**.

---

```

---


