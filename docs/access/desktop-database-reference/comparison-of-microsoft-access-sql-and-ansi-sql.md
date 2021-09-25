---
title: Microsoft Access SQL と ANSI SQL の比較
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 06/13/2019
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 798e424f1ae7138d15b2bc7db26b17dfebc86d03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569378"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a>Microsoft Access SQL と ANSI SQL の比較

**適用先:** Access 2013、Office 2013

Microsoft Access データベース エンジン SQL は、ANSI 文字セット 89 レベル 1 の仕様にほぼ準拠しています。 ただし、特定の ANSI SQL機能は、Microsoft Access アプリケーションではSQL。 その一方で、ANSI SQL ではサポートされていない予約語や機能が実装されています。

## <a name="major-differences"></a>主な違い

- Microsoft Office Access SQL と ANSI SQL とでは、異なる予約語およびデータ型があります。詳細については、「[SQL 予約語](sql-reserved-words.md)」および「[Microsoft Jet データベース エンジン SQL と ANSI SQL のデータ型](equivalent-ansi-sql-data-types.md)」を参照してください。Microsoft Office Access Database Engine OLE DB Provider と組み合わせて使うと、追加の予約語を使用できます。

- **[Between...And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**
    
  *expr1* \[NOT \] **between** *value1* **and** *value2*
    
  Microsoft Access SQL では、引数 *value1* に引数 *value2* より大きい値を指定できますが、ANSI SQL では引数 *value1* は必ず引数 *value2* 以下の値である必要があります。

- Microsoft Office Access SQL では、ANSI SQL の [ワイルドカード文字](using-wildcard-characters-in-string-comparisons.md)と、 **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** 演算子の指定項目の中で使われる Microsoft Office Access データベース エンジンに固有のワイルドカード文字の両方がサポートされています。ANSI SQL のワイルドカード文字と Microsoft Office Access データベース エンジンに固有のワイルドカード文字は互いに排他的です。このため、これらを同時に使用することはできず、どちらか一方を使用する必要があります。ANSI SQL のワイルドカード文字を使用できるのは、Microsoft Office Access データベース エンジンと Microsoft Office Access Database Engine OLE DB Provider を組み合わせて使う場合だけです。Microsoft Office Access または DAO を介して ANSI SQL のワイルドカード文字を使うと、リテラルとして解釈されます。Microsoft Office Access Database Engine OLE DB Provider を使用しているときは、Microsoft Office Access データベース エンジンのワイルドカード文字がリテラルとして解釈されます。
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>一致する文字</p></th>
    <th><p>Microsoft Access SQL</p></th>
    <th><p>ANSI SQL</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>任意の 1 文字</p></td>
    <td><p>?</p></td>
    <td><p>_ (アンダースコア)</p></td>
    </tr>
    <tr class="even">
    <td><p>0 文字以上の文字列</p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


- 一般的に、Microsoft Access SQL の方が ANSI SQL よりも制限がありません。たとえば、式のグループ化や並べ替えが可能です。

- Microsoft Access SQL では、ANSI SQL よりも強力な式がサポートされています。

## <a name="enhanced-features-of-microsoft-access-sql"></a>Microsoft Access サービスの拡張SQL

Microsoft Access SQL には、次の拡張機能があります。

- クロス集計クエリをサポートする [TRANSFORM](transform-statement-microsoft-access-sql.md) ステートメント。

- [StDev](sql-aggregate-functions-sql.md) や **VarP** などの **集計関数**。

- パラメーター クエリの定義に使用する [PARAMETERS](parameters-declaration-microsoft-access-sql.md) 宣言。

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a>Microsoft Access SQLでサポートされていない ANSI の機能SQL

Microsoft Access SQL では、ANSI SQL の次の機能がサポートされていません。

- DISTINCT 集計関数の参照。たとえば、Microsoft Access SQL では、SUM(DISTINCT *columnname*) のような DISTINCT 集計関数の参照がサポートされていません。

- クエリが返す行数を制限する LIMIT TO *nn* ROWS 句。クエリの適用範囲を制限するために使用できるのは、[WHERE 句](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql)のみです。

