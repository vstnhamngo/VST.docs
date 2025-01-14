# Danh sách các hàm


### 1.  Dữ liệu Room nước ngoài
<ins>Input</ins>
FOREIGN: Stock code

VD: FOREIGN:VNM hoặc FOREIGN:VNM,ACB

<ins>Output</ins>

| **Tên Trường**        | **Kiểu Dữ Liệu** | **Mô Tả**                                             | **Giá Trị/Định Dạng**                  |
| --------------------- | -------- | ----------------------------------------------------------- | --------------------------------- |
| **Rtype**             | String   | Xác định loại dữ liệu. Luôn có giá trị là `FOREIGN`. | `FOREIGN`                         |
| **StockCode**         | String   | Mã chứng khoán đại diện cho công ty.                       | Ví dụ: `VNM`                    |
| **TradingDate**       | Date     | Ngày giao dịch.                                         | Định dạng: `YYYY-MM-DDTHH:MM:SS`     |
| **TotalRoom**         | Number      | Tổng room dành cho nhà đầu tư nước ngoài.                 | Ví dụ: `2089955445.0`           |
| **OpenRoom**          | Number      | Room còn lại khi bắt đầu phiên giao dịch.         | Ví dụ: `984152735.0`            |
| **CurrRoom**          | Number      | Room còn lại hiện tại cho nhà đầu tư nước ngoài.               | Ví dụ: `984152735.0`            |
| **BuyVol**            | Number      | Khối lượng cổ phiếu mua trong phiên giao dịch.                 | Ví dụ: `96.30`                  |
| **SellVol**           | Number      | Khối lượng cổ phiếu bán trong phiên giao dịch.                   | Ví dụ: `0.0`                    |
| **BuyVal**            | Number      | Tổng giá trị cổ phiếu mua.                               | Ví dụ: `0.0`                    |
| **SellVal**           | Number      | Tổng giá trị cổ phiếu bán.                                 | Ví dụ: `0.0`                    |
| **OwnedRatio**        | Number      | Tỷ lệ sở hữu của nhà đầu tư nước ngoài.          | Ví dụ: `4.81`                   |
| **OwnedRatioOrgData** | Number      | Tỷ lệ sở hữu gốc.                              | Ví dụ: `0.0000`                 |
| **TotalBuyVol**       | Number      | Khối lượng cổ phiếu mua tích lũy.                   | Ví dụ: `0.0`                    |
| **TotalSellVol**      | Number      | Khối lượng cổ phiếu bán tích lũy.                     | Ví dụ: `0.0`                    |
| **TotalBuyVal**       | Number      | Tổng giá trị cổ phiếu mua tích lũy.                    | Ví dụ: `0.0`                    |
| **TotalSellVal**      | Number      | Tổng giá trị cổ phiếu bán tích lũy.                      | Ví dụ: `0.0`                    |
| **BuyPutVol**         | Number      | Khối lượng hợp đồng mua quyền bán.                               | Ví dụ: `0.0`                    |
| **BuyPutVal**         | Number      | Giá trị hợp đồng mua quyền bán.                                | Ví dụ: `0.0`                    |
| **SellPutVol**        | Number      | Khối lượng hợp đồng bán quyền bán.                                 | Ví dụ: `0.0`                    |
| **SellPutVal**        | Number      | Giá trị hợp đồng bán quyền bán.                                  | Ví dụ: `0.0`                    |
| **LastUpdate**        | Date Giờ | Dấu thời gian cập nhật lần cuối.                               | Định dạng: `YYYY-MM-DDTHH:MM:SS.sss` |

**Example**

```json
{
   "DataType": "Foreign",
   "StockCode": "VNM",
   "TradingDate": "2024-03-01T00:00:00",
   "TotalRoom": 2.089955445E9,
   "OpenRoom": 9.84152735E8,
   "CurrRoom": 9.84152735E8,
   "BuyVol": 96.3,
   "SellVol": 0,
   "BuyVal": 0,
   "SellVal": 0,
   "OwnedRatio": 4.81,
   "OwnedRatioOrgData": 0,
   "TotalBuyVol": 0,
   "TotalSellVol": 0,
   "TotalBuyVal": 0,
   "TotalSellVal": 0,
   "BuyPutVol": 0,
   "BuyPutVal": 0,
   "SellPutVol": 0,
   "SellPutVal": 0,
   "LastUpdate": "2024-03-01T11:13:12.49"
}
```

### 2.  Dữ liệu giao dịch

<ins>Input</ins>
X_TRADING_INFO: Stock code

VD: X_TRADING_INFO:VNM hoặc X_TRADING_INFO:VNM,ACB

<ins>Output</ins>
| **Tên Trường**         | **Kiểu Dữ Liệu** | **Mô Tả**                                 | **Giá Trị/Định Dạng**                  |
| ---------------------- | ---------------- | ----------------------------------------- | --------------------------------------- |
| **DataType**           | String           | Xác định loại dữ liệu.                    | Ví dụ: `X-TradingInfo`                 |
| **StockCode**          | String           | Mã chứng khoán đại diện cho công ty.      | Ví dụ: `ACB`                           |
| **LastUpdate**         | DateTime         | Thời điểm cập nhật cuối.                  | Định dạng: `YYYY-MM-DDTHH:MM:SS.sss`   |
| **TradingDate**        | DateTime         | Ngày giao dịch.                          | Định dạng: `YYYY-MM-DDTHH:MM:SS`       |
| **BasicPrice**         | Number           | Giá cơ bản.                              | Ví dụ: `23800.0`                       |
| **PriorLastPrice**     | Number           | Giá đóng cửa trước đó.                   | Ví dụ: `23800.0`                       |
| **PriorClosePrice**    | Number           | Giá đóng cửa phiên trước.                | Ví dụ: `23800.0`                       |
| **CeilingPrice**       | Number           | Giá trần.                                | Ví dụ: `26100.0`                       |
| **FloorPrice**         | Number           | Giá sàn.                                 | Ví dụ: `21500.0`                       |
| **OpenPrice**          | Number           | Giá mở cửa.                              | Ví dụ: `2784.53`                       |
| **ClosePrice**         | Number           | Giá đóng cửa.                            | Ví dụ: `24300.0`                       |
| **LastPrice**          | Number           | Giá giao dịch cuối cùng.                 | Ví dụ: `24300.0`                       |
| **LastVol**            | Number           | Khối lượng giao dịch cuối cùng.          | Ví dụ: `600.0`                         |
| **TotalVol**           | Number           | Tổng khối lượng giao dịch.               | Ví dụ: `4443379.0`                     |
| **TotalVal**           | Number           | Tổng giá trị giao dịch.                  | Ví dụ: `107669251000.0`                |
| **HighestPrice**       | Number           | Giá cao nhất.                            | Ví dụ: `18027.58`                      |
| **LowestPrice**        | Number           | Giá thấp nhất.                           | Ví dụ: `19286.46`                      |
| **AvrPrice**           | Number           | Giá trung bình.                          | Ví dụ: `24200.0`                       |
| **TotalTrade**         | Number           | Tổng số giao dịch.                       | Ví dụ: `511.0`                         |
| **KLCPLH**             | Number           | Khối lượng cổ phiếu lưu hành.            | Ví dụ: `1656515277.0`                  |
| **KLCPNY**             | Number           | Khối lượng cổ phiếu niêm yết.            | Ví dụ: `1662737277.0`                  |
| **KLCPLK**             | Number           | Khối lượng cổ phiếu lưu ký.              | Ví dụ: `0.0`                           |
| **KLCPLHDC**           | Number           | Khối lượng cổ phiếu lưu hành dự kiến.    | Ví dụ: `0.0`                           |
| **Change**             | Number           | Biến động giá.                           | Ví dụ: `500.0`                         |
| **PerChange**          | Number (%)       | Biến động giá theo phần trăm.            | Ví dụ: `2.10`                          |
| **TotalBuyTrade**      | Number           | Tổng số giao dịch mua.                   | Ví dụ: `956.0`                         |
| **TotalBuyVol**        | Number           | Tổng khối lượng mua.                     | Ví dụ: `5464100.0`                     |
| **OutstandingBuy**     | Number           | Khối lượng mua chưa khớp.                | Ví dụ: `1020721.0`                     |
| **TotalSellTrade**     | Number           | Tổng số giao dịch bán.                   | Ví dụ: `1082.0`                        |
| **TotalSellVol**       | Number           | Tổng khối lượng bán.                     | Ví dụ: `5460100.0`                     |
| **OutstandingSell**    | Number           | Khối lượng bán chưa khớp.                | Ví dụ: `1016721.0`                     |
| **BestBidVol**         | Number           | Khối lượng đặt mua tốt nhất.             | Ví dụ: `0.0`                           |
| **BestSellVol**        | Number           | Khối lượng đặt bán tốt nhất.             | Ví dụ: `0.0`                           |
| **BestBuy**            | Number           | Giá đặt mua tốt nhất.                    | Ví dụ: `0.0`                           |
| **BestSell**           | Number           | Giá đặt bán tốt nhất.                    | Ví dụ: `0.0`                           |
| **Spread**             | Number           | Chênh lệch giá.                          | Ví dụ: `0.0`                           |
| **AdjustRate**         | Number           | Tỷ lệ điều chỉnh.                        | Ví dụ: `0.000000000`                   |
| **TotalAdjustRate**    | Number           | Tổng tỷ lệ điều chỉnh.                   | Ví dụ: `1.000000`                      |
| **CorrectDiff**        | Number           | Sai lệch điều chỉnh.                     | Ví dụ: `0.00`                          |
| **IndexChange**        | Number           | Thay đổi chỉ số.                         | Ví dụ: `0.4312`                        |
| **AvrPriceFullTime**   | Number           | Giá trung bình trong phiên giao dịch.    | Ví dụ: `24200.0`                       |
| **MarketStatus**       | Number           | Trạng thái thị trường.                   | Ví dụ: `0`                             |

**Example**

```json
{
   "DataType": "X-TradingInfo",
   "StockCode": "VNM",
   "LastUpdate": "2020-01-20T21:40:00.807",
   "TradingDate": "2020-01-20T15:00:00",
   "BasicPrice": 118600,
   "PriorLastPrice": 118600,
   "PriorClosePrice": 118600,
   "CeilingPrice": 126900,
   "FloorPrice": 110300,
   "OpenPrice": 13921.24,
   "ClosePrice": 119000,
   "LastPrice": 119000,
   "LastVol": 82080,
   "TotalVol": 493600,
   "TotalVal": 5.8659E10,
   "HighestPrice": 86991.12,
   "LowestPrice": 95936.4,
   "AvrPrice": 118839,
   "TotalTrade": 489,
   "KLCPLH": 1.741377694E9,
   "KLCPNY": 1.741687793E9,
   "KLCPLK": 0,
   "KLCPLHDC": 1.741378252E9,
   "Change": 400,
   "PerChange": 0.34,
   "TotalBuyTrade": 674,
   "TotalBuyVol": 506530,
   "OutstandingBuy": 12930,
   "TotalSellTrade": 638,
   "TotalSellVol": 525110,
   "OutstandingSell": 31510,
   "BestBidVol": 6260,
   "BestSellVol": 9030,
   "BestBuy": 119100,
   "BestSell": 119100,
   "Spread": -100,
   "AdjustRate": 0,
   "TotalAdjustRate": 1,
   "CorrectDiff": 0,
   "IndexChange": 0.0208,
   "AvrPriceFullTime": 118839,
   "MarketStatus": 0
}
```
### 3.  Khớp lệnh theo lô

<ins>Input</ins>
X_TRADE: Stock code

VD: X_TRADE:VNM hoặc X_TRADE:VNM,ACB

<ins>Output</ins>
