Initially only created this to host an apt repo.
Maybe I'll use it for other things in future.

This repo is mostly other people's deb packages,
but other people host them in Github's releases,
which doesn't allow for interactions with apt directly.

DO NOT run the curl|sh thing the releases say to do.
That was added automatically by the tool I use, but curl|sh is always evil.

Repo is in the Releases, and created using https://github.com/X4BNet/github-apt-repos like::

    python3 -m githubaptrepos --gpg-user-id $DEBEMAIL --github-token "$(pass show 'Personal/Github API token'|head -1)" --deb-dir ~/vcs/mijofa.github.io/archive/pool --apt-dir ~/vcs/mijofa.github.io/archive --github-repo jellyfin/jellyfin-media-player --github-apt-repo mijofa/mijofa.github.io --github-delete-existing
