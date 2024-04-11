- 👋 Hi, I’m @Devante7
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
-  I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Devante7/Devante7 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->#!/usr/bin/env bash

git_root() {
    git rev-parse --show-toplevel 2> /dev/null
}

git_head_version() {
    local recent_tag
    if recent_tag="$(git describe --exact-match HEAD 2> /dev/null)"; then
        echo "${recent_tag#v}"
    else
        git rev-parse --short=12 HEAD
    fi
}

