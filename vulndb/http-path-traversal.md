---
title: HTTP Path Traversal
---
##### Overview

A path traversal vulnerability (also known as directory traversal) allows to access files and directories that are stored outside the web root folder. By manipulating variables that reference files with "dot-dot-slash (../)" sequences and its variations or by using absolute file paths, it may be possible to access arbitrary files and directories stored on file system including application source code or configuration and critical system files. It should be noted that access to files is limited by system operational access control.

This attack is also known as "dot-dot-slash", "directory traversal", "directory climbing" and "backtracking".

#### References

* [Directory traversal attack](https://en.wikipedia.org/wiki/Directory_traversal_attack)
