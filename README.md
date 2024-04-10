{ # https://tea.xyz/what-is-this-file
---
version: 1.0.0
codeOwners:
  - '0x9b2733Ae4A405e7EcdBD2Bcb2646623498a20191'
quorum: 1 ,
  "branches": ["master"],
  "plugins": [
    "@semantic-release/commit-analyzer",
    "@semantic-release/release-notes-generator",
    "@semantic-release/changelog",
    "@semantic-release/npm",
    [
      "@semantic-release/git",
      {
        "message": "${nextRelease.version} CHANGELOG [skip ci]\n\n${nextRelease.notes}"
      }
    ],
    "@semantic-release/github"
  ]
}
