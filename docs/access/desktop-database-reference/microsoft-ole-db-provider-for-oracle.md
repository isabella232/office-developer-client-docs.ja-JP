---
title: Microsoft OLE DB Provider for Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 258fbb5ef1810951788e0dc81dd00386064efc0a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622166"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a>Microsoft OLE DB Provider for Oracle

**適用先**: Access 2013、Office 2013

Microsoft OLE DB Provider for Oracle を使用すると、ADO から Oracle データベースにアクセスできます。

## <a name="connection-string-parameters"></a>接続文字列のパラメーター

このプロバイダーに接続するには、[ConnectionString](connectionstring-property-ado.md) プロパティの *Provider* 引数を次のように設定します。

```vb 
 
MSDAORA 
```

[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。

キーセットまたは動的カーソル による結合クエリを Oracle データベースで実行すると、エラーが発生します。Oracle では、読み取り専用の静的カーソルのみがサポートされています。

## <a name="typical-connection-string"></a>標準的な接続文字列

このプロバイダーの標準的な接続文字列を次に示します。

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
```

この文字列は、次に示すキーワードで構成されています。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>キーワード</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>OLE DB Provider for Oracle を指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong></p></td>
<td><p>サーバー名を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>User ID</strong></p></td>
<td><p>ユーザー名を指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>ユーザー パスワードを指定します。</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>プロバイダー固有の接続パラメーター

このプロバイダーは、ADO で定義されたパラメーターに加えて、プロバイダー固有の接続パラメーターをサポートしています。ADO の接続パラメーターと同様に、これらのプロバイダー固有のプロパティは [Connection](properties-collection-ado.md) の [Properties](connection-object-ado.md) コレクションで設定することも、 **ConnectionString** の一部として設定することもできます。

これらのパラメーターの詳細については、「OLE DB プログラマ リファレンス」を参照してください。「[ADO の動的プロパティ インデックス](ado-dynamic-property-index.md)」では、これらのパラメーターと対応する OLE DB プロパティを相互に参照できます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パラメーター</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Window Handle</strong></p></td>
<td><p>追加情報の入力を求めるために使用するウィンドウ ハンドルを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Locale Identifier</strong></p></td>
<td><p>ユーザーの言語に関する設定を指定する一意の 32 ビット番号 (1033 など) を示します。これらの設定は、日付と時刻の形式、アルファベット順の並べ替え方法、文字列の比較方法などを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>OLE DB Services</strong></p></td>
<td><p>OLE DB サービスを有効にするか無効にするかを指定するビットマスクを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Prompt</strong></p></td>
<td><p>接続の確立中にユーザーに入力を求めるかどうかを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Extended Properties</strong></p></td>
<td><p>プロバイダー固有の拡張接続情報を含む文字列です。通常のプロパティでは記述できないプロバイダー固有の接続情報についてのみ、このプロパティを使用します。</p></td>
</tr>
</tbody>
</table>

