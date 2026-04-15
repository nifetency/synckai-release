# Synckai CLI (Release)

Synckai is a lightweight CLI tool used to sync local files to an Amazon S3 bucket.

This release artifact is used internally by the Synckai GitHub Action, but it can also be used independently as a command-line tool.

---

##  Features

* Sync local files to S3 bucket
* Fast and simple CLI usage
* Designed for CI/CD workflows

---

##  Usage

Run the `synckai` binary using the following command:

```bash
 syncToS3 -f <folder> -b <bucket-name> 
```

---

##  Arguments

| Argument | Description                                            |
| -------- | ------------------------------------------------------ |
| `-f`     | Folder to sync                                         |
| `-b`     | Target S3 bucket name                                  |


---

##  Example

```bash
syncToS3 sync -f build -b my-s3-bucket 
```

This command will:

* Sync files from the `build` folder
* Upload them to `my-s3-bucket`
* Not create the bucket if it doesn't exist

---

##  AWS Configuration

Make sure AWS credentials are configured before running the tool.

You can set them using environment variables:

```bash
export AWS_ACCESS_KEY_ID=<your-access-key>
export AWS_SECRET_ACCESS_KEY=<your-secret-key>
export AWS_DEFAULT_REGION=<your-region>
```

---

##  GitHub Action Integration

This CLI tool is used by the Synckai GitHub Action.

 https://github.com/nifetency/synckai-actions

---

##  Notes

* Ensure the specified folder exists before running the command
* Proper IAM permissions are required for S3 operations
* Recommended for automation and CI/CD pipelines

---

##  License

MIT License
