//1安装protoc (极度耗时):

sudo apt-get install autoconf automake libtool curl make g++ unzip

git clone https://github.com/google/protobuf.git

cd protobuf

git submodule update --init --recursive

./autogen.sh

./configure

make

make check

sudo make install

sudo ldconfig

//2安装protoc(极快) 可以直接下载编译好的二进制程序,放入 GOPATH/bin

//安装go插件
//获取proto包
go get  -v -u github.com/golang/protobuf/proto    

//获取编译工具
go get  -v -u github.com/golang/protobuf/protoc-gen-go

//正常情况下 此时在 GOPATH/bin/ 下有一个可运行程序protoc-gen-go 
//测试  执行 命令 protoc 
