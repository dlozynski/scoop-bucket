# Scoop Bucket

# optional proxy

* scoop config proxy webproxy.mycompany.com:8080
* $env:no_proxy = "mycompany.com"

# run server

```
synergys --debug INFO --name server --address :8080 -c configuration-demo.cfg --no-daemon
```
# run client

```
synergyc.exe --name client --no-daemon --enable-drag-drop --restart <host>:8080
```
* host - server ip


## Usage of Scoop template?

1. Generate your own copy of this repository with the "Use this template"
   button.
2. Allow all GitHub Actions:
   - Navigate to `Settings` - `Actions` - `General` - `Actions permissions`.
   - Select `Allow all actions and reusable workflows`.
   - Then `Save`.
3. Allow writing to the repository from within GitHub Actions:
   - Navigate to `Settings` - `Actions` - `General` - `Workflow permissions`.
   - Select `Read and write permissions`.
   - Then `Save`.
4. Document the bucket in `README.md`.
5. Replace the placeholder repository string in `bin/auto-pr.ps1`.
6. Create new manifests by copying `bucket/app-name.json.template` to
   `bucket/<app-name>.json`.
7. Commit and push changes.

## How do I install these manifests?

After manifests have been committed and pushed, run the following:

```pwsh
scoop bucket add <bucketname> https://github.com/<username>/<bucketname>
scoop install <bucketname>/<manifestname>
```
