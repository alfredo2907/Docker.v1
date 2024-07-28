#Arsitektur Docker Container terdiri dari : 
Docker Client : Interface CLI yang digunakan untuk berkomunikasi dengan dockerd
Docker Daemon (dockerd) : Yang mendengar request client melalui docker API. Dimana dockerd juga yang bertanggungjawab atas mengelola object seperti images, containers, network dan volume
Docker Registry : Repo dari images
Images : Sebuah template yang bersifat read-only yang digunakan untuk membuat container. 1 images dapat digunakan di beberapa kontainer
Container : Instance dari image yang berjalan 
