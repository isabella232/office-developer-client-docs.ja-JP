---
title: SQL 式 (Access デスクトップ データベース リファレンス)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 06/13/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f38932ed4744e5479c523446f9ab77065f4eb203
ms.sourcegitcommit: d0e1ce095a478d90411abb8c147eb9efe19ffa5f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "34870865"
---
# <a name="sql-expressions"></a><span data-ttu-id="0d791-102">SQL 式</span><span class="sxs-lookup"><span data-stu-id="0d791-102">SQL expressions</span></span>

<span data-ttu-id="0d791-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d791-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d791-p101">SQL 式は、SQL ステートメントの一部または全体を構成する文字列です。たとえば、 **Recordset** オブジェクトの **FindFirst** メソッドで使用される SQL 式は、 [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句の抽出条件で構成されています。</span><span class="sxs-lookup"><span data-stu-id="0d791-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="0d791-106">Microsoft Access データベース エンジンは、Microsoft Visual Basic for Applications (VBA) Expression Service を使用して、単純な算術と関数の評価を実行します。</span><span class="sxs-lookup"><span data-stu-id="0d791-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="0d791-107">Microsoft Access データベース エンジン SQL 式で使用されるすべての演算子 (**[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**、**[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**、**[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** を除く) は、VBA Expression Service によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="0d791-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> 

<span data-ttu-id="0d791-108">さらに、VBA Expression Service には、SQL 式で使用できる 100 を超える VBA 関数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="0d791-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="0d791-109">たとえば、Microsoft Access クエリのデザイン ビューでこれらの VBA 関数を使用して SQL クエリを作成することができます。また、Microsoft Visual C++、Microsoft Visual Basic、Microsoft Excel コードの DAO **OpenRecordset** メソッドの SQL クエリでこれらの関数を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="0d791-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d791-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d791-110">See also</span></span>

- [<span data-ttu-id="0d791-111">Access VBA の概念</span><span class="sxs-lookup"><span data-stu-id="0d791-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
