Báo cáo Bài 3: Cấu hình xác thực SSH và Đẩy dự án lên GitHub

1. Thông tin Kho lưu trữ (GitHub Repository)
- URL Repository: https://github.com/username/ten-repository
- Giao thức cấu hình: SSH (`git@github.com:username/ten-repository.git`)

2. Các bước thực hiện cấu hình SSH
1. Khởi tạo SSH Key Ed25519:
```bash
ssh-keygen -t ed25519 -C "nhatndq.k06@gmail.com"
```
2. Thêm Public Key (`id_ed25519.pub`) vào GitHub:
```bash
cat ~/.ssh/id_ed25519.pub
```

3. Kiểm tra kết nối SSH:
```bash
ssh -T git@github.com
```

*Kết quả:* `Hi username! You've successfully authenticated, but GitHub does not provide shell access.`

4. Thêm Remote URL dạng SSH và Push code:
```bash
git remote add origin git@github.com:NDQNhat/Devops/ss4-ex3.git
git push -u origin master
```

3. Kết quả kiểm tra Remote URL (git remote -v)
```bash
origin  git@github.com:NDQNhat/Devops-NhatNDQ/ss4-ex3.git (fetch)
origin  git@github.com:NDQNhat/Devops-NhatNDQ/ss4-ex3.git (push)
```

