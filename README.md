# Welcome to your Expo app 👋

This is an [Expo](https://expo.dev) project created with [`create-expo-app`](https://www.npmjs.com/package/create-expo-app).

## Get started

1. Install dependencies

   ```bash
   npm install
   ```

2. Start the app

   ```bash
    npx expo start
   ```

In the output, you'll find options to open the app in a

- [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go), a limited sandbox for trying out app development with Expo

You can start developing by editing the files inside the **app** directory. This project uses [file-based routing](https://docs.expo.dev/router/introduction).

## Get a fresh project

When you're ready, run:

```bash
npm run reset-project
```

This command will move the starter code to the **app-example** directory and create a blank **app** directory where you can start developing.

## Learn more

To learn more about developing your project with Expo, look at the following resources:

- [Expo documentation](https://docs.expo.dev/): Learn fundamentals, or go into advanced topics with our [guides](https://docs.expo.dev/guides).
- [Learn Expo tutorial](https://docs.expo.dev/tutorial/introduction/): Follow a step-by-step tutorial where you'll create a project that runs on Android, iOS, and the web.

## Join the community

Join our community of developers creating universal apps.

- [Expo on GitHub](https://github.com/expo/expo): View our open source platform and contribute.
- [Discord community](https://chat.expo.dev): Chat with Expo users and ask questions.
Topic-branch Creating Rules
Topic-branch luôn phải được tạo ra từ nhánh main
git checkout main - chuyển sang nhánh main
git pull - cập nhật các thay đổi mới nhất của main về local
git checkout -b <topic-branch-name> - tạo nhánh mới từ main
Trước khi push topic-branch lên repo, luôn phải chắc chắn
phiên bản hiện tại là phiên bản mới nhất trên main (up-todate)
git pull origin main - cập nhật các thay đổi mới
nhất của main về local
git push - đưa branch lên repository
Mục đích của việc này là xử lý kịp thời khi có conflict và tránh việc mất code của người khác do quá trình merge và ghi đè khi merge không chính xác
Naming Rules
1. Topic-branch naming rules:
<type>/#<issue_number>_<issue_title_in_english>
Trong đó:
type :
feature - tính năng mới
modify - chỉnh sửa tính năng/logic đã có sẵn
fix - sửa lỗi
hotfix - sửa các lỗi cần gấp trực tiếp trên production
revert - revert lại các commit trước
issue_number : number của task ở trên jira/trello, bắt đầu bằng dấu #
issue_title_in_english : title trên jira/trello (dịch sang tiếng anh)
Example: feature/#100_change_base_url_and_redirection
fix/#100_fix_overload_query
(*Ն Đối với sub-topic-branch ՅXử lý subtask cần tách nhánh con
ra từ topic-branch): <type>/#
<issue_number>_**subtask**_<**subtask_title**_in_english>
Example: feature/#100_subtask_add_redirection
feature/#100Շ1]subtask_add_redirection
feature/#100Շ2]subtaskadd_redirection
feature/#100Շ3]subtask_add_redirection
⇒ feature/#100_subtask_add_redirection ⇒ develop
2. Commit naming rules:
<typeՂҡ <changed content>
issue_title_in_english : title trên jira/trello (dịch sang
tiếng anh)
buildց Thay đổi liên quan đến hệ thống build hoặc công cụ.
ciց Cài đặt hoặc chỉnh sửa cấu hình CI và script liên quan.
docsց Cập nhật hoặc thêm document.
featց Thêm chức năng mới.
fixց Những commit fixbug.
perfց Tối ưu hiệu suất mà không thay feature hiện tại của app
refactorց Tái cấu trúc code, không sửa lỗi hoặc thêm chức
năng mới.
revert: revert một hoặc nhiều commit trước đó.
styleց Chỉnh sửa định dạng hoặc phong cách code, không
ảnh hưởng logic.
testց Thêm unit test
Example:"feat: driver apply to recruit" "perf: optimize get entries query"
