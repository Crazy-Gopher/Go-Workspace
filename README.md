# Setting up your workspace

suppose this repo is checked out into the github.com/Crazy-Gopher/Go-Workspace directory. We can work on both github.com/Crazy-Gopher/Go-Workspace and github.com/Crazy-Gopher/Go-Workspace/tools simultaneously by creating a go.work file using go work init, followed by go work use MODULE_DIRECTORIES... to add directories containing go.mod files to the workspace

https://github.com/golang/tools/blob/master/gopls/doc/workspace.md
```
mkdir workspace
cd workspace
go work init

go mod init workspace
go work use .
go run .

go mod init setup
go work use ./setup
go run ./setup

go mod init tools
go work use ./tools
go run ./tools

go mod init gopls
go work use ./tools/gopls
go run ./tools/gopls

go mod init godoc
go work use ./tools/godoc
go run ./tools/godoc
```