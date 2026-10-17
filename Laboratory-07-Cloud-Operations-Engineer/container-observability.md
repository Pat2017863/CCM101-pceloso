# Container Observability Report

## 1. Application Deployment

- **Container name:** `client-website`
- **Image:** `nginx`
- **Host port:** `8080`
- **Container port:** `80`

The Nginx web server was deployed using Docker and configured to accept HTTP requests through port 8080 on the host. The container started successfully and was ready to handle web requests.

## 2. HTTP Traffic Testing

HTTP requests were sent to the Nginx web server using the `curl` command.

- **Successful request 1:** HTTP 200 OK — the Nginx welcome page loaded successfully.
- **Successful request 2:** HTTP 200 OK — the `/index.html` page was accessed successfully.
- **Successful request 3:** HTTP 200 OK — the Nginx welcome page loaded successfully.
- **Request to `/hidden-admin-page`:** HTTP 404 Not Found — the requested page does not exist.

The logs show four successful HTTP 200 responses in total because the root page was requested four times, including an additional test request. The missing-page request returned HTTP 404 as expected.

## 3. Application Logs

**Command executed:**

`docker logs client-website`

The command displayed the Nginx startup messages, successful HTTP requests, and the error generated when the missing page was requested.

### HTTP 404 Error Log

The following log entry shows the missing-page request and its HTTP 404 status:

```text
172.17.0.1 - - [17/Oct/2026:15:12:56 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
```

The corresponding Nginx error log is:

```text
2026/10/17 15:12:56 [error] 29#29: *5 open() "/usr/share/nginx/html/hidden-admin-page" failed (2: No such file or directory), client: 172.17.0.1, server: localhost, request: "GET /hidden-admin-page HTTP/1.1", host: "localhost:8080"
```

### Why Application Logs Are Important

Application logs help engineers identify which requests succeeded and which ones failed. They provide useful details about errors and user requests, allowing engineers to investigate problems and determine the appropriate solution.

## 4. Real-Time Container Metrics

**Command executed:**

`docker stats client-website`

- **Memory usage:** Approximately 3.5 MiB
- **CPU percentage:** Approximately 0.05%
- **Network I/O:** Approximately 3.2 kB received / 1.8 kB transmitted

These are illustrative estimates for a lightweight Nginx container, not measured values from my terminal. The Docker stats command displays the container's resource consumption in real time, including CPU usage, memory usage, and network activity. Actual values may vary depending on the number of requests and the container's activity.

## 5. Conclusion

Docker logs and resource metrics help cloud operations engineers examine application behavior and performance. The HTTP tests confirmed that Nginx returned HTTP 200 for successful requests and HTTP 404 for the missing page. The error log identified that the requested file could not be found in the Nginx web directory. Monitoring CPU, memory, and network usage also helps engineers identify potential resource problems and maintain reliable web services.

