---
title: ConnectionString プロパティ (ADO)
TOCTitle: ConnectionString Property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90e884f821c3ca7667020ffe041b4e064555c02b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478800"
---
# <a name="connectionstring-property-ado"></a>ConnectionString プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

データ ソースとの接続を確立するために使用される情報を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

文字列型 ( **String** ) の値を設定または取得します。

## <a name="remarks"></a>解説

**ConnectionString**プロパティを使用すると、一連のセミコロンで区切られた*引数**の値を =* ステートメントを含む詳細な接続文字列を渡すことによってデータ ソースを指定します。

ADO では、 **ConnectionString** プロパティに対して 5 種類の引数がサポートされます。その他の引数は ADO で処理されずに直接プロバイダーに渡されます。ADO でサポートされる引数を次に示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Provider=</em></p></td>
<td><p>接続に使用するプロバイダーの名前を指定します。</p></td>
</tr>
<tr class="even">
<td><p><em>ファイル名 =</em></p></td>
<td><p>設定済みの接続情報を格納したプロバイダー固有のファイル (たとえば、持続的なデータ ソース オブジェクト) の名前を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><em>リモート プロバイダー =</em></p></td>
<td><p>クライアント側の接続を開くときに使用するプロバイダーの名前を指定します (Remote Data Service のみ)。</p></td>
</tr>
<tr class="even">
<td><p><em>リモート サーバー =</em></p></td>
<td><p>クライアント側の接続を開くときに使用するサーバーのパス名を指定します (リモート データ サービスのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><em>URL=</em></p></td>
<td><p>接続文字列を、ファイルやディレクトリなどのリソースを識別する絶対 URL として指定します。</p></td>
</tr>
</tbody>
</table>


**ConnectionString** プロパティを設定して [Connection](connection-object-ado.md) オブジェクトを開いた後、ADO によって定義された引数名がプロバイダーの対応する引数名にマップされるなど、プロバイダーによってプロパティの内容が変更される場合があります。

**ConnectionString**プロパティは、 **Open**メソッドの呼び出し中に、現在の**接続文字列**プロパティをオーバーライドするために、 [Open](open-method-ado-connection.md)メソッドの*ConnectionString*引数に対して使用する値を自動的に継承します。

*ファイル名*引数には、関連付けられているプロバイダーをロードするのには ADO が発生するため、*プロバイダー*と*ファイル名*の両方の引数を渡すことはできません。

**ConnectionString** プロパティは、接続が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。

**ConnectionString** プロパティにおいて重複している引数は無視されます。引数の最後のインスタンスが使用されます。

**リモート データ サービスの使用法**使用すると、クライアント側の**Connection**オブジェクトの**ConnectionString**プロパティは*リモート プロバイダー*と*リモート サーバー*のパラメーターのみを含めることができます。

