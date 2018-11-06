# origami-simple

This is an origami sample with backward compatibility of opencv compiled with libc 2.23 and no ffmpeg 

```
:dependencies [   
  [origami "4.0.0-beta6" :exclusions [opencv/opencv-native]]
  [opencv/opencv-native-ubuntu16-noffmpeg "4.0.0-beta"]
  [org.clojure/clojure "1.8.0"]]
```

or deps.edn 

```
{:mvn/repos
 {
 	"vendredi" {:url "https://repository.hellonico.info/repository/hellonico/"}
 }
 :deps { 
 	origami {:mvn/version "4.0.0-beta6"}
    opencv/opencv-native-ubuntu16-noffmpeg {:mvn/version "4.0.0-beta"}
 }
}
```

# docker 

This also allows to run directly on a docker container and a Dockerfile is included here.

```
docker build -t my-origami-app .
docker run -it --name running-origami-app my-origami-app
```
