# S3 Assets

![License](https://img.shields.io/badge/license-MIT-blue.svg) [![Latest Stable Version](https://img.shields.io/packagist/v/blomstra/s3-assets.svg)](https://packagist.org/packages/blomstra/s3-assets) [![Total Downloads](https://img.shields.io/packagist/dt/blomstra/s3-assets.svg)](https://packagist.org/packages/blomstra/s3-assets)

A [Flarum](http://flarum.org) extension. Relocate Flarum disks onto S3 or compatible bucket

## Installation

Install with composer:

```sh
composer require blomstra/s3-assets:"*"
```

## Updating

```sh
composer update blomstra/s3-assets
php flarum cache:clear
```

## Configuration

The S3 (or compatible) bucket can be configured either by environment variables or via the extension settings. If the environment variables are set, they will override the settings entered in the admin panel, if set.

#### Environment variables
- `AWS_ACCESS_KEY_ID` - your access key ID
- `AWS_SECRET_ACCESS_KEY` - your secret
- `AWS_DEFAULT_REGION` - the region
- `AWS_BUCKET` - the bucket name
- `AWS_URL` - the public facing base URL of the bucket
- `AWS_ENDPOINT` - the ARN
- `AWS_PATH_STYLE_ENDPOINT` - boolean value

#### Transferring assets from the existing filesystem to the S3 bucket

After your new bucket is configured, any exisiting files, will not exist there (ie uploaded avatars, profile covers, etc).

Use the provided command to start moving these files:

```php
php flarum s3:move
```

## Links

- [Packagist](https://packagist.org/packages/blomstra/s3-assets)
- [GitHub](https://github.com/blomstra/s3-assets)
- [Discuss](https://discuss.flarum.org/d/PUT_DISCUSS_SLUG_HERE)