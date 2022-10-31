# representation-for-bug-with-download-archive-on-gitea

See more https://github.com/go-gitea/gitea/issues/21148, https://github.com/go-gitea/gitea/issues/19810

This is a repository to reproduce a bug related to the appearance of unwanted git hooks when loading the repository as an archive via the Web UI and the resulting breakdown of Pull Requests on Gitea (1.17.1)

Steps for representation: 
1. Import/Clone this repository onto your gitea instance

|⚠ |It is important to move the repository along with the LFS files|
|---|---|

![image](https://user-images.githubusercontent.com/10897900/198987306-edc86168-a0d1-499f-b4ce-bc32e4370485.png)

![image](https://user-images.githubusercontent.com/10897900/198986300-1a707e2f-1bd0-4c81-a2ca-beff86816b69.png)


2. Download the repository as an archive via the Web UI

![image](https://user-images.githubusercontent.com/10897900/198987225-1d65da13-6f45-4514-80fd-29bff1253689.png)


3. Create a PR with any modified lfs file

![image](https://user-images.githubusercontent.com/10897900/189642250-3eeb14e7-f2cd-429d-9cf6-af004e5825e2.png)

4. Close the PR and then create a new one just like it

![image](https://user-images.githubusercontent.com/10897900/198987723-8590c0f6-5113-40b8-9ab7-9b24b695db2a.png)

5. After click on button "Create Pull Request" get error 500 and broken PR

![image](https://user-images.githubusercontent.com/10897900/189642485-d9a0aaa7-34fd-4544-aeb2-6ccd43e64b95.png)

![image](https://user-images.githubusercontent.com/10897900/189642665-b21d13e2-190e-4254-a2b1-b0adbcefd4c1.png)
