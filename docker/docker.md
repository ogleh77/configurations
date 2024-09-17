Docker volumes are 3

- host volume is the volume you dirrectly mounted the container volume
- annonymous volume  docker run -v container volume
- name volume is the imporefment of the annonymous volume you naming the folder name  and it's defind like this 
   - docker volume create data
   - docker run  -v data:/var/lib/mysql/data
