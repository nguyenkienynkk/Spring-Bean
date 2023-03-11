Bean
Bean là những module chính của chương trình, được tạo ra và quản lý bởi Spring IoC container.


Inversion of Control (IoC) có thể hiểu một cách đơn giản IoC
là việc một object khởi tạo các phụ thuộc(dependencies) mà không
cần phải khởi tạo chúng. Các object này uỷ thác (delegates) các
việc xây dựng và khởi tạo các dependencies vào các Ioc Container.


IoC Container: là nơi các object được khởi tạo, config và nhúng nó
vào các dependencies và quản lý vòng đời của nó. Nó sử dụng
Dependency Injection(DI) để quản lý các components cấu thành nên
ứng dụng. Và lấy các thông tin dữ liệu từ các file config(XML)
hoặc các annotations.
Các module chứa trong IoC container được Spring gọi là các Bean.
IoC container của Spring gọi là Application context.


Các bean annotations:
@Component: annotation cấp class, mặc định biểu thị 1 giá trị bean với tên trùng với tên class bắt đầu bằng chữ cái in thường.
Nó có thể chỉ định tên khác bằng cách truyền tham số(param) vào annotations.
@Repository: annotation cấp class, đại diện cho lớp Data Access Object (DAO).
@Service: annotation cấp class, là nơi xử lý nghiệp vụ của hệ thống và có thể được sử dụng lại ở nhiều nơi.
@Controller: annotation cấp class, là nới đại diện cho lớp Controller trong mô hình MVC.
Configuration: annotation cấp class, là nơi có thể chứa các khai báo là bean thông qua Annotation @Bean.


DI
DI là một dạng thực hiện của IoC, bằng cách tiêm (inject) module vào một module khác cần nó
Nếu khi tạo module nào đó, mà module đó cần một module khác phụ thuộc,
thì IoC sẽ tìm trong IoC container xem có không, nếu có thì inject vào,
nếu chưa thì tạo mới, bỏ vào container và inject vào. Việc inject tự
động các dependency (module) như thế được gọi là Dependency injection.