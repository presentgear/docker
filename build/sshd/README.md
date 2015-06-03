This is a secure ssh server setup based on a blog post by @stribika:

    https://stribika.github.io/2015/01/04/secure-secure-shell.html

Includes git,vim,zsh,tmux because I like them.

Things to know:

Mount your entire $HOME directory to /home/ssher so you get all your keys and rc dotfiles.

Do not try to ssh as root, instead use: "ssh ssher@hostname" with a key.

You should probably build this yourself, if you cared enough to read that blog post.

Example:
    docker run --name="sshd" -v /etc/localtime:/etc/localtime:ro -v $HOME:/home/ssher -p 22022:22 -d presentgear/sshd:latest
