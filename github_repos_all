#显示github上每个储存库
import requests

# 执行API调用并储存响应。
url = 'https://api.github.com/search/repositories?q=language:python&sort=stars'
headers = {'Accept': 'application/vnd.github.v3+json'}
r = requests.get(url, headers=headers)
print(f"状态代码: {r.status_code}")

# 将API响应赋给一个变量。
response_dict = r.json()
print(f"存储库总数: {response_dict['total_count']}")

# 探索有关仓库的信息。
repo_dicts = response_dict['items']
print(f"已返回存储库: {len(repo_dicts)}")

print("\n关于每一个存储库的选定信息: ")
for repo_dict in repo_dicts:
    print(f"\n名称：{repo_dict['name']}")
    print(f"所有者: {repo_dict['owner']['login']}")
    print(f"评级: {repo_dict['stargazers_count']}")
    print(f"储存库: {repo_dict['html_url']}")
#    print(f"创建时间: {repo_dict['created_at']}")
#    print(f"最后一次更新的时间： {repo_dict['updated_at']}")
    print(f"描述: {repo_dict['description']}")
