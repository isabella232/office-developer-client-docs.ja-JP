---
title: カスタマイズ ファイルの SQL セクション
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 629c7a5601f35253f034bb9b488aef3c8a369fc5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622481"
---
# <a name="customization-file-sql-section"></a>カスタマイズ ファイルの SQL セクション


**適用先**: Access 2013、Office 2013

**sql** セクションには、クライアントのコマンド文字列を置き換える新規 SQL 文字列を含めることができます。このセクションに SQL 文字列がない場合、このセクションは無視されます。

新しい文字列SQLパラメーター化 *できます*。 つまり **、sql** セクション SQL 文字列 ('?' 文字で指定される) のパラメーターは、クライアント コマンド文字列の識別子内の対応する引数 (かっこ内のコンマ区切りリストで指定) に置き換える可能性があります。 The identifier and argument list behave like a function call.

たとえば、クライアント コマンド文字列が "CustomerByID(4)" で、SQL セクション ヘッダーが SQL CustomerByID であり、新しい SQL セクション文字列が "SELECT \[ \] FROM Customers WHERE \* CustomerID = ?"" と仮定します。 ハンドラーは生成され、SQL セクション ヘッダーは CustomerByID SQL で、新しい SQL セクション文字列は \[ \] "SELECT \* FROM Customers WHERE CustomerID = ?" です。 ハンドラーは"SELECT FROM Customers WHERE CustomerID = 4" を生成し、その文字列を使用してデータ \* ソースにクエリを実行します。

新規 SQL ステートメントが Null 文字列 ("") の場合、このセクションは無視されます。

新規 SQL ステートメント文字列が有効なステートメントでない場合、ステートメントの実行は失敗します。また、クライアント パラメーターは無視されます。このことを利用して、すべてのクライアント SQL コマンドを意図的に "無効" にするために次のような指定を行うことができます。

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a>構文

置き換える SQL 文字列エントリの形式は、次のとおりです。

**SQL=*sqlString***

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

