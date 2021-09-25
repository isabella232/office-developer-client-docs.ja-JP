---
title: Recordset2.FindPrevious メソッド (DAO)
TOCTitle: FindPrevious Method
ms:assetid: ec35faf4-20f2-a83f-54e4-ac1f66c3c2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836294(v=office.15)
ms:contentKeyID: 48548509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 337a410a3e2f1d493d98f1b17d3338e6c8cc927b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557996"
---
# <a name="recordset2findprevious-method-dao"></a>Recordset2.FindPrevious メソッド (DAO)

**適用先:** Access 2013、Office 2013

ダイナセット タイプまたはスナップショット タイプの **[Recordset](recordset-object-dao.md)** オブジェクトで、指定された条件を満たす前のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .FindPrevious(***Criteria***)

*式* Recordset2 オブジェクトを **表す変数** 。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>基準</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>レコードの検索に使用する文字列です。SQL ステートメントの WHERE 句に似ていますが、WHERE という語は付けません。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

特定の条件を満たすレコードだけでなく、すべてのレコードを検索対象とする場合は、**Move** メソッドを使用してレコード間を移動します。テーブル タイプの **Recordset** でレコードを検索するには、**Seek** メソッドを使用します。

条件を満たすレコードが検出されない場合、カレント レコードを参照するポインターは不明となり、**NoMatch** プロパティが **True** に設定されます。recordset に条件を満たすレコードが複数含まれている場合の検出対象は、**FindFirst** では最初に出現したもの、**FindNext** では次に出現したもの、などとなります。

次の表に、各 **Find** メソッドの検索開始位置と検索方向を示します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Find メソッド</p></th>
<th><p>検索開始位置</p></th>
<th><p>検索方向</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>FindFirst</strong></p></td>
<td><p>レコードセットの先頭</p></td>
<td><p>レコードセットの末尾</p></td>
</tr>
<tr class="even">
<td><p><strong>FindLast</strong></p></td>
<td><p>レコードセットの末尾</p></td>
<td><p>レコードセットの先頭</p></td>
</tr>
<tr class="odd">
<td><p><strong>FindNext</strong></p></td>
<td><p>現在のレコード</p></td>
<td><p>レコードセットの末尾</p></td>
</tr>
<tr class="even">
<td><p><strong>FindPrevious</strong></p></td>
<td><p>カレント レコード</p></td>
<td><p>レコードセットの先頭</p></td>
</tr>
</tbody>
</table>


ただし、いずれかの **Find** メソッドを使用した場合と、 **Move** メソッドを使用した場合の結果は同じではありません。後者は、条件を指定せずに、最初のレコード、最後のレコード、次のレコード、または前のレコードをカレント レコードにするだけです。Find 操作の後に Move 操作を使用する場合もあります。

**NoMatch** プロパティの値を必ず確認して、Find 操作が成功したかどうか調べてください。検索が成功した場合、 **NoMatch** は **False** です。失敗した場合、 **NoMatch** は **True** で、カレント レコードは未定義となります。この場合は、カレント レコードを参照するポインターを有効なレコードに戻す必要があります。


            **Find** メソッドを Microsoft Access データベース エンジンに接続された ODBC アクセスのレコードセットで使用すると、効率が悪い場合があります。特に大きなレコードセットを操作するときは、criteria の表現を変更すると、より迅速に特定のレコードを検出できる場合があります。

Microsoft Access データベース エンジンに接続している ODBC データベースでダイナセット タイプの大きな **Recordset** オブジェクトを操作している場合、 **Find** メソッド、 **Sort** プロパティ、または **Filter** プロパティを使用すると、処理速度が遅いことがあります。パフォーマンスを向上するには、カスタマイズした ORDER BY 句または WHERE 句のある SQL クエリ、パラメーター クエリ、またはインデックスが作成されている特定のレコードを取得する **QueryDef** オブジェクトを使用します。

日本語版の Microsoft Access データベース エンジンを使用する場合であっても、日付が格納されたフィールドを検索するときは米国の日付形式 (month-day-year) を使用することが推奨され、使用しないとデータが検出されないことがあります。Visual Basic の **Format** 関数を使用して、日付を変換してください。次に例を示します。

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

抽出条件が文字列と非整数値を連結したもので構成され、かつシステム パラメーターでコンマなどのピリオド以外の小数点の記号が使用されている場合 (たとえば、strSQL = "PRICE \> " & lngPrice と lngPrice = 125,50)、メソッドを呼び出そうとするとエラーが発生します。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。

> [!NOTE]
> - 最適なパフォーマンスを得る場合、条件 *** は"フィールド値" という形式で指定する必要があります。フィールドは基になる基本テーブルのインデックス付きフィールド、フィールドは基になる基本テーブルのインデックス付きフィールドで、プレフィックスはプレフィックス検索文字列  =  ("ART*"など) です。
> - 一般に、同じような検索を行う場合は、**Find** メソッドよりも **Seek** メソッドを使用する方がパフォーマンスが優れています。ただし、これを使用できるのは、テーブル タイプの **Recordset** オブジェクトだけを検索対象とする場合です。


