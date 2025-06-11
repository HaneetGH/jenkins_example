# Jenkins Pipeline Example

This project demonstrates how to:
- Accept a client ID as a parameter (e.g., `3mf.sb.amp.vg`)
- Convert it into a folder path (`3mf/sb/amp/vg`)
- Read the `config.xml` file inside that path
- Print its content to Jenkins console output

### 🔧 Structure

```
CLIENT_ID = 3mf.sb.amp.vg
Path resolved = config_samples/3mf/sb/amp/vg/config.xml
```

### ✅ How to Use
1. Create a Jenkins Pipeline job.
2. Point the pipeline script to this repository's `Jenkinsfile`.
3. Provide a valid `CLIENT_ID` when running the job.
