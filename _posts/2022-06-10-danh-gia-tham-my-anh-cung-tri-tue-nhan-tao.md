---
layout: post
title: Đánh giá thẩm mỹ ảnh cùng trí tuệ nhân tạo
subtitle: Tìm hiểu và bàn luận về bài toán đánh giá thẩm mỹ ảnh cùng những giải pháp giải quyết bài toán này trên góc độ kỹ thuật với công cụ là trí tuệ nhân tạo.
background: /img/academic/iaa/background.jpg
tags: Academic
comments: true
permalink: /danh-gia-tham-my-anh-cung-tri-tue-nhan-tao.html
---

> TL;DR: Tìm hiểu và bàn luận về bài toán đánh giá thẩm mỹ ảnh cùng những giải pháp giải quyết bài toán này trên góc độ kỹ thuật với công cụ là trí tuệ nhân tạo.
> Liên kết đến bản tiếng Anh của bài viết có thể được tìm thấy tại [đây](https://hieuphung97.com/image-aesthetics-assessment-with-ai.html).

---

#### Mục lục
- [Giới thiệu bài toán](#intro)
- [Tại sao việc đánh giá thẩm mỹ ảnh lại quan trọng?](#why-iaa)
- [Làm sao để đánh giá thẩm mỹ cho ảnh?](#how-iaa)
- [**Đánh giá thẩm mỹ ảnh cùng trí tuệ nhân tạo**](#iaa-with-ai) 👈
- [Bàn luận](#discussion)
- [Tài liệu tham khảo](#references)

<br/>

---

#### Kiến thức nền nên có
<ul>
  <li><a href="https://en.wikipedia.org/wiki/Machine_learning" target="_blank">Máy học (Machine Learning), hay học máy</a>
    <ul>
      <li><a href="https://en.wikipedia.org/wiki/Statistical_classification" target="_blank">Bài toán phân lớp (Classification Problem)</a></li>
      <li><a href="https://en.wikipedia.org/wiki/Regression_analysis" target="_blank">Bài toán hồi quy (Regression Problem)</a></li>
      <li><a href="https://en.wikipedia.org/wiki/Ranking" target="_blank">Bài toán xếp hạng (Ranking Problem)</a></li>
      <li><a href="https://en.wikipedia.org/wiki/Deep_learning" target="_blank">Học sâu (Deep Learning)</a></li>
    </ul>
  </li>
</ul>

<hr style="border:1px solid gray">

<br/>

# <a id="intro"></a>Giới thiệu bài toán

Thẩm mỹ [[1](#ref-1),[2](#ref-2),[3](#ref-3)] (danh từ) có nghĩa là cái đẹp hay khả năng cảm thụ cái đẹp.

Đánh giá thẩm mỹ ảnh (Image Aesthetics Assessment) [[4](#ref-4),[5](#ref-5)], khi được xét trên khía cạnh tính toán bởi máy móc, là một bài toán về thị giác máy tính nhằm phân loại các tấm ảnh vào các nhóm có mức độ thẩm mỹ khác nhau; hay nói cách khác, là đưa ra được những quyết định về mặt thẩm mỹ tương tự với cách làm của con người.

#### Các thuật ngữ có liên quan
- Đánh giá chất lượng ảnh (Image Quality Assessment)
- Khả năng ghi nhớ của ảnh (Image Memorability)
- Cắt ảnh (Image Cropping)

<br/>

---

# <a id="why-iaa"></a>Tại sao việc đánh giá thẩm mỹ ảnh lại quan trọng?
Các bạn thử tự hỏi bản thân xem đã bao giờ đánh giá thẩm mỹ của một bức ảnh hay chưa? Mình cá là hầu hết những ai đang đọc bài blog này đều đã làm công việc này rồi, thậm chí là hàng ngày. Không cần phải là một thứ gì đấy cao siêu, hành động đánh giá thẩm mỹ ảnh xuất hiện ngay trong quá trình các bạn chụp một tấm ảnh. Các bạn có thể sẽ căn góc độ chụp, điều chỉnh ánh sáng, thay đổi khẩu độ ống kính, hay nhắc nhở người mẫu thay đổi tư thế,v.v., tất cả là để thu được tấm hình đẹp nhất theo ý của bạn.

Ngoài đem lại giá trị về mặt tinh thần, một tấm ảnh đẹp còn có thể đem lại những giá trị rất lớn về vật chất. Không phải tự nhiên ta có những chuyên gia đánh giá chất lượng của ảnh. Không phải tự nhiên các mạng xã hội dựa trên việc chia sẻ những tấm ảnh như <a href="https://www.instagram.com/" target="_blank">Instagram</a> và <a href="https://www.pinterest.com/" target="_blank">Pinterest</a> lại mọc lên. Không phải tự nhiên lại xuất hiện ngành công nghiệp bán <a href="https://en.wikipedia.org/wiki/Stock_photography" target="_blank">ảnh stock</a>; chúng ta có <a href="https://www.pixtastock.com/" target="_blank">Pixtastock</a> ở thị trường Nhật Bản, hay ở quy mô lớn hơn, ta có ông lớn <a href="https://www.shutterstock.com/" target="_blank">Shutterstock</a>, và còn rất nhiều những cái tên khác.

Một lý do nữa mà theo mình khiến cho bài toán này quan trọng đó là nhu cầu tìm kiếm những tấm ảnh đẹp sẽ ngày một tăng. Khi mà số lượng ảnh được chia sẻ trên Internet ngày một lớn, giữa một rừng ảnh xấu có đẹp có với đủ các thể loại nội dung, việc tìm ra một tấm ảnh ưng mắt có thể sẽ càng trở nên khó khăn hơn. Có lẽ, đến một ngày nào đó, việc tìm kiếm và sắp xếp những tấm ảnh theo một thang đo thẩm mỹ nào đấy sẽ trở thành tính năng tiêu chuẩn của tất cả các công cụ tìm kiếm.

<br/>

---

# <a id="how-iaa"></a>Làm sao để đánh giá thẩm mỹ cho ảnh?

Giờ ta sẽ cùng xem con người và máy móc làm công việc đánh giá thẩm mỹ ảnh kiểu gì.

## Cách con người đánh giá
Là một cá nhân, ắt hẳn mỗi người sẽ có những cách đánh giá của riêng mình; nhưng nhìn chung, để việc đánh giá diễn ra một cách có hệ thống, ta sẽ cần phải định nghĩa ra những tiêu chí thẩm mỹ.

Những tiêu chí có thể kể đến như:
- Bố cục của ảnh
- Ánh sáng
- Nhấn mạnh chủ thể chính
- Sự ưng mắt của người mẫu
- Sự hấp dẫn của hoa văn họa tiết
- Tính độc đáo về nội dung
- ...

Xét về tiêu chí bố cục, có rất nhiều cách để sắp xếp bố cục cho một tấm ảnh, phổ biến nhất có lẽ là <a href="https://en.wikipedia.org/wiki/Rule_of_thirds" target="_blank">quy tắc 1 phần 3 (Rule of Thirds)</a>, kế đến có thể là <a href="https://en.wikipedia.org/wiki/Symmetry" target="_blank">đối xứng (Symmetry)</a>,..., và còn rất nhiều những cách sắp xếp khác cho bố cục của ảnh.
<center><img src="/img/academic/iaa/rule_of_thirds.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

Việc thỏa mãn một tiêu chí bố cục nào đấy có thể giúp cho tấm ảnh trở nên đẹp hơn. Một video ngắn (<a href="https://www.instagram.com/reel/CaPxY2pqOH0/" target="_blank">instagram.com/reel/CaPxY2pqOH0/</a>) giới thiệu về một vài loại bố cục thường được dùng trong hội họa và nhiếp ảnh được chia sẻ bởi <a href="https://www.instagram.com/mitchleeuwe/" target="_blank">mitchleeuwe</a> có thể giúp các bạn hiểu rõ hơn về tiêu chí thẩm mỹ này.

<br/>

Về yếu tố ánh sáng, một tấm ảnh có ánh sáng đẹp có thể được định nghĩa là một tấm ảnh có ánh sáng vừa đủ, không bị thiếu sáng hay cháy sáng dẫn đến làm mất các chi tiết trên ảnh.
<table>
  <tr>
    <td><center><img src="/img/academic/iaa/lighting.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
    <td><center><img src="/img/academic/iaa/lighting_2.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
    <td><center><img src="/img/academic/iaa/lighting_3.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
  </tr>
</table>

<br/>

Việc <a href="https://thevirtualinstructor.com/blog/emphasis-a-principle-of-art" target="_blank">nhấn mạnh</a> được chủ thể chính cũng có thể giúp cho một tấm ảnh trở nên đẹp hơn. Bằng việc vận dụng những yếu tố như sự tương phản về màu sắc, hiệu ứng gần xa, sự cô lập,v.v., các nghệ sĩ có thể hướng được sự tập trung của người xem đến một vài khu vực nhất định trên ảnh một cách có chủ ý, nhằm phục vụ ý đồ nghệ thuật của mình.
<center><img src="/img/academic/iaa/object_emphasis.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

<br/>

Những đánh giá về sự ưng mắt của người mẫu hay sự hấp dẫn của hoa văn họa tiết lại có phần chủ quan hơn, đến từ quan điểm cá nhân của người đánh giá.

<table>
  <tr>
    <td><center><img src="/img/academic/iaa/sailor_moon.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
    <td><center><img src="/img/academic/iaa/sailor_moon_2.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
  </tr>
</table>

Tùy vào sự khác biệt về kinh nghiệm, giới tính, quốc gia, tôn giáo,v.v., mà những đánh giá của mỗi người lại có thể khác nhau.

<table>
  <tr>
    <td><center><img src="/img/academic/iaa/xo_pattern.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
    <td><center><img src="/img/academic/iaa/memphis_style_pattern.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
  </tr>
</table>

<br/>

Tính độc đáo về mặt nội dung thậm chí còn cần con mắt nghệ nghĩ của những người đánh giá, để chọn ra được bức ảnh có nội dung độc và lạ nhất trong những bức ảnh đang có.
<center><img src="/img/academic/iaa/content_uniqueness.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

Và còn rất nhiều những tiêu chí khác mà ta có thể định nghĩa để đánh giá độ thẩm mỹ cho những bức ảnh. Có thể thấy đây là một công việc không hề đơn giản với con người, có rất rất nhiều yếu tố có thể được đặt lên bàn cân cho việc đánh giá thẩm mỹ. Vậy, liệu rằng máy móc có thể làm thay con người công việc này?

## Cách máy móc đánh giá
Trước trả lời câu hỏi liệu máy móc có thể đánh giá được thẩm mỹ của một bức ảnh, ta sẽ phân loại các tiêu chí đánh giá thẩm mỹ ảnh vừa được liệt kê ở trên vào hai nhóm:

- Các tiêu chí đánh giá về kỹ thuật
  - Bố cục của ảnh
  - Ánh sáng
  - Nhấn mạnh chủ thể chính
- Các tiêu chí đánh giá về nội dung
  - Sự ưng mắt của người mẫu
  - Sự hấp dẫn của hoa văn họa tiết
  - Tính độc đáo về nội dung

Hai chữ "kỹ thuật" cũng đã phần nào nói lên sự máy móc của những tiêu chí thuộc nhóm đầu tiên. Khi con người có thể đánh giá một tiêu chí về mặt định lượng, các quyết định được đưa ra sẽ càng trở nên khách quan hơn, và sẽ càng dễ dàng hơn để lập trình cho máy biết được như thế nào là thỏa mãn một tiêu chí nào đó, hay đạt được tiêu chí đó ở mức độ như thế nào.

Ngược lại, các tiêu chí đánh giá về nội dung lại chứa nhiều ý kiến chủ quan trong đó. Việc tìm ra được quy luật vì thế mà cũng trở nên khó khăn hơn, khó cho việc đánh giá một cách máy móc.

Để đánh giá được thẩm mỹ của ảnh một cách trọng vẹn, ta sẽ cần phải quan tâm cả về những yếu tố khách quan và những yếu tố mang tính chủ quan. Điều này đặt ra các thách thức cho con người trong việc truyền đạt những tri thức này cho máy nhằm mô phỏng lại quá trình đánh giá thẩm mỹ ảnh. Ta sẽ cùng đến với những phần tiếp theo để xem các công trình nghiên cứu hiện nay đang giải quyết vấn đề này như thế nào.

<br/>

---

# <a id="iaa-with-ai"></a>Đánh giá thẩm mỹ ảnh cùng trí tuệ nhân tạo

<center><img src="/img/academic/iaa/iaa_dimensions.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>
<center><i>Các khía cạnh của bài toán đánh giá thẩm mỹ ảnh [<a href="#ref-4">4</a>]</i></center>

Hình vẽ phía trên cho ta một bức tranh toàn cảnh về bài toán đánh giá thẩm mỹ ảnh. Những khía cạnh tạo nên bức tranh này gồm
- đầu vào (Input) của bài toán,
- phạm vi (Scope) của bài toán,
- đặc trưng (Features) được sử dụng,
- đầu ra (Output) của bài toán,
- và ứng dụng (Application).

Trong bài blog này, ta sẽ chỉ tập trung vào ba khía cạnh: Đặc trưng được sử dụng, đầu ra của bài toán, và phạm vi của bài toán.

## Đặc trưng được sử dụng
Đầu tiên, nói về các đặc trưng được sử dụng cho việc giải quyết bài toán, nếu ta coi giải pháp mà ta sử dụng để giải quyết bài toán đánh giá thẩm mỹ ảnh là một cỗ máy thì các đặc trưng ta cung cấp sẽ là nguyên liệu để cỗ máy đó hoạt động. Trong các công trình nghiên cứu từ trước cho đến nay về bài toán đánh giá thẩm mỹ ảnh, các nguyên liệu này có thể là...

### Các đặc trưng được trích xuất bằng tay (Hand-Crafted Features) bởi các chuyên gia
Với vốn hiểu biết phong phú của mình về nhiếp ảnh, vật lý, toán học, và có thể là về nhiều lĩnh vực khác, các chuyên gia sẽ đề xuất những đặc trưng mà họ cho rằng có thể đại diện cho những tấm ảnh. Lấy ví dụ như <a href="https://en.wikipedia.org/wiki/Color_histogram" target="_blank">Color Histogram<a>, bằng việc phân tích các thông tin này, có lẽ ta sẽ tìm được ra những quy luật để phân biệt một tấm ảnh có màu sắc hài hòa với những tấm ảnh khác.

<center><img src="/img/academic/iaa/hand_crafted_features.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

Các công trình sử dụng những đặc trưng được trích xuất bằng tay thường có tuổi đời khá cao, chứa hàm lượng toán lớn và kết quả thu được bởi các giải pháp được đề xuất bởi những công trình này chưa thực sự tốt. Tuy nhiên, ta có thể dễ dàng nhìn ra các yếu tố dẫn đến những quyết định liên quan đến thẩm mỹ của ảnh khi sử dụng các đặc trưng này.

### Các đặc trưng tổng quát (Generic Features)
Đây là những đặc trưng được trích xuất ra từ ảnh mà không hướng đến giải quyết cho một bài toán cụ thể. Có thể lấy ví dụ như Bag of Visual Words [[6]](#ref-6) hay Fisher Vectors [[7]](#ref-7). Với những kết quả tốt hơn so với những cách tiếp cận cũ, việc sử dụng các đặc trưng tổng quát đã chứng tỏ rằng các đặc trưng thẩm mỹ của ảnh vốn đã nằm trong các đặc trưng tổng quát mà không cần sử dụng những kỹ thuật chuyên biệt để trích xuất như với các đặc trưng được trích xuất bằng tay. Điều này đã đưa ta đến gần hơn với kỷ nguyên của những đặc trưng được học trực tiếp từ dữ liệu --- các đặc trưng được học bởi các mô hình học sâu.

### Các đặc trưng được học bởi các mô hình học sâu (Deep Features)
Các đặc trưng được học ra trực tiếp từ dữ liệu bởi các mô hình học sâu không yêu cầu cung cấp trước các tri thức về đánh giá thẩm mỹ ảnh. Mô hình học sâu sẽ tự học ra các luật từ ảnh đầu vào và nhãn, hay đáp án, tương ứng mà con người cung cấp. Ưu điểm của phương pháp này là cho kết quả tốt hơn nhiều so với việc sử dụng các đặc trưng được trích xuất bằng tay. Tuy nhiên, số lượng dữ liệu cần có là rất rất lớn và ta sẽ gần như không thể lý giải được những quyết định mà mô hình học sâu đưa ra khi đánh giá thẩm mỹ cho một tấm ảnh.

Một vài mô hình trích xuất đặc trưng được các công trình đánh giá thẩm mỹ ảnh khá ưa chuộng có thể kể đến như: AlexNet [[8]](#ref-8), VGG [[9]](#ref-9), MobileNet [[10](#ref-10),[11](#ref-11),[12](#ref-12)], ResNet [[13]](#ref-13). Từ những phần tiếp theo của bài viết, ta sẽ tập trung vào các công trình sử dụng các đặc trưng được học bởi các mô hình học sâu.

## Đầu ra của bài toán
Sau khi đã có đầu vào cho cỗ máy, ta sẽ mong muốn cỗ máy này tạo ra cho chúng ta một cái gì đấy. Các loại đầu ra của bài toán đánh giá thẩm mỹ ảnh có thể được chia thành bốn nhóm, phục vụ cho bốn bài toán: Phân lớp, hồi quy, xếp hạng, và giải thích.

### Bài toán phân lớp
Với bài toán phân lớp, đầu ra có thể là phân loại một ảnh vào nhóm có mức độ thẩm mỹ thấp/cao, hay phân loại vào nhóm điểm thẩm mỹ trong một khoảng điểm cố định cho trước (ví dụ 1, 2,..., 10). Độ đo thường được sử dụng để đánh giá cho bài toán này cũng giống với các bài toán phân lớp thông thường, ví dụ như <a href="https://en.wikipedia.org/wiki/Accuracy_and_precision" target="_blank">độ chính xác</a>, <a href="https://en.wikipedia.org/wiki/F-score" target="_blank">chỉ số F1</a>, v.v..

<center><img src="/img/academic/iaa/classification_problem.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

### Bài toán hồi quy
Sang đến bài toán hồi quy, một bức ảnh có thể được chấm điểm thẩm mỹ dưới dạng số thực. Độ đo phổ biến được sử dụng cho bài toán này gồm có <a href="https://en.wikipedia.org/wiki/Mean_squared_error" target="_blank">sai số toàn phương trung bình (Mean Squared Error)</a>, <a href="https://en.wikipedia.org/wiki/Mean_absolute_error" target="_blank">sai số tuyệt đối trung bình (Mean Absolute Error)</a>,v.v..

<center><img src="/img/academic/iaa/regression_problem.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

### Bài toán xếp hạng
Với bài toán xếp hạng, kiến trúc phổ biến sẽ là mạng Siamese (kiến trúc hai mạng được chia sẻ trọng số) [[14]](#ref-14) kết hợp với một <a href="https://gombru.github.io/2019/04/03/ranking_loss/" target="_blank">hàm mất mát (Loss Function) phục vụ cho bài toán xếp hạng</a>. Ngoài ra, ta còn có Triplet Network [[15]](#ref-15) (kiến trúc ba mạng được chia sẻ trọng số) kết hợp với Triplet Loss [[15]](#ref-15). <a href="https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient" target="_blank">Tương quan Spearman (Spearman’s correlation)</a> hay <a href="https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient" target="_blank">hệ số tương quan thứ tự xếp hạng Spearman (Spearman rank-order correlation coefficient)</a> là độ đo được phổ biến trong bài toán này.

<center><img src="/img/academic/iaa/ranking_problem.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

### Bài toán giải thích
Ngoài ra, một nhóm các bài toán tập trung vào việc giải thích cho những quyết định thẩm mỹ do mô hình máy học đưa ra cũng nhận được sự quan tâm từ giới nghiên cứu. Với các mô hình dựa trên kiến trúc <a href="https://cs231n.github.io/convolutional-networks/" target="_blank">mạng nơ-ron tích chập (Convolutional Neural Networks)</a>, các kỹ thuật như CAM [[16]](#ref-16), GradCAM [[17]](#ref-17) được sử dụng. Những bài toán giải thích quyết định đánh giá thẩm mỹ còn có thể tồn tại dưới dạng một <a href="https://en.wikipedia.org/wiki/Multi-task_learning" target="_blank">bài toán đa tác vụ (Multi-task)</a> nhằm đánh giá mức độ thẩm mỹ của ảnh trên nhiều tiêu chí một cách đồng thời [[18]](#ref-18), hay dưới dạng một <a href="https://paperswithcode.com/task/image-captioning" target="_blank">bài toán sinh chú thích cho ảnh (Image Captioning)</a> nhằm tạo ra những đoạn văn bản dùng để giải thích cho những quyết định về thẩm mỹ [[19]](#ref-19).


## Phạm vi của bài toán
Như đã đề cập trong những phần trên, quá trình đánh giá thẩm mỹ ảnh của con người luôn tồn tại yếu tố khách quan lẫn chủ quan trong đó.

Một cách phổ biến để gán nhãn dữ liệu cho bài toán đánh giá thẩm mỹ ảnh đó là chấm điểm cho mỗi bức ảnh thật nhiều lần với sự tham gia của nhiều cá nhân. Bằng cách này, độ thẩm mỹ của một bức ảnh sẽ được đại diện bởi một phân phối dữ liệu điểm.

<center><img src="/img/academic/iaa/image_subjectivity.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>
<center><i>Tính chủ quan trong chấm điểm thẩm mỹ cho ảnh [<a href="#ref-4">4</a>]</i></center>

Xét trên phạm vi của bài toán đánh giá thẩm mỹ, có hai hướng tiếp cận để giải quyết bài toán này.

### Đánh giá thẩm mỹ ảnh một cách tổng quát
Các công trình nghiên cứu đi theo hướng tiếp cận này coi thẩm mỹ là một thuộc tính cố hữu của ảnh, không phụ thuộc vào con mắt đánh giá của bất cứ cá nhân nào. Do đó, với mỗi ảnh đầu vào sẽ chỉ có một đầu ra tương ứng duy nhất đặc trưng cho độ thẩm mỹ của ảnh đó. Để có được dữ liệu cho việc huấn luyện mô hình, cách đơn giản nhất là sử dụng giá trị kỳ vọng, hay có thể hiểu đơn giản là giá trị trung bình, được tính ra từ phân phối dữ liệu điểm thẩm mỹ của từng ảnh.

Một số công trình thậm chí còn thiết kế ra các mô hình học trực tiếp các phân phối điểm của ảnh thay vì chỉ học ra các giá trị kỳ vọng. Việc tính toán sai số giữa kết quả dự đoán của mô hình và nhãn của dữ liệu sẽ cần các công cụ tính khoảng cách giữa các phân phối xác suất, ví dụ như <a href="https://en.wikipedia.org/wiki/Earth_mover%27s_distance" target="_blank">Earth mover's distance (EMD)</a>, <a href="https://stats.stackexchange.com/a/274861" target="_blank">Chi-square distance</a>, <a href="https://en.wikipedia.org/wiki/Kullback%E2%80%93Leibler_divergence" target="_blank">KL divergence</a>, v.v.. Tiêu biểu cho cách thiết kế này có thể kể đến NIMA [[20]](#ref-20). Mặc dù không phải công trình đầu tiên sử dụng EMD cho việc đánh giá thẩm mỹ ảnh, NIMA vẫn là cái tên được nhiều người biết đến nhất, thậm chí là khi nhắc đến bài toán đánh giá thẩm mỹ ảnh nói chung. Mã nguồn của công trình này đã được triển khai trên nhiều Framework phổ biến như <a href="https://github.com/idealo/image-quality-assessment" target="_blank">Tensorflow</a>, <a href="https://github.com/titu1994/neural-image-assessment" target="_blank">Keras</a>, <a href="https://github.com/yunxiaoshi/Neural-IMage-Assessment" target="_blank">PyTorch</a>.

### Đánh giá thẩm mỹ ảnh theo cá nhân
Ngoài cách tiếp cận theo hướng đánh giá thẩm mỹ một cách tổng quát cho ảnh, một số công trình giải quyết bài toán này theo hướng cá nhân hóa. Cách tiếp cận phổ biến của những công trình này là việc xuất phát từ các mô hình đánh giá thẩm mỹ ảnh tổng quát, từ đó sử dụng các dữ liệu ảnh được gán nhãn của từng cá nhân để huấn luyện ra mô hình phục vụ cho riêng cá nhân đó. Đôi khi, việc thu thập những dữ liệu được gán nhãn này tương đối tốn kém, thậm chí là bất khả thi trong nhiều trường hợp. Để giải quyết vấn đề này, một vài công trình thậm chí còn đề xuất thay thế bởi các nguồn dữ liệu khác mang tính cá nhân như hành vi sử dụng mạng xã hội.

Vậy là với ba khía cạnh vừa được đề cập, ta đã cùng nhau đi qua một lượt các vấn đề mà các công trình nghiên cứu về bài toán đánh giá thẩm mỹ ảnh đang giải quyết.

<br/>

---

# <a id="discussion"></a>Bàn luận

Ở phần cuối của bài blog, mình xin chia sẻ một vài suy nghĩ cá nhân khi bắt tay vào nghiên cứu chủ đề này.

Với mình, điểm khó nhất khi nghiên cứu bài toán đánh giá thẩm mỹ ảnh đó là làm sao để có thể định nghĩa được rõ ràng các tiêu chí đánh giá thẩm mỹ; ở đây mình tạm xét những tiêu chí được cho là có thể đánh giá về mặt kỹ thuật. Nhiều khi, cách định nghĩa các tiêu chí thẩm mỹ còn quyết định xem tiêu chí đó có thể đánh giá một cách khách quan hay không. Tiêu chí được định nghĩa càng rõ ràng thì càng dễ để cho con người hay thậm chí là máy móc đánh giá.

Thực sự đến bây giờ mình vẫn nghĩ, liệu rằng các giải pháp sử dụng các mô hình học sâu hiện tại cho việc giải quyết bài toán đánh giá thẩm mỹ, dù cũng đạt được những con số tạm gọi là "ấn tượng", dù cũng tự nhận là tốt hơn những công trình trước đây ở một mức nào đấy, liệu có thực sự học được cái gì đấy hay không, hay chỉ đơn giản là **OVERFITTING** trên bộ kiểm định của một bộ dữ liệu công khai nào đấy. Vì đã là mô hình học sâu thì cũng không cần phải quá quan tâm đến bên trong mô hình đang học như thế nào, học được cái gì, chỉ cần cung cấp đầu vào đúng định dạng là sẽ nhận được đầu ra mà thôi.

Cá nhân mình đánh giá, chắc sẽ cần phải một thời gian khá dài nữa trước khi giới nghiên cứu có thể hiểu bài toán đánh giá thẩm mỹ ảnh như những gì họ đã biết về bài toán phân lớp ảnh, bài toán phát hiện đối tượng trong ảnh, v.v., để đạt được đến giai đoạn mà máy móc vượt qua khả năng của con người, đến giai đoạn mà chỉ cần nhích thêm một vài phần trăm, phần nghìn của chỉ số là đã trở thành mô hình SOTA. Hi vọng, ta sẽ được nhìn thấy những giải pháp đột phá cho bài toán này trong khoảng 5--10 năm sắp tới.

<center><img src="/img/academic/iaa/iaa_expectancy.png" alt="" title="" style="max-width: 100%; height: auto;"/></center>

Tất cả những ý kiến mình nêu ra ở đây hoàn toàn dựa vào những hiểu biết mà mình có được cùng với những suy luận mang tính chủ quan; do đó, đôi chỗ có thể xuất hiện những nhận định chưa được chính xác. Hi vọng có thể nhận được những ý kiến đóng góp và chia sẻ từ phía cộng đồng để bản thân có thể hiểu sâu hơn về chủ đề này.

<br/>

---

# <a id="references"></a>Tài liệu tham khảo

[1] <a id="ref-1" href="http://tratu.soha.vn/dict/vn_vn/Th%E1%BA%A9m_m%C4%A9" target="_blank">Soha Dictionary</a>\
[2] <a id="ref-2" href="https://vtudien.com/viet-viet/dictionary/nghia-cua-tu-th%E1%BA%A9m%20m%E1%BB%B9" target="_blank">Vietnamese Dictionary</a>\
[3] <a id="ref-3" href="http://tratu.coviet.vn/hoc-tieng-anh/tu-dien/lac-viet/V-V/th%e1%ba%a9m+m%e1%bb%b9.html" target="_blank">Co Viet Dictionary</a>\
[4] <a id="ref-4" href="https://hal.archives-ouvertes.fr/hal-03311344/file/Subjectivity_and_Explainability_in_Image_Aesthetic_Quality_Assessment.pdf" target="_blank">Advances and Challenges in Computational Image Aesthetics</a>\
[5] <a id="ref-5" href="https://arxiv.org/pdf/2103.11616.pdf" target="_blank">A Survey on Image Aesthetic Assessment</a>\
[6] <a id="ref-6" href="https://www.cs.cmu.edu/~efros/courses/LBMV07/Papers/csurka-eccv-04.pdf" target="_blank">Visual Categorization with Bags of Keypoints</a>\
[7] <a id="ref-7" href="https://proceedings.neurips.cc/paper/1998/file/db1915052d15f7815c8b88e879465a1e-Paper.pdf" target="_blank">Exploiting Generative Models in Discriminative Classifiers</a>\
[8] <a id="ref-8" href="https://proceedings.neurips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf" target="_blank">ImageNet Classification with Deep Convolutional Neural Networks</a>\
[9] <a id="ref-9" href="https://arxiv.org/pdf/1409.1556.pdf" target="_blank">Very Deep Convolutional Networks for Large-Scale Image Recognition</a>\
[10] <a id="ref-10" href="https://arxiv.org/pdf/1704.04861.pdf" target="_blank">MobileNets: Efficient Convolutional Neural Networks for Mobile Vision Applications</a>\
[11] <a id="ref-11" href="https://arxiv.org/pdf/1801.04381.pdf" target="_blank">MobileNetV2: Inverted Residuals and Linear Bottlenecks</a>\
[12] <a id="ref-12" href="https://arxiv.org/pdf/1905.02244.pdf" target="_blank">Searching for MobileNetV3</a>\
[13] <a id="ref-13" href="https://arxiv.org/pdf/1512.03385.pdf" target="_blank">Deep Residual Learning for Image Recognition</a>\
[14] <a id="ref-14" href="http://yann.lecun.com/exdb/publis/pdf/chopra-05.pdf" target="_blank">Learning a Similarity Metric Discriminatively, with Application to Face Verification</a>\
[15] <a id="ref-15" href="https://arxiv.org/pdf/1412.6622.pdf" target="_blank">Deep metric learning using Triplet network</a>\
[16] <a id="ref-16" href="https://openaccess.thecvf.com/content_cvpr_2016/papers/Zhou_Learning_Deep_Features_CVPR_2016_paper.pdf" target="_blank">Learning Deep Features for Discriminative Localization</a>\
[17] <a id="ref-17" href="https://arxiv.org/pdf/1610.02391.pdf" target="_blank">Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization</a>\
[18] <a id="ref-18" href="https://arxiv.org/pdf/1606.01621.pdf" target="_blank">Photo Aesthetics Ranking Network with Attributes and Content Adaptation</a>\
[19] <a id="ref-19" href="https://arxiv.org/pdf/1908.11310.pdf" target="_blank">Aesthetic Image Captioning From Weakly-Labelled Photographs</a>\
[20] <a id="ref-20" href="https://arxiv.org/pdf/1709.05424.pdf" target="_blank">NIMA: Neural Image Assessment</a>

<hr style="border:1px solid gray">

<br/>

#### Nguồn các tấm ảnh được sử dụng trong bài blog
- <a href="https://xframe.io/photos/22262" target="_blank">https://xframe.io/photos/22262</a>
- <a href="https://madhansart.com/emphasis-in-art/" target="_blank">https://madhansart.com/emphasis-in-art/</a>
- <a href="https://www.flickr.com/photos/120139997@N08/14533502625/" target="_blank">https://www.flickr.com/photos/120139997@N08/14533502625/</a>
- <a href="https://www.flickr.com/photos/timw1/49061321922/" target="_blank">https://www.flickr.com/photos/timw1/49061321922/</a>
- <a href="https://www.freepik.com/free-vector/memphis-style-pattern-design_1065872.htm" target="_blank">https://www.freepik.com/free-vector/memphis-style-pattern-design_1065872.htm</a>
- <a href="https://www.pexels.com/photo/nature-bird-red-winter-46166/" target="_blank">https://www.pexels.com/photo/nature-bird-red-winter-46166/</a>
- <a href="https://www.pexels.com/photo/white-and-gray-bird-on-the-bag-of-brown-and-black-pig-swimming-on-the-beach-during-daytime-66258/" target="_blank">https://www.pexels.com/photo/white-and-gray-bird-on-the-bag-of-brown-and-black-pig-swimming-on-the-beach-during-daytime-66258/</a>
- <a href="https://www.pexels.com/photo/grey-bird-perched-on-a-tree-branch-2662434/" target="_blank">https://www.pexels.com/photo/grey-bird-perched-on-a-tree-branch-2662434/</a>
- <a href="https://www.pexels.com/photo/photo-of-yellow-and-blue-macaw-with-one-wing-open-perched-on-a-wooden-stick-2317904/" target="_blank">https://www.pexels.com/photo/photo-of-yellow-and-blue-macaw-with-one-wing-open-perched-on-a-wooden-stick-2317904/</a>
- <a href="https://www.pexels.com/photo/macro-photography-of-colorful-hummingbird-349758/" target="_blank">https://www.pexels.com/photo/macro-photography-of-colorful-hummingbird-349758/</a>
