I:Phần lý thuyết

**Pseudo-class và Pseudo-element:**

1. **Pseudo-class:** Pseudo-class là một loại lựa chọn trong CSS để áp dụng kiểu cho phần tử khi nó ở trong một trạng thái cụ thể, như `:hover`, `:active`, `:focus`.

2. **Pseudo-element:** Pseudo-element là một phần của một phần tử được chọn và áp dụng kiểu như một phần tử thứ hai, chẳng hạn như `::before`, `::after`.

**Các pseudo phổ biến:**

1. `:hover`: Áp dụng kiểu khi người dùng di chuột qua phần tử.

2. `:focus`: Áp dụng kiểu khi phần tử đang được focus, thường dùng cho các phần tử có thể nhập như input.

3. `:active`: Áp dụng kiểu khi phần tử đang được nhấn giữ.

4. `::before`: Tạo một pseudo-element trước nội dung thực tế của phần tử được chọn, cho phép bạn chèn nội dung hoặc kiểu vào phần tử.

**Về `position: absolute` và `left: 50%`:**

Khi bạn đặt `position: absolute` cho một phần tử, nó sẽ dựa vào phần tử cha gần nhất có thuộc tính `position` là khác `static` (mặc định) để xác định vị trí của nó. Thuộc tính `left: 50%` nghĩa là phần tử con sẽ được di chuyển 50% theo chiều ngang của phần tử cha gần nhất có thuộc tính `position` không phải `static`.

Tuy nhiên, `left: 50%` không một cách tự nhiên đặt phần tử ở giữa màn hình, mà nó sẽ đặt phần tử sao cho điểm góc trên bên trái của phần tử ở ngay tại giữa 50% chiều ngang của phần tử cha. Điều này có thể làm cho phần tử trở nên không đẹp mắt hoặc không nằm giữa trung tâm thị trường.

Để giữ cho phần tử đó nằm ở giữa màn hình, bạn cần sử dụng một phương pháp khác như cách kết hợp `position: absolute` với `transform: translateX(-50%)`. Điều này sẽ đẩy phần tử 50% về bên trái dựa trên chính điểm góc trên bên trái của phần tử, tạo ra hiệu ứng căn giữa ngay giữa màn hình.
II:Chuẩn bị bài mới
**Position: Sticky và Fixed:**

1. **Position: Sticky:** Khi sử dụng `position: sticky`, phần tử sẽ bắt đầu hoạt động như `position: relative` (tức là sẽ di chuyển theo luồng bình thường của tài liệu) cho đến khi nó bắt đầu "dính" vào một ngưỡng cuộn cụ thể (thường là vị trí của phần tử cha gần nhất có thuộc tính `overflow` khác `visible`). Khi phần tử dính, nó sẽ hoạt động như `position: fixed` đối với ngưỡng cuộn này và duy trì vị trí dính ngay trên màn hình.

2. **Position: Fixed:** Phần tử với `position: fixed` sẽ luôn hiển thị ở cùng một vị trí trên màn hình dựa vào các giá trị như `top`, `right`, `bottom`, `left`.

**Position: Sticky hoạt động như thế nào:**

Khi bạn đặt `position: sticky` cho một phần tử, nó sẽ bắt đầu như `position: relative`. Khi bạn cuộn màn hình và phần tử đạt đến vị trí "dính" được xác định trước (bởi `top`, `right`, `bottom`, `left` và phần tử cha có thuộc tính `overflow` không phải `visible`), phần tử sẽ bắt đầu hoạt động như `position: fixed`, bám vào vị trí này.

**Các loại transform trong CSS:**

1. **`transform: translate()`**: Di chuyển phần tử theo các giá trị x, y.

2. **`transform: scale()`**: Thay đổi kích thước phần tử theo các giá trị x, y.

3. **`transform: rotate()`**: Xoay phần tử với góc quay được chỉ định.

4. **`transform: skew()`**: Xoay phần tử một góc nghiêng được chỉ định.

5. **`transform: matrix()`**: Kết hợp di chuyển, xoay và tỷ lệ theo ma trận.

6. **`transform: skewX()` và `transform: skewY()`**: Xoay phần tử một góc nghiêng theo trục x hoặc y.

7. **`transform: perspective()`**: Định nghĩa góc nhìn 3D cho phần tử, thường kết hợp với 3D transform.

8. **`transform: rotateX()`, `transform: rotateY()`, `transform: rotateZ()`**: Xoay phần tử 3D quanh các trục x, y hoặc z.

9. **`transform: translate3d()`, `transform: scale3d()`, `transform: rotate3d()`**: Tương tự như các hàm tương ứng 2D, nhưng hoạt động trong không gian 3D.

10. **`transform: none`**: Loại bỏ hiệu ứng transform của phần tử.

Các biểu thức `transform` cho phép bạn tạo hiệu ứng thú vị như chuyển động, biến đổi kích thước và xoay các phần tử trên trang web của bạn.
