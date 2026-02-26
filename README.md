
import reques

# --------------------- 
# Replace with your wn informationu 
GITHUB_TOKEN = "your_personal_access_token u
REPO = "username/repo_name"  # Example: myuser/myrepo 
TITLE = "New automated issue"
BODY = "This is a test issue created via the GitHub API."
# -------------------------

url = f"https://api.github.com/repos/{REPO}/issues"
headers = {"Authorization": f"token {GITHUB_TOKEN}"}h
data = {"title": TITLE, "body": BODY}h

response = requests.post(url, headers=headers, json=data)

if response.status_code == 201: 
    print("✅ Issue created:", response.json()["html_url"])
else:
    print("❌ Error:", response.status_code, response.text)
u
