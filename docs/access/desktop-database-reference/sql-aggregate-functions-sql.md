---
title: SQL 集計関数 (SQL)
TOCTitle: SQL aggregate functions (SQL)
ms:assetid: 8866cd71-0216-25b4-6a6a-02cb7acad9a2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197054(v=office.15)
ms:contentKeyID: 48546136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 946afd4ad9c1a2976e4833b59fa8467911ac1c56
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945979"
---
# <a name="sql-aggregate-functions-sql"></a><span data-ttu-id="d8df6-102">SQL 集計関数 (SQL)</span><span class="sxs-lookup"><span data-stu-id="d8df6-102">SQL aggregate functions (SQL)</span></span>


<span data-ttu-id="d8df6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d8df6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8df6-p101">SQL 集計関数を使用すると、値の集合からさまざまな統計情報を求めることができます。SQL 集計関数は、 **QueryDef** オブジェクトの **SQL** プロパティのクエリおよび集計式で使用できます。また、SQL クエリに基づく **Recordset** オブジェクトを作成する場合にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="d8df6-p101">Using the SQL aggregate functions, you can determine various statistics on sets of values. You can use these functions in a query and aggregate expressions in the **SQL** property of a **QueryDef** object or when creating a **Recordset** object based on an SQL query.</span></span>

- <span data-ttu-id="d8df6-106">[Avg 関数](https://msdn.microsoft.com/library/ff822755\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="d8df6-106">[Avg function](https://msdn.microsoft.com/library/ff822755\(v=office.15\))</span></span>

- <span data-ttu-id="d8df6-107">[Count 関数](https://msdn.microsoft.com/library/ff844748\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="d8df6-107">[Count function](https://msdn.microsoft.com/library/ff844748\(v=office.15\))</span></span>

- <span data-ttu-id="d8df6-108">[First、Last 関数します。](https://msdn.microsoft.com/library/ff197381\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="d8df6-108">[First, Last functions](https://msdn.microsoft.com/library/ff197381\(v=office.15\))</span></span>

- <span data-ttu-id="d8df6-109">[Min、Max 関数](https://msdn.microsoft.com/library/ff194490\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="d8df6-109">[Min, Max functions](https://msdn.microsoft.com/library/ff194490\(v=office.15\))</span></span>

- <span data-ttu-id="d8df6-110">[StDev、StDevP 関数](https://msdn.microsoft.com/library/ff197043\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="d8df6-110">[StDev, StDevP functions](https://msdn.microsoft.com/library/ff197043\(v=office.15\))</span></span>

- <span data-ttu-id="d8df6-111">[Sum 関数](https://msdn.microsoft.com/library/ff844764\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="d8df6-111">[Sum function](https://msdn.microsoft.com/library/ff844764\(v=office.15\))</span></span>

- <span data-ttu-id="d8df6-112">[Var、VarP 関数](https://msdn.microsoft.com/library/ff192105\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="d8df6-112">[Var, VarP functions](https://msdn.microsoft.com/library/ff192105\(v=office.15\))</span></span>

