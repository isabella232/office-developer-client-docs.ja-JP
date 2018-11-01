---
title: SQL 集計関数 (SQL)
TOCTitle: SQL Aggregate Functions (SQL)
ms:assetid: 8866cd71-0216-25b4-6a6a-02cb7acad9a2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197054(v=office.15)
ms:contentKeyID: 48546136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1fd06b02d4331a51e0f8a186f713d80d98bbed20
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870563"
---
# <a name="sql-aggregate-functions-sql"></a><span data-ttu-id="f5102-102">SQL 集計関数 (SQL)</span><span class="sxs-lookup"><span data-stu-id="f5102-102">SQL Aggregate Functions (SQL)</span></span>


<span data-ttu-id="f5102-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f5102-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5102-p101">SQL 集計関数を使用すると、値の集合からさまざまな統計情報を求めることができます。SQL 集計関数は、 **QueryDef** オブジェクトの **SQL** プロパティのクエリおよび集計式で使用できます。また、SQL クエリに基づく **Recordset** オブジェクトを作成する場合にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="f5102-p101">Using the SQL aggregate functions, you can determine various statistics on sets of values. You can use these functions in a query and aggregate expressions in the **SQL** property of a **QueryDef** object or when creating a **Recordset** object based on an SQL query.</span></span>

<span data-ttu-id="f5102-106">**[Avg 関数](https://msdn.microsoft.com/library/ff822755\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="f5102-106">**[Avg Function](https://msdn.microsoft.com/library/ff822755\(v=office.15\))**</span></span>

<span data-ttu-id="f5102-107">**[Count 関数](https://msdn.microsoft.com/library/ff844748\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="f5102-107">**[Count Function](https://msdn.microsoft.com/library/ff844748\(v=office.15\))**</span></span>

<span data-ttu-id="f5102-108">**[First 関数および Last 関数](https://msdn.microsoft.com/library/ff197381\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="f5102-108">**[First, Last Functions](https://msdn.microsoft.com/library/ff197381\(v=office.15\))**</span></span>

<span data-ttu-id="f5102-109">**[Min 関数および Max 関数](https://msdn.microsoft.com/library/ff194490\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="f5102-109">**[Min, Max Functions](https://msdn.microsoft.com/library/ff194490\(v=office.15\))**</span></span>

<span data-ttu-id="f5102-110">**[StDev 関数および StDevP 関数](https://msdn.microsoft.com/library/ff197043\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="f5102-110">**[StDev, StDevP Functions](https://msdn.microsoft.com/library/ff197043\(v=office.15\))**</span></span>

<span data-ttu-id="f5102-111">**[Sum 関数](https://msdn.microsoft.com/library/ff844764\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="f5102-111">**[Sum Function](https://msdn.microsoft.com/library/ff844764\(v=office.15\))**</span></span>

<span data-ttu-id="f5102-112">**[Var 関数および VarP 関数](https://msdn.microsoft.com/library/ff192105\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="f5102-112">**[Var, VarP Functions](https://msdn.microsoft.com/library/ff192105\(v=office.15\))**</span></span>

