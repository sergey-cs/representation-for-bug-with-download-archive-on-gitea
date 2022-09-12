# representation-for-bug-with-download-archive-on-gitea
This is a repository to reproduce a bug related to the appearance of unwanted git hooks when loading the repository as an archive via the Web UI and the resulting breakdown of Pull Requests on Gitea (1.17.1)

Steps for representation: 
1. Import/Clone this repository onto your gitea instance
![image](https://user-images.githubusercontent.com/10897900/189641786-0d5aae07-efd1-4a4b-8ecd-7a2ce92d1403.png)

2. Download the repository as an archive via the Web UI
![image](https://user-images.githubusercontent.com/10897900/189641956-65ab702e-3c60-4324-98e8-ac126aeb7f21.png)

3. Create a PR with any modified lfs file
![image](https://user-images.githubusercontent.com/10897900/189642250-3eeb14e7-f2cd-429d-9cf6-af004e5825e2.png)


4. After click on button "Create Pull Request" get error 500 and broken PR
![image](https://user-images.githubusercontent.com/10897900/189642485-d9a0aaa7-34fd-4544-aeb2-6ccd43e64b95.png)
![image](https://user-images.githubusercontent.com/10897900/189642665-b21d13e2-190e-4254-a2b1-b0adbcefd4c1.png)
