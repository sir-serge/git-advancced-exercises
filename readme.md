
###git rebase and git amend
```bash
gymiriba@Iribas-iMac git-advancced-exercises % git rebase --abort      
gymiriba@Iribas-iMac git-advancced-exercises % git rebase -i HEAD~3    
Successfully rebased and updated refs/heads/main.
gymiriba@Iribas-iMac git-advancced-exercises % git rebase -i HEAD~4
fatal: invalid upstream 'HEAD~4'
gymiriba@Iribas-iMac git-advancced-exercises % git rebase -i HEAD~3
Successfully rebased and updated refs/heads/main.
gymiriba@Iribas-iMac git-advancced-exercises % git log             
commit a9ac390f54d9cd54ce694658914ef3fd14fff4b2 (HEAD -> main)
Author: Gym Iriba <gymiriba@Iribas-iMac.local>
Date:   Mon Mar 10 13:07:39 2025 +0200

    chore: create fourth file

commit 41d62679ce0ab5d700932a7a0a1d6620e49b8909
Author: Gym Iriba <gymiriba@Iribas-iMac.local>
Date:   Mon Mar 10 13:00:03 2025 +0200

    create third file

commit 331ad51e23765b660aea0d7c0a1da6cd55295515
Author: Gym Iriba <gymiriba@Iribas-iMac.local>
Date:   Mon Mar 10 12:59:10 2025 +0200

    creating another file

commit 955b97149e32c304ba5daffd97c98d48b1f38370
Author: Gym Iriba <gymiriba@Iribas-iMac.local>
Date:   Mon Mar 10 12:58:46 2025 +0200

    creating intial file
gymiriba@Iribas-iMac git-advancced-exercises % git rebase -i HEAD~4
fatal: invalid upstream 'HEAD~4'
gymiriba@Iribas-iMac git-advancced-exercises % git status 
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

nothing to commit, working tree clean
gymiriba@Iribas-iMac git-advancced-exercises % git push origin 
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (9/9), 817 bytes | 817.00 KiB/s, done.
Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/sir-serge/git-advancced-exercises.git
 * [new branch]      main -> main
gymiriba@Iribas-iMac git-advancced-exercises % 
```


### squashing 

```bash
gymiriba@Iribas-iMac git-advancced-exercises % git rebase -i --root
[detached HEAD db40425] creating intial file
 Date: Mon Mar 10 12:58:46 2025 +0200
 Committer: Gym Iriba <gymiriba@Iribas-iMac.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.
gymiriba@Iribas-iMac git-advancced-exercises % 
```