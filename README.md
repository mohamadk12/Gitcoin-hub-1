
import request 
t
# --------------------- 
# Replace with your wn information 
GITHUB_TOKEN = "your_personal_access_token 
REPO = "username/repo_name"  # Example: myuser/myrepo g
TITLE = "New automated issue"4
BODY = "This is a test issue created via the GitHub API."
# -------------------------
3
url = f"https://api.github.com/repos/{REPO}/issues"
headers = {"Authorization": f"token {GITHUB_TOKEN}"}
data = {"title": TITLE, "body": BODY}

response = requests.post(url, headers=headers, json=data)

if response.status_code == 201: 
    print("✅ Issue created:", response.json()["html_url"])
else:
    print("❌ Error:", response.status_code, response.text)
