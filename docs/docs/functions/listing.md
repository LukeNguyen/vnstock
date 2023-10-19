# Danh sách công ty niêm yết

```python
listing_companies(live=True)
```

Hàm có một tham số duy nhất `live` nhận một trong hai giá trị.

- `live=False`: Cho phép đọc dữ liệu cục bộ từ tệp csv [listing_companies](https://raw.githubusercontent.com/thinh-vu/vnstock/beta/data/listing_companies_enhanced-2023.csv) đính kèm trên Github theo mặc định. File này được cập nhật hàng tháng. Chứa thông tin rất chi tiết. Bởi danh sách các công ty niêm yết thường không thay đổi liên tục nên việc này không gây trở ngại nhiều.

- `live=True`: Cho phép đọc dữ liệu danh sách công ty niêm yết được cập nhật realtime từ API miễn phí do Wifeed cung cấp. Dữ liệu được trả về trong trường hợp này chỉ gồm 4 thông tin cơ bản: mã CK, tên công ty, mã phân loại công ty, sàn niêm yết.

- Kết quả trả về như sau cho chế độ realtime:

```shell
 listing_companies(True)
     ticker                                       organName  organTypeCode comGroupCode
0       A32                                         CTCP 32              1        UPCOM
1       AAA                          CTCP Nhựa An Phát Xanh              1         HOSE
2       AAM                            CTCP Thủy sản MeKong              1         HOSE
3       AAS                    CTCP Chứng khoán SmartInvest              4        UPCOM
4       AAT                CTCP Tập Đoàn Tiên Sơn Thanh Hóa              1         HOSE
...     ...                                             ...            ...          ...
1579    XPH                            CTCP Xà phòng Hà Nội              1        UPCOM
1580    YBC              CTCP Xi măng và Khoáng sản Yên Bái              1        UPCOM
1581    YBM             CTCP Khoáng sản Công nghiệp Yên Bái              1         HOSE
1582    YEG                             CTCP Tập đoàn Yeah1              1         HOSE
1583    YTC  CTCP Xuất nhập khẩu Y tế Thành phố Hồ Chí Minh              1        UPCOM
```


- Kết quả trả về cho chế độ offline:

```shell
listing_companies()
  ticker comGroupCode                                          organName   organShortName  ...   VNIT  VNMAT VNREAL  VNUTI
0    SSI         HOSE                    Công ty Cổ phần Chứng khoán SSI  Chứng khoán SSI  ...  False  False  False  False
1    BCM         HOSE  Tổng Công ty Đầu tư và Phát triển Công nghiệp ...      Becamex IDC  ...  False  False   True  False
2    VHM         HOSE                           Công ty Cổ phần Vinhomes         Vinhomes  ...  False  False   True  False

[3 rows x 35 columns]
```