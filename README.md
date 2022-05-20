Select O.CustomerID as [Customer ID], count(OL.OrderID) as [Order ID]
From [WideWorldImporters].Sales.Orders as O
Inner Join [WideWorldImporters].[Sales].[OrderLines] as OL
ON O.OrderID = OL.OrderID
Group By O.CustomerID
Order By [Order ID] Desc 
