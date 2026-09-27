# Types of Cloud Storage

Cloud storage can be divided into three main types: Block Storage, File Storage, and Object Storage.

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| Block Storage | Stores data in fixed-size blocks that can be managed by an operating system like a traditional hard drive. | Virtual machines, databases, and applications that need fast disk access. | AWS EBS |
| File Storage | Stores files in folders and directories that can be shared across multiple systems. | Shared files, documents, and applications that need a common file system. | AWS EFS |
| Object Storage | Stores data as objects together with metadata and a unique identifier. | Images, videos, backups, documents, and other unstructured data. | AWS S3 |

## Why Object Storage is Best for the Client

Object Storage is suitable for the photo-sharing application because it is designed to store large amounts of unstructured data such as images. It can scale to handle millions of files while making the files accessible through web-based applications.
