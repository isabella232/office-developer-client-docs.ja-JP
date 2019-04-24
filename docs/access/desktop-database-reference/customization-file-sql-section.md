---
title: カスタマイズ ファイルの SQL セクション
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ae259589cc8d4945068901c59105425599edc64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295136"
---
# <a name="customization-file-sql-section"></a>カスタマイズ ファイルの SQL セクション


**適用先:** Access 2013、Office 2013

**sql** セクションには、クライアントのコマンド文字列を置き換える新規 SQL 文字列を含めることができます。このセクションに SQL 文字列がない場合、このセクションは無視されます。

新しい SQL 文字列を*パラメーター化*することができます。 つまり、 **sql**セクションの sql 文字列 (' ? ' 文字で示される) のパラメーターは、クライアントのコマンド文字列 (かっこで囲まれたコンマ区切りのリストで指定されています) の*識別子*で、対応する引数によって置き換えられます。 The identifier and argument list behave like a function call.

たとえば、クライアントのコマンド文字列が "CustomerByID (4)" で、sql セクションヘッダーが\[sql CustomerByID\]で、新しい SQL セクション文字列が "CustomerID = ? の\*顧客から選択" であるとします。 ハンドラーが生成するので、sql セクションヘッダー \[は sql\] CustomerByID で、新しい sql セクション文字列は "CustomerID \* : 得意先から選択してください = ?" です。 ハンドラーは、[CustomerID = \* 4 の顧客から選択] を生成し、その文字列を使用してデータソースに対してクエリを実行します。

新規 SQL ステートメントが Null 文字列 ("") の場合、このセクションは無視されます。

新規 SQL ステートメント文字列が有効なステートメントでない場合、ステートメントの実行は失敗します。また、クライアント パラメーターは無視されます。このことを利用して、すべてのクライアント SQL コマンドを意図的に "無効" にするために次のような指定を行うことができます。

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a>構文

置き換える SQL 文字列エントリの形式は、次のとおりです。

**SQL = * sqlString***

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パーツ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>SQL</strong></p></td>
<td><p>これが SQL セクション エントリであることを示すリテラル文字列。</p></td>
</tr>
<tr class="even">
<td><p><strong><em>sqlString</em></strong></p></td>
<td><p>クライアント文字列を置き換える SQL 文字列。</p></td>
</tr>
</tbody>
</table>

