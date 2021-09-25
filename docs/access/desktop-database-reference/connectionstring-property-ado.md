---
title: ConnectionString プロパティ (ADO)
TOCTitle: ConnectionString property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9c78651cc6a706fdf3fecc43258d39baea13bb3d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615747"
---
# <a name="connectionstring-property-ado"></a>ConnectionString プロパティ (ADO)


**適用先**: Access 2013、Office 2013

データ ソースとの接続を確立するために使用される情報を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

文字列型 (**String**) の値を設定または取得します。

## <a name="remarks"></a>注釈

**ConnectionString プロパティを使用** して、一連の引数 *= セミコロン* で区切られた value ステートメントを含む詳細な接続文字列を渡して、データ ソースを指定します。

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
<td><p><em>File Name=</em></p></td>
<td><p>設定済みの接続情報を格納したプロバイダー固有のファイル (たとえば、持続的なデータ ソース オブジェクト) の名前を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><em>Remote Provider=</em></p></td>
<td><p>クライアント側の接続を開くときに使用するプロバイダーの名前を指定します (Remote Data Service のみ)。</p></td>
</tr>
<tr class="even">
<td><p><em>Remote Server=</em></p></td>
<td><p>クライアント側の接続を開くときに使用するサーバーのパス名を指定します (リモート データ サービスのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><em>URL=</em></p></td>
<td><p>接続文字列を、ファイルやディレクトリなどのリソースを識別する絶対 URL として指定します。</p></td>
</tr>
</tbody>
</table>


**ConnectionString** プロパティを設定して [Connection](connection-object-ado.md) オブジェクトを開いた後、ADO によって定義された引数名がプロバイダーの対応する引数名にマップされるなど、プロバイダーによってプロパティの内容が変更される場合があります。

**ConnectionString** プロパティは、[Open](open-method-ado-connection.md) メソッドの *ConnectionString* 引数に使用された値を自動的に継承します。したがって、**Open** メソッドの呼び出し中に現在の **ConnectionString** プロパティを上書きできます。

*File Name* 引数により関連のあるプロバイダーが呼び出されるため、*Provider* 引数と *File Name* 引数の両方を渡すことはできません。

**ConnectionString** プロパティは、接続が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。

**ConnectionString** プロパティにおいて重複している引数は無視されます。引数の最後のインスタンスが使用されます。

**リモート データ サービスの使用状況** クライアント側の Connection オブジェクトで **使用する場合、ConnectionString** プロパティには、リモート プロバイダーパラメーターとリモート サーバー パラメーター *のみを含* めできます。 

