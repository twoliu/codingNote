# git学习
	命令 ：
		
		1. git add XXX 添加文件到暂存区
					
			1. git add . 添加所有文件到暂存区
				
		2. git commit -m 'XXX' 提交文件到本地仓库 [一次性的提交所有的暂存区文件到版本库]
				
		3. git status 查看当前仓库的状态[只有add 和 commit之后的文件被修改了,才能看到状态]
				
		4. git diff XXX 查看文件的差异[可以对比上次到底修改了什么文件,然后在提交]
				
		5. git log 查看提交的历史
				
		6. git reset --hard '版本id'  可以回退到指定的版本
				
		
		7. git reflog  查看命令的历史(所有操作的历史)
		
		8. git init 初始化版本库 (每当初始化版本库的时候,git会默认创建一个主分支master,我们默认是在master上面做各种操作)
		
		9. git checkout -- XXX 撤销文件的修改 [修改未添加到暂存区,则恢复到和版本库一致,添加到暂存区在修改,回复到和暂存区一致]

		10. git reset head XXX 将暂存区的修改回退到工作区

		11. git rm XXX 删除文件  

		12. 