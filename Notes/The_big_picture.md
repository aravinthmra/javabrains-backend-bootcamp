# The Big Picture

## The three tier architecture
                    Browser
    (Page load)<->          -> (REST call) 
CDN                                 Backend server
                                            -> Database

-> Here, with microservices, the backend server converts to usually comprise the following set-up

                        API Gateway
      <->                   <->                     <->
    Service A            Service B              Service C
      <->                   <->                     <->
    Database A          Database B              Databse C


## CDN (Content Delivery Network)
- stored on multiple servers in various locations
- routes the request to the server closest to the user
- faster than getting this from the origin server

![web-application-flow](Notes/assets/webapplication-flow.jpg)

## Web request - how it works?
- The browser send a request to the DNS (Domain Name System) server, to resolve the domain name of the URL to its corresponding IP address.
- The DNS server returns the IP address of the closest CDN edge server to the user's location.
- The CDN edge server checks its cache
  - If found in the cache, the CDN edge server returns the cached version
  - If not found in the cache, the CDN edge server sends a request to the origin server,
    - and the origin server return the requested content to the CDN edge server.

## Web page - what makes one?
- HTML page
- CSS assets
- Images
- JS assets
- Fonts


## References:-

### Link to the javabrains-bootcamp's git repo
https://github.com/koushikkothagal/java-backend-bootcamp

### Link to this notes-repo
https://github.com/aravinthmra/javabrains-backend-bootcamp
