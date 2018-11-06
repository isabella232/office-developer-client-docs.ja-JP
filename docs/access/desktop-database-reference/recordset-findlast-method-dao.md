---
title: Recordset.FindLast メソッド (DAO)
TOCTitle: FindLast Method
ms:assetid: 65236519-3474-a760-99bc-2e8f6bfeee7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195128(v=office.15)
ms:contentKeyID: 48545311
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d7b80444005a780e2f26c03229d0a66d66ce69eb
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996770"
---
# <a name="recordsetfindlast-method-dao"></a>Recordset.FindLast メソッド (DAO)

**適用されます**Access 2013、Office 2013。

ダイナセット タイプまたはスナップショット タイプの **[Recordset](recordset-object-dao.md)** オブジェクトで、指定された条件を満たす最後のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。FindLast (***条件***)

*式***レコード セット**オブジェクトを表す変数です。

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
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Criteria</em></p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>レコードの検索に使用する文字列です。SQL ステートメントの WHERE 句に似ていますが、WHERE という語は付けません。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

特定の条件を満たすレコードだけでなく、すべてのレコードを検索対象とする場合は、 **Move** メソッドを使用してレコード間を移動します。テーブル タイプの **Recordset** でレコードを検索するには、 **Seek** メソッドを使用します。

条件を満たすレコードが検出されない場合、カレント レコードを参照するポインターは不明となり、 **NoMatch** プロパティが **True** に設定されます。recordset に条件を満たすレコードが複数含まれている場合の検出対象は、 **FindFirst** では最初に出現したもの、 **FindNext** では次に出現したもの、などとなります。

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
<td><p>カレント レコード</p></td>
<td><p>レコードセットの末尾</p></td>
</tr>
<tr class="even">
<td><p><strong>FindPrevious</strong></p></td>
<td><p>カレント レコード</p></td>
<td><p>レコードセットの先頭</p></td>
</tr>
</tbody>
</table>


**Recordset** の末尾までデータが格納されていない状態で **FindLast** メソッドを使用すると、検索が始まる前に、Microsoft Access データベース エンジンによってレコードセットが末尾まで埋められます。

ただし、いずれかの **Find** メソッドを使用した場合と、 **Move** メソッドを使用した場合の結果は同じではありません。後者は、条件を指定せずに、最初のレコード、最後のレコード、次のレコード、または前のレコードをカレント レコードにするだけです。Find 操作の後に Move 操作を使用する場合もあります。

**NoMatch** プロパティの値を必ず確認して、Find 操作が成功したかどうか調べてください。検索が成功した場合、 **NoMatch** は **False** です。失敗した場合、 **NoMatch** は **True** で、カレント レコードは未定義となります。この場合は、カレント レコードを参照するポインターを有効なレコードに戻す必要があります。

**Find** メソッドを Microsoft Access データベース エンジンに接続された ODBC アクセスのレコードセットで使用すると、効率が悪い場合があります。特に大きなレコードセットを操作するときは、criteria の表現を変更すると、より迅速に特定のレコードを検出できる場合があります。

Microsoft Access データベース エンジンに接続している ODBC データベースでダイナセット タイプの大きな **Recordset** オブジェクトを操作している場合、 **Find** メソッド、 **Sort** プロパティ、または **Filter** プロパティを使用すると、処理速度が遅いことがあります。パフォーマンスを向上するには、カスタマイズした ORDER BY 句または WHERE 句のある SQL クエリ、パラメーター クエリ、またはインデックスが作成されている特定のレコードを取得する **QueryDef** オブジェクトを使用します。

日付を含むフィールドを検索するときは、米国バージョンの Microsoft Access データベース エンジンを使用していない場合でも、米国の日付形式 (month-day-year) を使用する必要があります。それ以外の日付形式を使用すると、データが検出されない場合があります。日付を変換するには、Visual Basic の **Format** 関数を使用します。次に例を示します。

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

基準は、整数以外の値に連結された文字列の作成し、システムのパラメーターは、米国以外の小数点の記号、カンマなどを指定する場合 (たとえば、strSQL ="価格\>"& lngPrice でと lngPrice = 125,50) をしようとするときにエラーが発生しました。メソッドを呼び出します。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみであるためです。

> [!NOTE]
> - 最高のパフォーマンスを*基準*する必要がありますいずれかの方法でフォーム"*フィールド* = *値*"*フィールド*が、インデックス付きのフィールド内にある基になるベース テーブル、または「*フィールド**のプレフィックス*と同じように」*フィールド*がある、*プレフィックス*と基になるベース テーブルでインデックス付きのフィールドは、プレフィックス検索文字列 (たとえば、「アート *」) です。
> - 一般に、同じような検索を行う場合は、 **Find** メソッドよりも **Seek** メソッドを使用する方がパフォーマンスが優れています。ただし、これを使用できるのは、テーブル タイプの **Recordset** オブジェクトだけを検索対象とする場合です。


