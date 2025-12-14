import subprocess

def run(cmd):
    subprocess.run(cmd, shell=True)

repo_url = "https://github.com/your-username/your-repository.git"

run("git init")
run("git add .")
run('git commit -m "Uploaded using Python subprocess"')
run(f"git remote add origin {repo_url}")
run("git branch -M main")
run("git push -u origin main")

print("Files uploaded to GitHub successfully")
