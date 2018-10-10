---
title: SQL 式 (デスクトップ データベース参照のアクセス)
TOCTitle: SQL Expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 328804dc8186c082cf22d409b4071368af8873e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476226"
---
# <a name="sql-expressions"></a>SQL 式


**適用されます**Access 2013 |。Office 2013

SQL 式は、SQL ステートメントの一部または全体を構成する文字列です。たとえば、**Recordset** オブジェクトの **FindFirst** メソッドで使用される SQL 式は、[WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) 句の抽出条件で構成されています。

Microsoft Access データベース エンジンでは、VBA (Microsoft® Visual Basic® for Applications) の式作成機能を利用して、簡単な算術評価や関数評価を実行します。**[Between](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**、**[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))**、および **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))** を除く Microsoft Access データベース エンジン SQL で使用される式の演算子は、すべて VBA の式作成機能によって定義されています。また、VBA の式作成機能には、SQL 式の中で使用できる 100 個以上の VBA 関数が用意されています。たとえば、Microsoft Office Access クエリのデザイン ビューで作成する SQL クエリでこれらの VBA 関数を使用できます。同様に、Microsoft Visual C++®、Microsoft Visual Basic、および Microsoft Excel の各コード内の DAO の **OpenRecordset** メソッドで使用する SQL クエリにも、VBA 関数を使用できます。

