# Container Observability Report

## 1. Application Deployment

- Container name: `client-website`
- Image: `nginx`
- Host port: `8080`
- Container port: `80`

## 2. HTTP Traffic Testing

Three HTTP requests were sent to the Nginx web server using `curl`.

- Successful request 1: [Enter the result]
- Successful request 2: [Enter the result]
- Successful request 3: [Enter the result]
- Request to `/hidden-admin-page`: [Enter the result]

The expected results are HTTP 200 for the successful requests and HTTP 404 for the missing page.

## 3. Application Logs

Command executed:

`docker logs client-website`

### HTTP 404 Error Log

Paste the exact line from your terminal that records the `/hidden-admin-page` request and its 404 status.

[Paste your actual 404 log line here.]

### Why Application Logs Are Important

Application logs help engineers identify which requests succeeded and which ones failed. They provide useful details about errors, allowing engineers to investigate problems and determine the appropriate fix.

## 4. Real-Time Container Metrics

Command executed:

`docker stats client-website`

- Memory usage: [Enter the actual value shown]
- CPU percentage: [Enter the actual percentage shown]
- Network I/O: [Enter the displayed value if required]

These measurements show the container's resource consumption at the time of observation.

## 5. Conclusion

Docker logs and resource metrics were used to examine the Nginx application's behavior and performance.
