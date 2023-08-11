# Ludium-study-inha-2023-Github-Tutorial

<br>

[1. 중심 레포지터리 포크하기](#1-중심-레포지터리-포크하기)

[2. 포크한 내 레포지터리 클론하기](#2-포크한-내-레포지터리-클론하기)

[3. 깃 사용자 정보 설정하기](#3-깃-사용자-정보-설정하기)

[4. 개인 브랜치 생성하기](#4-개인-브랜치-생성하기)

[5. 작업하기](#5-작업하기-📌)

[6. 커밋 & 푸시하기](#6-커밋--푸시하기-📌)

[7. 풀 리퀘스트 하기](#7-풀-리퀘스트-하기-📌)

<br>

# 1. 중심 레포지터리 포크하기
이 레포지터리가 우리가 다 같이 개발하는 중심 레포지터리라 가정합니다. 협업을 위해 이 레포지터리를 포크해보세요.

1. 포크 버튼 클릭

    ![깃허브_포크_1](./깃허브%20포크_1.png)

2. Create fork 클릭

    ![깃허브_포크_2](./깃허브%20포크_2.png)

3. 빨간색 원 => 포크된 내 레포지터리<br>
파란색 원 => 포크했던 중심 레포지터리<br>
노란색 원 => 포크된 내 레포지터리 주소 복사

    ![깃허브_포크_3](./깃허브%20포크_3.png)

<br>

# 2. 포크한 내 레포지터리 클론하기
이 레포지터리는 윈도우 환경에 클론해도 상관 없지만, wsl 리눅스 환경을 기준으로 설명합니다.

1. CMD 관리자 권한으로 실행
2. `wsl` : wsl 접속
3. `cd ~` : 홈 디렉터리로 이동
4. `git clone` `${포크한 내 레포지터리 주소}` : 원격 저장소를 로컬에 복제
5. `ls` : 현재 디렉토리의 목록 확인
6. `cd` `${포크한 내 레포지터리 이름}` : 내 레포지터리 폴더로 경로 이동
7. `code .` : VS Code로 해당 폴더 열기

    ![깃허브_클론_1](./깃허브%20클론_1.png)

<br>

# 3. 깃 사용자 정보 설정하기

`git config --global user.name` `${깃허브 닉네임}`

`git config --global user.email` `${깃허브 아이디}`

최초 한 번만 설정하면 됩니다. 만약 잘못 설정했을 경우 `git config --glboal --unset user.name` 명령어를 통해 삭제하고 다시 설정하면 됩니다.

![깃_사용자_정보_설정_1](./깃%20사용자%20정보%20설정_1.png)

<br>

# 4. 개인 브랜치 생성하기

1. 깃 그래프 설치하기

    ![깃_그래프_설치_1](./깃%20그래프%20설치_1.png)

2. 브랜치 생성하기

    `git branch` `${생성할 브랜치 이름}`

    빨간색 원 부분이 중요합니다. <b>메인 브랜치, 새로 생성한 개인 브랜치, 원격 저장소가 모두 동일하게 가장 최신 버전</b>임을 한 줄에 나란히 표시된 것으로 확인할 수 있습니다. 또한 현재 디렉토리는 메인 브랜치임을 테두리가 굵게 표시된 모양으로 확인할 수 있습니다. 

    ![깃_브랜치_생성_1](깃%20브랜치%20생성_1.png)

3. 생성한 개인 브랜치로 이동하기

    `git switch` `${이동할 브랜치 이름}`

    작업할 브랜치로 이동합니다.

<br>

# 5. 작업하기 (📌)
포크 및 클론에 성공했다면 여기에 이름을 추가해서 커밋해보세요.

    - 장지원
    - 

1. 생성한 개인 브랜치로 이동하기

    `git switch` `${이동할 브랜치 이름}`

    작업할 브랜치로 이동합니다.

2. 리드미에 내 이름 추가해보기

    ![깃_커밋_1](./깃%20커밋_1.png)

<br>

# 6. 커밋 & 푸시하기 (📌)
작업한 내용을 <b>내 레포지터리</b>에 커밋 푸시합니다. 메인 브랜치가 아닌 <b>개인 브랜치</b>에 커밋 푸시하는 것을 권장합니다.

1. 스테이징 : 로컬 (내 PC) 저장소에 저장할 파일을 선택합니다.

    `git add .` : 변경된 모든 파일을 스테이징 합니다.

2. 커밋하기 : 로컬 (내 PC) 저장소에 저장합니다.

    `git commit -m` `${커밋 메세지}` : 커밋 메세지는 변경한 작업 내용에 대해서 알 수 있도록 작성합니다.

    ![깃_커밋_2](./깃%20커밋_2.png)

3. 푸시하기 : 원격 (깃허브) 저장소에 반영합니다.

    `git push origin` `${푸시할 원격 저장소의 브랜치 이름}`

    최초 사용자 정보 설정 시에 발생하는 웹 페이지입니다. 깃허브 로그인하고 Authorize Visual-Studio-Code 버튼을 클릭하면 됩니다.

    ![깃_커밋_3](./깃%20커밋_3.png)

    푸시가 완료된 화면입니다. 현재 작업 중인 브랜치는 개인 브랜치이며, 개인 브랜치가 가장 최신 버전임을 확인할 수 있습니다. 메인 브랜치는 아직 기존 버전임을 확인할 수 있습니다.

    ![깃_커밋_4](./깃%20커밋_4.png)

<br>

# 7. 풀 리퀘스트 하기 (📌)
지금까지 작업한 내용은 내 레포지터리의 개인 브랜치에만 저장되어 있습니다. 이제부터는 내가 작업한 내용과 중심 레포지터리의 코드를 합치기 위한 풀 리퀘스트 과정을 진행해보겠습니다. 여기서 가장 중요한 것은 중심 레포지터리를 포크한 내 레포지터리로 <b>싱크 포크</b>하는 것입니다.

1. 싱크 포크하기 (📌)

    중심 레포지터리의 메인 브랜치 코드를 개인 레포지터리 원격 저장소의 메인 브랜치에 반영하는 과정입니다.
    
    - 포크한 내 레포지터리 깃허브 페이지에 접속합니다.
    
    - 기존에 열려있던 웹 페이지에서 진행할 경우 <b>페이지 새로고침</b> 먼저 해야 합니다.

    - Sync fork 클릭 시 싱크 포크할 내용이 있는 지 확인할 수 있습니다. 

    - 싱크 포크가 필요한 화면 (Update branch 버튼 클릭)

        ![깃_싱크_포크_1](./깃%20싱크%20포크_1.png)

    - 싱크 포크가 완료된 화면

        ![깃_싱크_포크_2](./깃%20싱크%20포크_2.png)


    - 싱크 포크가 완료되었다는 건 중심 레포지터리의 코드가 내 개인 레포지터리 원격 저장소에 반영되었다는 것입니다.

    - 여기서 만약 싱크 포크가 이미 완료되어 있을 경우, 내 개인 레포지터리의 메인 브랜치와 개인 브랜치 코드를 합치기 위해 바로 3번으로 넘어가세요.
    
2. 내 레포지터리 동기화 (업데이트) (📌)

    이제 VS Code로 돌아가서 내 개인 레포지터리의 원격 저장소와 로컬 저장소를 동기화시켜줍니다.

    `git pull` : 원격 저장소의 코드를 로컬 저장소에 내려 받기

    ![깃_싱크_포크_3](./깃%20싱크%20포크_3.png)

    `git switch main` : 로컬 저장소의 메인 브랜치로 이동

    `git pull origin main` : 현재 브랜치에 원격 저장소의 메인 브랜치 코드 반영하기

3. 다른 사람 코드와 내 코드 합치기 (📌)

    ![깃_싱크_포크_4](./깃%20싱크%20포크_4.png)

    `git switch main` : 로컬 저장소의 메인 브랜치로 이동

    `git merge` `${머지할 개인 브랜치 이름}` : 최신 버전의 다른 사람 코드가 들어있는 메인 브랜치와 내가 작업한 개인 브랜치의 코드 합치기

    아래 화면처럼 충돌(느낌표)이 발생할 경우 직접 코드를 확인하면서 해결해줘야 합니다. 또한 코드를 합치면서 잘 실행되는지 오류가 발생하진 않는지 확인하는 것이 좋습니다.
    
    만약 여기서 머지 전으로 돌아가고 싶다면 `git merge --abort` 명령어를 입력하면 됩니다.

    ![깃_싱크_포크_5](./깃%20싱크%20포크_5.png)

    코드를 수정하여 충돌을 해결하였고, 느낌표가 사라졌음을 확인할 수 있습니다. 이제야 비로소 커밋이 가능합니다. 이번엔 명령어 대신 Commit 버튼을 통해 커밋을 해보겠습니다.

    ![깃_싱크_포크_6](./깃%20싱크%20포크_6.png)

    푸시도 Sync Changes 버튼을 통해 진행해봅니다.

    ![깃_싱크_포크_7](./깃%20싱크%20포크_7.png)

    다른 사람의 코드와 내 코드를 합치는 데 성공하였습니다. 아래 화면은 완료된 화면으로, 내 개인 레포지터리 메인 브랜치가 가장 최신 버전임을 확인할 수 있습니다.

    ![깃_싱크_포크_8](./깃%20싱크%20포크_8.png)

4. 풀 리퀘스트 요청 하기 (📌)

    이제 내 개인 레포지터리의 메인 브랜치가 가장 최신의 코드입니다. 중심 레포지터리에 반영시키기 위해 내 개인 레포지터리 페이지로 접속합니다.

    혹시 그 사이에 싱크 포크가 또 필요하진 않은지 확인하는 것이 좋습니다. 만약 풀 리퀘스트 전에 싱크 포크가 제대로 이루어지지 않을 경우 골치가 아파질 수 있습니다.

    아래 화면은 싱크 포크가 완료된 화면입니다.

    ![깃_풀_리퀘스트_1](./깃%20풀%20리퀘스트_1.png)

    Contribute 버튼 클릭

    Open pull request 클릭

    ![깃_풀_리퀘스트_2](./깃%20풀%20리퀘스트_2.png)

    내가 작성한 커밋 내용을 참고하여 제목과 내용을 입력하고 Create pull request 버튼을 클릭합니다.

    ![깃_풀_리퀘스트_3](./깃%20풀%20리퀘스트_3.png)

    풀 리퀘스트 요청이 완료되었습니다. 만약 여기까지 해냈다면 정말 고생하셨어요. 이제 저한테 깃허브 이메일을 알려주시면 중심 레포지터리의 공동 작업자로 초대해드리겠습니다.

5. 공동 작업자 초대 수락하기

    이 과정은 처음 한 번만 하면 됩니다.
    
    깃허브에 로그인한 상태에서 우측 상단의 알림 아이콘을 클릭하면 초대된 내용을 확인할 수 있습니다.
    
    Accept invitation 버튼 클릭
    
    ![깃_공동_작업자_초대_수락_1](./깃%20공동%20작업자%20초대%20수락_1.png)

    이제부터는 중심 레포지터리의 공동 작업자로서, 풀 리퀘스트 요청과 동시에 머지까지 진행할 수 있습니다.

6. 최종 머지하기 (📌)
    
    풀 리퀘스트 요청 후에 머지는 일종의 승인 과정으로, 최종적으로 머지하게 되면 중심 레포지터리에 풀 리퀘스트한 코드가 반영됩니다.

    Merge pull request 버튼 클릭

    ![깃_풀_리퀘스트_4](./깃%20풀%20리퀘스트_4.png)

    Confirm merge 버튼 클릭

    ![깃_풀_리퀘스트_5](./깃%20풀%20리퀘스트_5.png)

7. 내 레포지터리 동기화 (업데이트) (📌)

    이제 최종적으로 확정된 중심 레포지터리의 코드를 내 레포지터리에 모두 반영해줘야 합니다.

    내 레포지터리 페이지로 이동해서 다시 한 번 싱크 포크를 진행해줍니다.

    ![깃_풀_리퀘스트_6](./깃%20풀%20리퀘스트_6.png)

    `git pull` : 싱크 포크한 코드를 로컬 저장소에 반영합니다.

    ![깃_풀_리퀘스트_7](./깃%20풀%20리퀘스트_7.png)

    `git switch` `${개인 브랜치 이름}`

    `git pull origin main`

    `git push origin` `${개인 브랜치 이름}`

    개인 브랜치로 이동해서 메인 브랜치의 코드를 내려 받기 하고 원격 저장소에까지 반영해주면 아래 화면처럼 모든 브랜치가 최신 버전으로 업데이트 되었음을 확인할 수 있습니다.

    ![깃_풀_리퀘스트_8](./깃%20풀%20리퀘스트_8.png)

    이제 다시 작업할 때는 개인 브랜치로 이동해서 개발하면 됩니다.