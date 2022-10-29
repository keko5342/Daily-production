# 20221015勉強内容
作ったもの、RailsチュートリアルのDockerコンテナイメージ作り
簡易版Dockerfileの記載

usage
```
$ docker build -t my-rails-image .

$ docker run -it --rm my-rails-image bash
root@0b4ef87ab25e:/# which rails
/usr/local/bundle/bin/rails
root@0b4ef87ab25e:/# exit

$ docker run -it -v $(pwd):/work -w /work -p 4649:3000 my-rails-image bash

$ cd my-blog
$ bundle install
$ rails server --binding=0.0.0.0
```

参考にしたページ
https://aws.amazon.com/jp/builders-flash/202009/container-rails-app/?awsf.filter-name=*all
