---
title: Microsoft OLE DB Provider for Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6f1c7c65d0ac1dd2a6d3ea132a31955f175bc7f
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997484"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a>Microsoft OLE DB Provider for Internet Publishing

**適用されます**Access 2013、Office 2013。

Microsoft OLE DB Provider for Internet Publishing を使用すると、ADO から、Microsoft FrontPage や Microsoft Internet Information Server が提供するリソースにアクセスできます。このリソースには、HTML ファイルなどの Web ソース ファイルや Windows 2000 の Web フォルダーも含まれます。

## <a name="connection-string-parameters"></a>接続文字列パラメーター

このプロバイダーに接続するには、*ConnectionString* プロパティの [Provider](connectionstring-property-ado.md) 引数を次のように設定します。

```vb 
 
MSDAIPP.DSO 
```

この値は、[Provider](provider-property-ado.md) プロパティを使用して設定または取得することもできます。

## <a name="typical-connection-string"></a>一般的な接続文字列

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
> 場合 MSDAIPP。DSO はプロバイダーの値として明示的に指定されたか、*プロバイダー*の接続文字列キーワードまたは**Provider**プロパティを使うことはできません"URL ="接続文字列にします。 "URL=" を使用すると、エラーが発生します。 代わりに、「 [OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md)」に示されているように URL のみを指定します。

