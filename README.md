# Danh sách các hàm


### 1.  Dữ liệu Room nước ngoài
<ins>Input</ins>
FOREIGN: Stock code

VD: FOREIGN:VNM hoặc FOREIGN:VNM,ACB

<ins>Output</ins>

| **Tên Trường**        | **Kiểu Dữ Liệu**  | **Mô Tả**                                            | **Giá Trị/Định Dạng**           |
| --------------------- | --------          | -----------------------------------------------------| --------------------------------|
| **Rtype**             | String            | Xác định loại dữ liệu. Luôn có giá trị là `FOREIGN`. | `FOREIGN`                       |
| **StockCode**         | String            | Mã chứng khoán đại diện cho công ty.                 | Ví dụ: `VNM`                    |
| **TradingDate**       | Date              | Ngày giao dịch.                                      | Định dạng: `YYYY-MM-DDTHH:MM:SS`|
| **TotalRoom**         | Number      | Tổng room dành cho nhà đầu tư nước ngoài.                  | Ví dụ: `2089955445.0`           |
| **OpenRoom**          | Number      | Room còn lại khi bắt đầu phiên giao dịch.                  | Ví dụ: `984152735.0`            |
| **CurrRoom**          | Number      | Room còn lại hiện tại cho nhà đầu tư nước ngoài.           | Ví dụ: `984152735.0`            |
| **BuyVol**            | Number      | Khối lượng cổ phiếu mua trong phiên giao dịch.             | Ví dụ: `96.30`                  |
| **SellVol**           | Number      | Khối lượng cổ phiếu bán trong phiên giao dịch.             | Ví dụ: `0.0`                    |
| **BuyVal**            | Number      | Tổng giá trị cổ phiếu mua.                                 | Ví dụ: `0.0`                    |
| **SellVal**           | Number      | Tổng giá trị cổ phiếu bán.                                 | Ví dụ: `0.0`                    |
| **OwnedRatio**        | Number      | Tỷ lệ sở hữu của nhà đầu tư nước ngoài.                    | Ví dụ: `4.81`                   |
| **OwnedRatioOrgData** | Number      | Tỷ lệ sở hữu gốc.                                          | Ví dụ: `0.0000`                 |
| **TotalBuyVol**       | Number      | Khối lượng cổ phiếu mua tích lũy.                          | Ví dụ: `0.0`                    |
| **TotalSellVol**      | Number      | Khối lượng cổ phiếu bán tích lũy.                          | Ví dụ: `0.0`                    |
| **TotalBuyVal**       | Number      | Tổng giá trị cổ phiếu mua tích lũy.                        | Ví dụ: `0.0`                    |
| **TotalSellVal**      | Number      | Tổng giá trị cổ phiếu bán tích lũy.                        | Ví dụ: `0.0`                    |
| **BuyPutVol**         | Number      | Khối lượng thỏa thuận hợp đồng mua quyền bán.              | Ví dụ: `0.0`                    |
| **BuyPutVal**         | Number      | Giá trị thỏa thuận hợp đồng mua quyền bán.                 | Ví dụ: `0.0`                    |
| **SellPutVol**        | Number      | Khối lượng thỏa thuận hợp đồng bán quyền bán.              | Ví dụ: `0.0`                    |
| **SellPutVal**        | Number      | Giá trị thỏa thuận hợp đồng bán quyền bán.                 | Ví dụ: `0.0`                    |
| **LastUpdate**        | Date Giờ    | Dấu thời gian cập nhật lần cuối.                           | Định dạng: `YYYY-MM-DDTHH:MM:SS`|

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

| **Tên Trường**        | **Kiểu Dữ Liệu** | **Mô Tả**                                         | **Giá Trị/Định Dạng**          |
| --------------------- | ---------------- | ------------------------------------------------- | ------------------------------ |
| **DataType**          | String           | Xác định loại dữ liệu.                            | Ví dụ: `X-TRADE`               |
| **Package**           | Number           | Gói giao dịch.                                    | Ví dụ: `74501`                 |
| **StockCode**         | String           | Mã chứng khoán đại diện cho công ty.              | Ví dụ: `ACB`                   |
| **TradingDate**       | DateTime         | Ngày giao dịch.                                   | Định dạng: `YYYY-MM-DDTHH:MM:SS` |
| **Price**             | Number           | Giá giao dịch.                                    | Ví dụ: `42150.00`              |
| **Vol**               | Number           | Khối lượng giao dịch.                             | Ví dụ: `900.0`                 |
| **TotalVol**          | Number           | Tổng khối lượng giao dịch.                        | Ví dụ: `1197700.0`             |
| **TotalVal**          | Number           | Tổng giá trị giao dịch.                           | Ví dụ: `50483055000.0`         |
| **Change**            | Number           | Biến động giá.                                    | Ví dụ: `2750.00`               |
| **IsBuy**             | Number (0 hoặc 1)| Giao dịch mua hay bán.                            | `0`: Bán, `1`: Mua             |
| **PerChange**         | Number (%)       | Biến động giá theo phần trăm.                     | Ví dụ: `6.98`                  |
| **LastUpdate**        | DateTime         | Thời điểm cập nhật cuối.                          | Định dạng: `YYYY-MM-DDTHH:MM:SS.sss` |

**Example**
```json
{
  "DataType": "X-TRADE",
  "Package": 74501,
  "Stockcode": "ACB",
  "TradingDate": "2024-04-01T14:45:00.217",
  "Price": 42150,
  "Vol": 900,
  "TotalVol": 1197700,
  "TotalVal": 50483055000,
  "Change": 2750,
  "IsBuy": 0,
  "PerChange": 6.98,
  "LastUpdate": "2024-04-03T14:45:05.69"
}
```
### 4. Dữ liệu thị trường

<ins>Input</ins>
X_TRADE: Stock code

VD: X_STOCK_BEST_PRICE:VNM, X_STOCK_BEST_PRICE:VNM,ACB hoặc X_STOCK_BEST_PRICE:ALL

<ins>Output</ins>

| **Tên Trường**       | **Kiểu Dữ Liệu** | **Mô Tả**                                       | **Giá Trị/Định Dạng**          |
|----------------------|-----------------|-------------------------------------------------|--------------------------------|
| **Best1Bid**        | Decimal         | Giá đặt mua tốt nhất 1                          | Ví dụ: `8000.0`               |
| **Best1BidVol**     | Decimal         | Khối lượng đặt mua tốt nhất 1                   | Ví dụ: `27300.0`              |
| **Best1Offer**      | Decimal         | Giá đặt bán tốt nhất 1                          | Ví dụ: `8100.0`               |
| **Best1OfferVol**   | Decimal         | Khối lượng đặt bán tốt nhất 1                   | Ví dụ: `56300.0`              |
| **Best2Bid**        | Decimal         | Giá đặt mua tốt nhất 2                          | Ví dụ: `7900.0`               |
| **Best2BidVol**     | Decimal         | Khối lượng đặt mua tốt nhất 2                   | Ví dụ: `52000.0`              |
| **Best2Offer**      | Decimal         | Giá đặt bán tốt nhất 2                          | Ví dụ: `8200.0`               |
| **Best2OfferVol**   | Decimal         | Khối lượng đặt bán tốt nhất 2                   | Ví dụ: `23700.0`              |
| **Best3Bid**        | Decimal         | Giá đặt mua tốt nhất 3                          | Ví dụ: `7800.0`               |
| **Best3BidVol**     | Decimal         | Khối lượng đặt mua tốt nhất 3                   | Ví dụ: `54100.0`              |
| **Best3Offer**      | Decimal         | Giá đặt bán tốt nhất 3                          | Ví dụ: `8300.0`               |
| **Best3OfferVol**   | Decimal         | Khối lượng đặt bán tốt nhất 3                   | Ví dụ: `24400.0`              |
| **Exchange**        | String          | Sàn giao dịch                                  | Ví dụ: `HNX`                  |
| **StockCode**       | String          | Mã chứng khoán đại diện cho công ty            | Ví dụ: `DVM`                  |
| **TradingDate**     | DateTime        | Ngày giao dịch                                 | Định dạng: `YYYY-MM-DDTHH:MM:SS` |
| **LastUpdate**      | DateTime        | Thời điểm cập nhật cuối                        | Định dạng: `YYYY-MM-DDTHH:MM:SS.sss` |

**Example**
```json
{
  "Best1Bid": 8000,
  "Best1BidVol": 27300,
  "Best1Offer": 8100,
  "Best1OfferVol": 56100,
  "Best2Bid": 7900,
  "Best2BidVol": 52000,
  "Best2Offer": 8200,
  "Best2OfferVol": 23700,
  "Best3Bid": 7800,
  "Best3BidVol": 54100,
  "Best3Offer": 8300,
  "Best3OfferVol": 24400,
  "Exchange": "HNX",
  "StockCode": "DVM",
  "TradingDate": "2025-02-05T00:00:00",
  "LastUpdate": "2025-02-05T14:26:54.22"
}
```
### 5. Dữ liệu Index

<ins>Input</ins>
X_EXCHANGE: Stock code

VD: X_EXCHANGE:VN30, X_EXCHANGE:VN30-HNXindex,VN30 hoặc X_EXCHANGE:ALL

<ins>Output</ins>

| **Tên Trường**         | **Kiểu Dữ Liệu** | **Mô Tả**                                      | **Giá Trị/Định Dạng**            |
|------------------------|-----------------|------------------------------------------------|----------------------------------|
| **CloseIndex**        | Decimal         | Chỉ số đóng cửa                                | Ví dụ: `95.74`                 |
| **DiffBuySellTrade**  | Decimal         | Chênh lệch số lượng giao dịch mua - bán        | Ví dụ: `654.0`                 |
| **DiffBuySellVol**    | Decimal         | Chênh lệch khối lượng mua - bán                | Ví dụ: `-26428400.0`           |
| **Exchange**         | String          | Sàn giao dịch                                  | Ví dụ: `UPCOM`                 |
| **ForeignBuyPutVal** | Decimal         | Giá trị đặt mua của nhà đầu tư nước ngoài      | Ví dụ: `0.0`                   |
| **ForeignBuyPutVol** | Decimal         | Khối lượng đặt mua của nhà đầu tư nước ngoài   | Ví dụ: `0.0`                   |
| **ForeignBuyVal**    | Decimal         | Giá trị mua của nhà đầu tư nước ngoài          | Ví dụ: `0.0`                   |
| **ForeignBuyVol**    | Decimal         | Khối lượng mua của nhà đầu tư nước ngoài       | Ví dụ: `0.0`                   |
| **ForeignSellPutVal** | Decimal        | Giá trị đặt bán của nhà đầu tư nước ngoài      | Ví dụ: `0.0`                   |
| **ForeignSellPutVol** | Decimal        | Khối lượng đặt bán của nhà đầu tư nước ngoài   | Ví dụ: `0.0`                   |
| **ForeignSellVal**    | Decimal        | Giá trị bán của nhà đầu tư nước ngoài          | Ví dụ: `0.0`                   |
| **ForeignSellVol**    | Decimal        | Khối lượng bán của nhà đầu tư nước ngoài       | Ví dụ: `0.0`                   |
| **HighestIndex**     | Decimal         | Chỉ số cao nhất trong phiên                    | Ví dụ: `95.89`                 |
| **IndexCode**        | String          | Mã chỉ số                                      | Ví dụ: `UPCOMINDEX`            |
| **LowestIndex**      | Decimal         | Chỉ số thấp nhất trong phiên                   | Ví dụ: `95.12`                 |
| **OpenIndex**        | Decimal         | Chỉ số mở cửa                                  | Ví dụ: `95.31`                 |
| **PriorIndex**       | Decimal         | Chỉ số tham chiếu                              | Ví dụ: `95.31`                 |
| **Row**             | Long            | Số thứ tự hàng dữ liệu                         | Ví dụ: `3`                     |
| **Rows**            | Int             | Tổng số hàng dữ liệu                           | Ví dụ: `4`                     |
| **TotalBuyTrade**   | Decimal         | Tổng số lệnh mua                               | Ví dụ: `207361.0`              |
| **TotalBuyVal**     | Decimal         | Tổng giá trị giao dịch mua                     | Ví dụ: `0.0`                   |
| **TotalBuyVol**     | Decimal         | Tổng khối lượng giao dịch mua                 | Ví dụ: `787302900.0`           |
| **TotalPutVal**     | Decimal         | Tổng giá trị đặt lệnh                          | Ví dụ: `35543052100.0`         |
| **TotalPutVol**     | Decimal         | Tổng khối lượng đặt lệnh                       | Ví dụ: `4473309.0`             |
| **TotalSellTrade**  | Decimal         | Tổng số lệnh bán                               | Ví dụ: `206707.0`              |
| **TotalSellVal**    | Decimal         | Tổng giá trị giao dịch bán                     | Ví dụ: `0.0`                   |
| **TotalSellVol**    | Decimal         | Tổng khối lượng giao dịch bán                 | Ví dụ: `813731300.0`           |
| **TotalVal**        | Decimal         | Tổng giá trị giao dịch                         | Ví dụ: `659546112200.0`        |
| **TotalVol**        | Decimal         | Tổng khối lượng giao dịch                      | Ví dụ: `38985470.0`            |
| **TradingDate**     | DateTime        | Ngày giao dịch                                 | Định dạng: `YYYY-MM-DDTHH:MM:SS` |
| **LastUpdate**      | DateTime        | Thời điểm cập nhật cuối                        | Định dạng: `YYYY-MM-DDTHH:MM:SS.sss` |

**Example**
```json
{
  "CloseIndex": 228.2,
  "DiffBuySellTrade": 481,
  "DiffBuySellVol": -28087300,
  "Exchange": "HNX",
  "ForeignBuyPutVal": 0,
  "ForeignBuyPutVol": 0,
  "ForeignBuyVal": 0,
  "ForeignBuyVol": 0,
  "ForeignSellPutVal": 0,
  "ForeignSellPutVol": 0,
  "ForeignSellVal": 0,
  "ForeignSellVol": 0,
  "HighestIndex": 228.46,
  "IndexCode": "HNXINDEX",
  "LowestIndex": 223.31,
  "OpenIndex": 226,
  "PriorIndex": 226.61,
  "Row": 1,
  "Rows": 2,
  "TotalBuyTrade": 206679,
  "TotalBuyVal": 0,
  "TotalBuyVol": 784277400,
  "TotalPutVal": 6676830000,
  "TotalPutVol": 399400,
  "TotalSellTrade": 206198,
  "TotalSellVal": 0,
  "TotalSellVol": 812364700,
  "TotalVal": 769440559700,
  "TotalVol": 45787871,
  "TradingDate": "2025-02-05T00:00:00",
  "LastUpdate": "2025-02-05T14:43:16.217"
}
```
