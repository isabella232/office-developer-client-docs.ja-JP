---
title: SQL 式 (デスクトップ データベース参照のアクセス)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25b7d11430b730b6cedd1d8a084acd4984c5f292
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944151"
---
# <a name="sql-expressions"></a><span data-ttu-id="6da0d-102">SQL 式</span><span class="sxs-lookup"><span data-stu-id="6da0d-102">SQL expressions</span></span>


<span data-ttu-id="6da0d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6da0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6da0d-p101">SQL 式は、SQL ステートメントの一部または全体を構成する文字列です。たとえば、**Recordset** オブジェクトの **FindFirst** メソッドで使用される SQL 式は、[WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) 句の抽出条件で構成されています。</span><span class="sxs-lookup"><span data-stu-id="6da0d-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the**FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://msdn.microsoft.com/library/ff195245\(v=office.15\)).</span></span>

<span data-ttu-id="6da0d-106">Microsoft Access データベース エンジンは、単純な算術演算や関数の評価を実行するのにマイクロソフトの Visual Basic for Applications (VBA) の式のサービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="6da0d-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="6da0d-107">除く**[との間](https://msdn.microsoft.com/library/ff192436\(v=office.15\))** **[](https://msdn.microsoft.com/library/ff836369\(v=office.15\))\*\*\*\*[のような](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) Microsoft Access データベース エンジンの SQL 式で使用される演算子のすべては、VBA の式サービスによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="6da0d-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))**, and **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) are defined by the VBA expression service.</span></span> <span data-ttu-id="6da0d-108">さらに、VBA の式のサービスには、SQL 式で使用できる 100 個以上の VBA 関数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="6da0d-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="6da0d-109">たとえば、これらの VBA 関数を使用して、Microsoft Access クエリのデザイン ビューで、SQL クエリを作成、Microsoft Visual C++、Microsoft Visual Basic、および Microsoft の DAO の**何らか**の方法で SQL クエリでこれらの関数を使用することもできます。Excel コードです。</span><span class="sxs-lookup"><span data-stu-id="6da0d-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

