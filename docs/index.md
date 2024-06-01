---
layout: page
---

# Low quality identifier service API

The low-quality image identifier service provides a cloud-hosted photo gallery which allows you to identify low quality images to mark and sort them for cleanup. 

This guide shows you how to interact with the low quality identifier service using the REST API.

## Quickstart

The quickstart guide shows you how to immediatly begin using this service to tag photos for cleanup.

[Quickstart](api/quickstart)

## Tutorials

Learn how to do common tasks within the low-quality image identifier service.

Before you begin, you must follow the prerequisite tutorial below. You only have to do this one time per development system.

* [Getting started](tutorials/before-you-start-a-tutorial)

After your system is ready, these tutorials show you how to perform common tasks.

* [Add a new user](tutorials/add-a-new-photo-tutorial)
* [Add a new photo](tutorials/add-a-new-photo-tutorial)
* [View photo quality check results](tutorials/view-photo-quality-checks)

## API reference docs

Detailed descriptions of the low-quality image identifier service's resources.

The API reference documents refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When running a local test, the `{base_url}` is
generally `http://localhost:3000`.

* [Users resource](api/users)
* [Photos resource](api/photos)