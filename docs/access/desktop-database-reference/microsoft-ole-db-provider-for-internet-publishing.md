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
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="9f7b0-102">Microsoft OLE DB Provider for Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="9f7b0-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="9f7b0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f7b0-p101">Microsoft OLE DB Provider for Internet Publishing を使用すると、ADO から、Microsoft FrontPage や Microsoft Internet Information Server が提供するリソースにアクセスできます。このリソースには、HTML ファイルなどの Web ソース ファイルや Windows 2000 の Web フォルダーも含まれます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-p101">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server. Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="9f7b0-106">接続文字列のパラメーター</span><span class="sxs-lookup"><span data-stu-id="9f7b0-106">Connection String Parameters</span></span>

<span data-ttu-id="9f7b0-107">このプロバイダーに接続するには、*ConnectionString* プロパティの [Provider](connectionstring-property-ado.md) 引数を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="9f7b0-108">この値は、[Provider](provider-property-ado.md) プロパティを使用して設定または取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="9f7b0-109">標準的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="9f7b0-109">Typical Connection String</span></span>

<span data-ttu-id="9f7b0-110">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="9f7b0-111">\-または -</span><span class="sxs-lookup"><span data-stu-id="9f7b0-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="9f7b0-112">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f7b0-113">キーワード</span><span class="sxs-lookup"><span data-stu-id="9f7b0-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="9f7b0-114">説明</span><span class="sxs-lookup"><span data-stu-id="9f7b0-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f7b0-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="9f7b0-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="9f7b0-116">OLE DB Provider for Internet Publishing を指定します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f7b0-117"><strong>Data Source</strong> または <strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="9f7b0-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="9f7b0-118">ファイルまたは web フォルダーで公開されているディレクトリの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-118">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f7b0-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="9f7b0-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="9f7b0-120">ユーザー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f7b0-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="9f7b0-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="9f7b0-122">ユーザー パスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9f7b0-p102">接続文字列の "URL=" の *ResourceURL* の値を無効な値に設定すると、既定では、Internet Publishing Provider により有効な値の入力を促すダイアログ ボックスが表示されます。この動作は、アプリケーションの中間層のコンポーネントでは好ましくありません。ダイアログ ボックスを閉じるまでプログラムの実行が中断され、このコンポーネントから応答がなく、クライアントがフリーズしたように見えるためです。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-p102">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value. This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9f7b0-125">場合 MSDAIPP。DSO はプロバイダーの値として明示的に指定されたか、<EM>プロバイダー</EM>の接続文字列キーワードまたは<STRONG>Provider</STRONG>プロパティを使うことはできません"URL ="接続文字列にします。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the <EM>Provider</EM> connection string keyword or the <STRONG>Provider</STRONG> property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="9f7b0-126">"URL=" を使用すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-126">If you do, an error will occur.</span></span> <span data-ttu-id="9f7b0-127">代わりに、「 <A href="the-ole-db-provider-for-internet-publishing.md">OLE DB Provider for Internet Publishing</A>」に示されているように URL のみを指定します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-127">Instead, simply specify the URL as shown in the topic <A href="the-ole-db-provider-for-internet-publishing.md">Using ADO with the OLE DB Provider for Internet Publishing</A>.</span></span></P>


