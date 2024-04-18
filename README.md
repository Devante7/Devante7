   Resource Server (RS)  server that provides operations on protected
      resources, where operations require a valid access token issued by
      an AS.

   Resource Owner (RO)  subject entity that may grant or deny operations
      on resources it has authority upon.

      Note: the act of granting or denying an operation may be manual
      (i.e. through an interaction with a physical person) or automatic
      (i.e. through predefined organizational rules).
every sync 
<!---every project 
Devante7/Devante7 is a ✨ special ✨ repository because its `README.md` (dev) appears on your GitHub profile.
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
}:test run for unknown sources

