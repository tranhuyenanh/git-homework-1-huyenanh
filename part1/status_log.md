On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        draft.md
        notes.txt
        todo.txt

nothing added to commit but untracked files present (use "git add" to track)
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   notes.txt
	new file:   todo.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	draft.md
	status_log.md

diff --git a/part1/notes.txt b/part1/notes.txt
index e69de29..02cf657 100644
--- a/part1/notes.txt
+++ b/part1/notes.txt
@@ -0,0 +1,3 @@
+Dong 1: Ghi chu
+Dong 2: Cong viec
+Dong 3: Hoan thanh
diff --git a/part1/notes.txt b/part1/notes.txt
index e69de29..02cf657 100644
--- a/part1/notes.txt
+++ b/part1/notes.txt
@@ -0,0 +1,3 @@
+Dong 1: Ghi chu
+Dong 2: Cong viec
+Dong 3: Hoan thanh

--- Giai thich Muc 6 ---
Lenh git commit -a chi tu dong stage va commit doi voi cac file da duoc theo doi (already-tracked files). Cac file moi tao chua tung duoc add (untracked files) nhu draft.md hay status_log.md se bi bo qua va khong duoc commit tu dong.

--- Part C: Phân biệt git fetch và git pull ---
- git fetch: Chỉ tải các commit và thông tin mới từ remote repository về máy local (cập nhật các nhánh remote-tracking) nhưng KHÔNG tự động gộp (merge) vào thư mục làm việc (working directory) của bạn.
- git pull: Là kết hợp của 'git fetch' và 'git merge'. Nó vừa tải dữ liệu mới về, vừa tự động gộp ngay các thay đổi đó vào nhánh local hiện tại.
