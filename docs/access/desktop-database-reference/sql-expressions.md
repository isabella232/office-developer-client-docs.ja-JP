---
title: SQL 式 (Access デスクトップ データベース リファレンス)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 06/13/2019
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 003462c4a16ca9a9de809f9dd87f661a0242992a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589100"
---
# <a name="sql-expressions"></a>SQL 式

**適用先:** Access 2013、Office 2013

SQL 式は、SQL ステートメントの一部または全体を構成する文字列です。たとえば、 **Recordset** オブジェクトの **FindFirst** メソッドで使用される SQL 式は、 [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句の抽出条件で構成されています。

Microsoft Access データベース エンジンは、Microsoft Visual Basic for Applications (VBA) Expression Service を使用して、単純な算術と関数の評価を実行します。 Microsoft Access データベース エンジン SQL 式で使用されるすべての演算子 (**[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**、**[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**、**[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** を除く) は、VBA Expression Service によって定義されます。 

さらに、VBA Expression Service には、SQL 式で使用できる 100 以上の VBA 関数が用意されています。たとえば、Microsoft Access クエリのデザイン ビューでこれらの VBA 関数を使用して SQL クエリを作成することができます。また、Microsoft Visual C++、Microsoft Visual Basic、Microsoft Excel コードの DAO **OpenRecordset** メソッドの SQL クエリでこれらの関数を使用することもできます。

## <a name="see-also"></a>関連項目

- [Access VBA の概念](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
