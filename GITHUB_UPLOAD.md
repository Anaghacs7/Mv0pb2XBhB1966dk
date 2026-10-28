# Publish this project to GitHub (Windows PowerShell)

1. Extract the ZIP and open the `Mv0pb2XBhB1966dk` folder in File Explorer.
2. Click the address bar, type `powershell`, and press Enter.
3. Create an **empty** GitHub repository named exactly `Mv0pb2XBhB1966dk` (do not initialize with README).
4. Run the following commands one at a time:

```powershell
git init
git add .
git commit -m "Initial candidate ranking project"
git branch -M main
git remote add origin https://github.com/Anaghacs7/Mv0pb2XBhB1966dk.git
git push -u origin main
```

If `remote origin already exists`, check `git remote -v`, then run:

```powershell
git remote set-url origin https://github.com/Anaghacs7/Mv0pb2XBhB1966dk.git
git push -u origin main
```

5. Verify the README and notebook appear at `https://github.com/Anaghacs7/Mv0pb2XBhB1966dk`.
6. Only publish the CSV if its license and candidate privacy requirements permit public redistribution.
