---
title: SQL 式 (デスクトップ データベース参照のアクセス)
TOCTitle: SQL Expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92ad643c2a602a24a411db33def62af89520f9b7
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937779"
---
# <a name="sql-expressions"></a>SQL 式


**適用されます**Access 2013、Office 2013。

SQL 式は、SQL ステートメントの一部または全体を構成する文字列です。たとえば、**Recordset** オブジェクトの **FindFirst** メソッドで使用される SQL 式は、[WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) 句の抽出条件で構成されています。

Microsoft Access データベース エンジンは、単純な算術演算や関数の評価を実行するのにマイクロソフトの Visual Basic for Applications (VBA) の式のサービスを使用します。 除く**[との間](https://msdn.microsoft.com/library/ff192436\(v=office.15\))** **[](https://msdn.microsoft.com/library/ff836369\(v=office.15\))****[のような](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) Microsoft Access データベース エンジンの SQL 式で使用される演算子のすべては、VBA の式サービスによって定義されます。 さらに、VBA の式のサービスには、SQL 式で使用できる 100 個以上の VBA 関数が用意されています。 たとえば、これらの VBA 関数を使用して、Microsoft Access クエリのデザイン ビューで、SQL クエリを作成、Microsoft Visual C++、Microsoft Visual Basic、および Microsoft の DAO の**何らか**の方法で SQL クエリでこれらの関数を使用することもできます。Excel コードです。

