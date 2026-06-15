DAX クエリービューでメジャーを一括登録するコードを下記に記します。

```
DEFINE
	MEASURE FactSales[売上金額] =
		SUM ( FactSales[TotalIncludingTax] )

	MEASURE FactSales[売上総利益] =
		SUM ( FactSales[Profit] )

	MEASURE FactSales[請求書数] =
		DISTINCTCOUNT ( FactSales[WWIInvoiceId] )

	MEASURE FactSales[販売明細数] =
		DISTINCTCOUNT ( FactSales[SaleKey] )

	MEASURE FactSales[平均請求額] =
		DIVIDE ( [売上金額], [請求書数] )

	MEASURE FactSales[粗利率] =
		DIVIDE ( [売上総利益], [売上金額] )

	MEASURE FactSales[前年同期間売上] =
		CALCULATE ( [売上金額], SAMEPERIODLASTYEAR ( DimDate[Date] ) )

	MEASURE FactSales[納品日基準売上金額] =
		CALCULATE ( [売上金額], USERELATIONSHIP ( DimDate[Date], FactSales[DeliveryDate] ) )

	MEASURE FactSales[納品日基準年初来売上] =
		CALCULATE (
			[売上金額],
			USERELATIONSHIP ( DimDate[Date], FactSales[DeliveryDate] ),
			DATESYTD ( DimDate[Date] )
		)

	MEASURE FactSales[納品日基準前年同期間売上] =
		CALCULATE (
			[売上金額],
			USERELATIONSHIP ( DimDate[Date], FactSales[DeliveryDate] ),
			SAMEPERIODLASTYEAR ( DimDate[Date] )
		)

EVALUATE
	ROW ( "Status", "Measures defined" )
```