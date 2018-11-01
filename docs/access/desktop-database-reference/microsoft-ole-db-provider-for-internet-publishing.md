---
title: Microsoft OLE DB Provider for Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bb0bb40d0f12bd9d5a6c8b29af1d4e27d806db87
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882085"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a>Microsoft OLE DB Provider for Internet Publishing

**適用されます**Access 2013、Office 2013。

Microsoft OLE DB Provider for Internet Publishing を使用すると、ADO から、Microsoft FrontPage や Microsoft Internet Information Server が提供するリソースにアクセスできます。このリソースには、HTML ファイルなどの Web ソース ファイルや Windows 2000 の Web フォルダーも含まれます。

## <a name="connection-string-parameters"></a>接続文字列のパラメーター

このプロバイダーに接続するには、*ConnectionString* プロパティの [Provider](connectionstring-property-ado.md) 引数を次のように設定します。

```vb 
 
MSDAIPP.DSO 
```

この値は、[Provider](provider-property-ado.md) プロパティを使用して設定または取得することもできます。

## <a name="typical-connection-string"></a>標準的な接続文字列

このプロバイダーの標準的な接続文字列を次に示します。

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

\-または -

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
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
<td><p>OLE DB Provider for Internet Publishing を指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong> または <strong>URL</strong></p></td>
<td><p>ファイルまたは web フォルダーで公開されているディレクトリの URL を指定します。</p></td>
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


接続文字列の "URL=" の *ResourceURL* の値を無効な値に設定すると、既定では、Internet Publishing Provider により有効な値の入力を促すダイアログ ボックスが表示されます。この動作は、アプリケーションの中間層のコンポーネントでは好ましくありません。ダイアログ ボックスを閉じるまでプログラムの実行が中断され、このコンポーネントから応答がなく、クライアントがフリーズしたように見えるためです。


> [!NOTE]
> <P>場合 MSDAIPP。DSO はプロバイダーの値として明示的に指定されたか、<EM>プロバイダー</EM>の接続文字列キーワードまたは<STRONG>Provider</STRONG>プロパティを使うことはできません"URL ="接続文字列にします。 "URL=" を使用すると、エラーが発生します。 代わりに、「 <A href="the-ole-db-provider-for-internet-publishing.md">OLE DB Provider for Internet Publishing</A>」に示されているように URL のみを指定します。</P>


