---
title: SQL 式 (デスクトップ データベース参照のアクセス)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a8d340f008fd198068d6dacc1b2bf847838ede1
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025736"
---
# <a name="sql-expressions"></a><span data-ttu-id="f8a8e-102">SQL 式</span><span class="sxs-lookup"><span data-stu-id="f8a8e-102">SQL expressions</span></span>

<span data-ttu-id="f8a8e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f8a8e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8a8e-p101">SQL 式は、SQL ステートメントの一部または全体を構成する文字列です。たとえば、 **Recordset** オブジェクトの **FindFirst** メソッドで使用される SQL 式は、 [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句の抽出条件で構成されています。</span><span class="sxs-lookup"><span data-stu-id="f8a8e-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="f8a8e-106">Microsoft Access データベース エンジンは、単純な算術演算や関数の評価を実行するのにマイクロソフトの Visual Basic for Applications (VBA) の式のサービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="f8a8e-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="f8a8e-107">除く**[との間](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)** **[](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)\*\*\*\*[のような](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) Microsoft Access データベース エンジンの SQL 式で使用される演算子のすべては、VBA の式サービスによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="f8a8e-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> <span data-ttu-id="f8a8e-108">さらに、VBA の式のサービスには、SQL 式で使用できる 100 個以上の VBA 関数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="f8a8e-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="f8a8e-109">たとえば、これらの VBA 関数を使用して、Microsoft Access クエリのデザイン ビューで、SQL クエリを作成、Microsoft Visual C++、Microsoft Visual Basic、および Microsoft の DAO の**何らか**の方法で SQL クエリでこれらの関数を使用することもできます。Excel コードです。</span><span class="sxs-lookup"><span data-stu-id="f8a8e-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8a8e-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8a8e-110">See also</span></span>

- [<span data-ttu-id="f8a8e-111">アクセス VBA の概念</span><span class="sxs-lookup"><span data-stu-id="f8a8e-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)