---
title: カスタマイズ ファイルの SQL セクション
TOCTitle: Customization File SQL Section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 391d87d23f50fb2b25e5fb8033da95f44eeeb09c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868617"
---
# <a name="customization-file-sql-section"></a>カスタマイズ ファイルの SQL セクション


**適用されます**Access 2013、Office 2013。

**sql** セクションには、クライアントのコマンド文字列を置き換える新規 SQL 文字列を含めることができます。このセクションに SQL 文字列がない場合、このセクションは無視されます。

新規 SQL 文字列は、*パラメーター化された*可能性があります。 つまり、(かっこで囲まれたコンマ区切りのリストで指定)、クライアントのコマンド文字列の*識別子*に対応する引数 ('?' の文字で指定)、 **sql**セクションの SQL 文字列内のパラメーターを置き換えることができます。 識別子と引数のリストは、関数呼び出しと同じように動作します。

たとえば、SQL セクション ヘッダーは、クライアントのコマンド文字列は、"CustomerByID(4)"を\[SQL CustomerByID\] 、新しい SQL セクションの文字列で、"を選択\*お客様の場所を [得意先コード] から = の ?」です。 ハンドラーを生成しますが、SQL セクション ヘッダーは、 \[SQL CustomerByID\] 、新しい SQL セクションの文字列で、"を選択\*お客様の場所を [得意先コード] から = の ?」です。 ハンドラーが生成されます"を選択\*お客様の場所を [得意先コード] から = の 4」と、その文字列を使用して、データ ソースのクエリを実行するのには。

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

