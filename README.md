⚙️ Dockerfile Overview
FROM nginx:alpine              # Use lightweight Nginx image
RUN rm -rf /usr/share/nginx/html/*   # Remove default Nginx content
COPY . /usr/share/nginx/html         # Copy your app files
EXPOSE 80                            # Expose port 80


👉 This Dockerfile builds a lightweight Nginx container that serves your index.html Todo app.

🚀 Commands to Build and Run
1️⃣ Build Docker Image
docker build -t todo-app .

2️⃣ Run Container
docker run -d -p 8080:80 todo-app


Now open 👉 http://localhost:8080

You’ll see your Todo app running 🎉

🧹 Optional Commands

Stop all running containers:

docker stop $(docker ps -q)


Remove all containers:

docker rm $(docker ps -a -q)


Remove all images:

docker rmi $(docker images -q)

💡 Highlights

Uses Nginx Alpine (very small image size)

Fully static app (HTML + CSS + JS)

Data stored in browser localStorage

Ideal for Docker beginners 🚀
