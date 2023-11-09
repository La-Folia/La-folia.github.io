---
layout: post
title: Git hub Guide for Equinoxer
image: '/images/50.jpg'
tags:   [work, technology]
date:   2023-9-14 15:01:35 +0300
description: Sin tantum modo ad indicia veteris memoriae cognoscenda, curiosorum. Haec et tu ita     pos    uisti, et verba vestra sunt. Idemne potest esse dies...

---

***

# Git blog file 을 다운받고, 게시글을 업로드 하는 방법 
이는 곧 github에 repository에다가 파일을 업로드하는 것과 동일하다.

***
# Git blog file을 local 저장소로 옮기자 (Git clone)
우선 그전, 최초로 mail을 통해서 권한을 받았다면, repository를git clone을
해주어야 하는데, 우선 본인이 blog 파일들을 내려받을 최초의 local 저장소를
만들어준다.

***

우선 우리는 blog의 파일을 모두 pull해야 한다. 최초로 pull할때는 먼저 저장소를 clone해야 한다. clone을 위한 주소는 다음을 통해서도 볼 수 있다.
<img src="/images/1003.png">

{% highlight js %}
mkdir "File name"
{% endhighlight %}
파일을 위치를 들어가고 나가는 명령어로는 cd, ls 등 다양하게 있으니 본인
운영체제에 맞게 구글링해서 공부해보도록 하자.

이후 파일에 들어가준다.
{% highlight js %}
cd "File name"
{% endhighlight %}

그리고 들어간 폴더 안에서 git clone을 해줄 것이다.
우선 Equinox의 경우, clone 주소는 다음과 같다.
{% highlight js %}
https://github.com/La-Folia/La-folia.github.io.git
{% endhighlight %}

오케이. 이제 git clone을 해주자.
{% highlight js %}
git clone <https://github.com/계정/리포지토리.git>
{% endhighlight %}

우리의 경우,
{% highlight js %}
git clone https://github.com/La-Folia/La-folia.github.io.git
{% endhighlight %}

이제 작업 환경을 구성해주어야 한다.
우선 해당 폴더 안으로 들어가준다.
{% highlight js %}
cd La-folia.github.io
{% endhighlight %}

이후, 다음과 같이 입력한다.
{% highlight js %}
git init projecttest
cd projecttest
git config user.name "사용자 이름"
git config user.email 메일 주소
{% endhighlight %}

***

# Git add, Commit, Push 를 통하여 게시글을 올리자.
이제 본격적으로 blog를 수정하려면 기본적으로 _post 파일에 들어가서 markdown 을
입력하고 관련된 사진을 images 파일에 저장하여 git add, commit, push를
해줌으로서 게시글이 등록된다. 즉,
{% highlight markdown %}
1. _post에 markdown 파일 생성 및 글 작성
2. 이때 관련된 파일은 images에 파일저장
3. 작업 중이던 모든 파일들을 올리려면
4. git add .
5. git commit -m "commit message"
6. git push
{% endhighlight %}
의 절차를 따른다.


이제 끝났다. 하지만 이외에 가장 중요한게 있는데, 협업을 하다보면 각기 다른
기능을 작업하는 경우가 대부분인데, 이때, 그 문서들이 섞이지 않도록
버전관리를 하면서 협업해야 한다. 그 이유는 각 팀원의 새로운 branch에서도
원격 저장소에 push를 할 수 있기 때문이다.

***

따라서, 원격 저장소에 다른 팀원들의 commit이 추가되어 있는지 확인하기 위해
git pull 명령어를 사용하여 최신 수정 내역을 당겨온다
{% highlight js %}
git pull
{% endhighlight %}

이후 우리가 원하는대로 작업한 것을 다시 add, commit, push를 하면 된다.
원격 저장소에 push를 할 수 있기 때문이다.

***

이와 관련하여 원리를 이해할 수 있는 몇가지 사진을 첨부하겠다. 이후 설명은
추가로 업로드 할 계획이다.
