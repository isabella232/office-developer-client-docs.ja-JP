---
title: SQL 式 (デスクトップ データベース参照のアクセス)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 5bbe9718bfb18ced5f09d2a9396e1e0829d0d81b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710546"
---
# <a name="sql-expressions"></a>SQL 式

**適用されます**Access 2013、Office 2013。

SQL 式は、SQL ステートメントの一部または全体を構成する文字列です。たとえば、 **Recordset** オブジェクトの **FindFirst** メソッドで使用される SQL 式は、 [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句の抽出条件で構成されています。

Microsoft Access データベース エンジンは、単純な算術演算や関数の評価を実行するのにマイクロソフトの Visual Basic for Applications (VBA) の式のサービスを使用します。 除く**[との間](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)** **[](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)****[のような](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) Microsoft Access データベース エンジンの SQL 式で使用される演算子のすべては、VBA の式サービスによって定義されます。 さらに、VBA の式のサービスには、SQL 式で使用できる 100 個以上の VBA 関数が用意されています。 たとえば、これらの VBA 関数を使用して、Microsoft Access クエリのデザイン ビューで、SQL クエリを作成、Microsoft Visual C++、Microsoft Visual Basic、および Microsoft の DAO の**何らか**の方法で SQL クエリでこれらの関数を使用することもできます。Excel コードです。

## <a name="see-also"></a>関連項目

- [アクセス VBA の概念](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
