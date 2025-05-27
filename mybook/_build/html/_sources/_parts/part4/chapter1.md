# 流程圖節點介紹
展示當前策略Studio的區塊中所能使用之節點，與對應的簡易說明。


<table style="border-collapse: collapse; width: 100%; font-size: 14px;">
  <thead style="background-color: #1f4e78; color: white;">
    <tr>
      <th style="width:10%; border: 1px solid black; padding: 8px; color: white;">主章節</th>
      <th style="width:15%; border: 1px solid black; padding: 8px; color: white;">子章節</th>
      <th style="width:75%; border: 1px solid black; padding: 8px; color: white;">簡易說明</th>
    </tr>
  </thead>
  <tbody>
    <tr style="background-color: #f9f9f9;">
      <td rowspan="3" style="border: 1px solid black; padding: 8px; vertical-align: top;">資料載入</td>
      <td style="border: 1px solid black; padding: 8px;">最新資料</td>
      <td style="border: 1px solid black; padding: 8px;">載入每檔股票於最新一日的欄位資料。</td>
    </tr>
    <tr style="background-color: #ffffff;">
      <td style="border: 1px solid black; padding: 8px;">歷史資料</td>
      <td style="border: 1px solid black; padding: 8px;">載入每檔股票於過去歷史的欄位資料。</td>
    </tr>
    <tr style="background-color: #f9f9f9;">
      <td style="border: 1px solid black; padding: 8px;">通用欄位方塊</td>
      <td style="border: 1px solid black; padding: 8px;">用作後續比較運算的判斷基準，可輸入常數、小數點、文字與布林值。</td>
    </tr>
    <tr style="background-color: #f9f9f9;">
      <td rowspan="3" style="border: 1px solid black; padding: 8px; vertical-align: top;">條件計算</td>
      <td style="border: 1px solid black; padding: 8px;">比較運算</td>
      <td style="border: 1px solid black; padding: 8px;">x欄位與y欄位之間的關係運算子，支援大於、大於等於、小於、小於等於、等於和不等於六種選項。</td>
    </tr>
    <tr style="background-color: #ffffff;">
      <td style="border: 1px solid black; padding: 8px;">邏輯運算</td>
      <td style="border: 1px solid black; padding: 8px;">複數個運算子產出之間的邏輯運算子，支援聯集（or）和交集（and）兩種選項。</td>
    </tr>
    <tr style="background-color: #ffffff;">
      <td style="border: 1px solid black; padding: 8px;">分組運算</td>
      <td style="border: 1px solid black; padding: 8px;">將指定資料切割成組別，或篩選出最高/低的N支股票，支援等量分N組、等距分N組、最高N檔、最低N檔與介於min~max等五種選項。</td>
    </tr>
    <tr style="background-color: #f9f9f9;">
      <td rowspan="5" style="border: 1px solid black; padding: 8px; vertical-align: top;">回測產出</td>
      <td style="border: 1px solid black; padding: 8px;">Pipeline 產出</td>
      <td style="border: 1px solid black; padding: 8px;">將連結的資料載入與條件計算區塊使用表格產出，方便使用者查看篩選出的股票。</td>
    </tr>
    <tr style="background-color: #ffffff;">
      <td style="border: 1px solid black; padding: 8px;">交易時間</td>
      <td style="border: 1px solid black; padding: 8px;">提供給回測計算節點，設定投組再平衡頻率與遞延天數，支援每日、每週初/末和每月初/末等五種選項。</td>
    </tr>
    <tr style="background-color: #f9f9f9;">
      <td style="border: 1px solid black; padding: 8px;">滑價手續費</td>
      <td style="border: 1px solid black; padding: 8px;">提供給回測計算節點，設定投組交易時的滑價與手續費成本模型，滑價模型支援無滑價、固定金額滑價、固定基點滑價、交易量滑價、百分比滑價與台股滑價等六種選項；手續費模型支援無手續費、每交易股數、每交易筆數、每交易金額與台股手續費等五種選項。</td>
    </tr>
    <tr style="background-color: #ffffff;">
      <td style="border: 1px solid black; padding: 8px;">訂單參數</td>
      <td style="border: 1px solid black; padding: 8px;">提供給回測計算節點，設定更多關於投組內股票的交易邏輯，包含成交時點、每檔股票最大槓桿、訂單存活日和下單股數加權模型等四種選項。</td>
    </tr>
    <tr style="background-color: #f9f9f9;">
      <td style="border: 1px solid black; padding: 8px;">回測計算</td>
      <td style="border: 1px solid black; padding: 8px;">接收前述Pipeline產出、交易時間、滑價手續費與訂單參數等區塊參數，設定回測之起訖時間和交易本金。</td>
    </tr>
  </tbody>
</table>



