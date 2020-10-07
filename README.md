# hello-world
Just another repository
Branch edited: readme-edits
URANUS

Finally remote push using ssh works. A working guide: https://kamarada.github.io/en/2019/07/14/using-git-with-ssh-keys/#.X33VaHkzbAQgit%20s

Steps followed for this repository:

  1: Created a clean ubuntu server URANUS with ssh access.
  2. Generated a new key pair> ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
  3. Started the ssh-agent> eval "$(ssh-agent -s)"
  4. Added the private key to ssh-agent> ssh-add ~/.ssh/id_rsa
  5. Pasted the content of ~/.ssh/id_rsa.pub into a new key at github.com, name=URANUS
  6. Tested remote access> ssh -T git@github.com
  7. Cloned this repository un URANUS, altered a file, committed but failed on push.
  8. Checked remote mechanism> git remote -v
      origin  https://github.com/kjelkols/hello-world.git (fetch)
      ...
  9. Successfully changed this to ssh> git remote set-url origin git@github.com/kjelkols/hello-world.git
      origin  git@github.com/kjelkols/hello-world.git (fetch)
      ...
git push now works on github

  
  
  

  
  
