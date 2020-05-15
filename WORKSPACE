workspace(name = "monorepo")

load("@//bazel/repository:dependencies.bzl", "workspace_dependencies")

workspace_dependencies()

load("@//bazel/repository:go.bzl", "setup_go")
load("@//bazel/repository:haskell.bzl", "setup_haskell")
load("@//bazel/repository:nixpkgs.bzl", "setup_nixpkgs")
load("@//bazel/repository:posix.bzl", "setup_posix")
load("@//bazel/repository:python.bzl", "setup_python")

setup_go()
setup_haskell()
setup_nixpkgs()
setup_posix()
setup_python()

load(
    "@io_bazel_rules_docker//repositories:repositories.bzl",
    rules_docker_repositories = "repositories"
)
rules_docker_repositories()

load("@//bazel/repository:docker.bzl", "setup_docker")
setup_docker()