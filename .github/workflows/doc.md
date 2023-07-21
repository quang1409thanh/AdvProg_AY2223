# Một số chức năng dùng trên github.

`Các chức năng ngoài repo để lưu trữ code.`

## I. Chức năng pullrequest [more...](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)

1. Mục đích
    - Cho phép đề xuất của mình vào dự án của người khác (hoặc của chính mình)
2. Cách sử dụng

        `Thường được sử dụng như sau`
    - B1: Fork repository 
    - B2: Tạo branch mới (tránh ảnh hưởng đến dự án chỉnh)
    - B3: Thực hiện thay đổi
    - B4: Tạo pull request `chờ được aporve`
    - B5: Thảo luận
    - B6: Đồng ý và merge vào 
## II. Chưc năng github action [more...](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions)
1. Khái niệm
        
        `GitHub Actions là một dịch vụ tích hợp liên tục (Continuous Integration - CI) và liên tục triển khai (Continuous Deployment - CD) của GitHub. Nó cho phép bạn tự động hóa quy trình làm việc của dự án, chẳng hạn như chạy các bài kiểm tra tự động, triển khai ứng dụng và thực hiện các tác vụ khác mỗi khi có sự kiện xảy ra trong repository.`
2. Thực hiện
    - Workflows: (khi github actioc được bật, github action sẽ tự động triển khai theo file được viết trong file yaml trong thư mục `workflows/action.yml` )
    - Jobs
    - Steps
        
        nó sẽ thực hiện khi push hoặc pull request
## III. Ứng dụng để test tự động
1. Có 1 project muốn fork về, sửa code và push lên để check có đúng không
2. Ý tưởng: vì nếu pull request vào repo của người khác thì cần chờ aprove, còn nếu pull request vào repo của mình thì nó sẽ diễn ra tự động. => Tạo 1 repo giống hệt với cái của họ như sau.
3. sau đó 
    - sửa code bên nhánh phụ push lên
    - bật chức năng action tạo pull request từ nhánh phụ sang nhánh chính, như vậy test tự động sẽ được diễn ra.
một số lưu ý cần thiết reset lại branch master
        
        - Git checkout master: chuyển qua branch master
        - Git remote add upstream https://github.com/csuet/AdvProg_AY2223.git
        - Git fetch upstream
        - Git reset –hard upstream/master

