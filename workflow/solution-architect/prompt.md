Tôi muốn khi gọi AI ra nó hiện lên pop-up hỏi tôi lần lượt

Câu 1: Dự án làm cho BE hay FE? 2 option BE và FE.
Câu 2: Làm cho ngôn ngữ lập trình nào? 2 option Python và JavaScript.
Câu 3: Dùng framework nào?
- Nếu là JavaScript thì có 3 option là NestJS, React Native, Typescript (Cho chọn nhiều).
- Nếu là Python thì có 2 option là Flask (Cho chọn 1).
- Còn lại hiển thị Others.
Câu 4 (Nếu user chọn BE): Dự án có sử dụng database không? Cho 3 option là SQL, NoSQL, Không sử dụng database.
Câu cuối: AI hỏi thêm có muốn load thêm skill nào không? Nếu có thì cho user nhập tên những skill muốn load thêm, cách nhau bằng dấu phẩy. Nếu không thì chọn No.

Các skill sử dụng:
- BE: backend-dev-guidelines
- FE: web-design-guidelines, ui-ux-pro-max
- NodeJS: nodejs-best-practices, nodejs-backend-patterns
  - NestJS: nestjs-expert
  - React Native: react-native-architecture, react-state-management, react-best-practices
  - Typescript: typescript-expert, typescript-pro, typescript-advanced-types
- Python: python-patterns, python-pro
  - Flask: python-fastapi-development
- Database: database, database-design
  - SQL: Không cần skill nào thêm
  - NoSQL: nosql-expert

Tôi muốn khi gọi AI ra nó hiện lên pop-up hỏi tôi lần lượt các câu hỏi và load các skill như tôi đã nêu ra. Ngoài ra tôi cần thêm 1 action là load-skills để chủ động load lại skills khi cần thiết. Ví dụ như khi hết token cần compact thì tôi sẽ load lại skills để tiếp tục sử dụng AI mà không bị gián đoạn. Lứu ý là cần load cả skill mà user thêm ở field "có muốn load thêm skill nào không?" nữa nhé.

Ở bước load-skills AI sẽ hỏi tôi cần load thêm skill nào nữa không? Nếu có thì tôi sẽ nhập tên những skill muốn load thêm, cách nhau bằng dấu phẩy. Nếu không thì tôi sẽ chọn No. Sau đó AI sẽ load lại tất cả skills tương ứng với cấu hình đã chọn ở bước AUTO-INIT, bao gồm cả những skill tùy chọn mà tôi đã nhập thêm.