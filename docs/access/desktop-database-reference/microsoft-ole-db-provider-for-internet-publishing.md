---
title: Microsoft OLE DB Provider for Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 38183cd8306f2425a362bd2650639120a2d16845
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699780"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="de82c-102">Microsoft OLE DB Provider for Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="de82c-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="de82c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="de82c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de82c-p101">Microsoft OLE DB Provider for Internet Publishing を使用すると、ADO から、Microsoft FrontPage や Microsoft Internet Information Server が提供するリソースにアクセスできます。このリソースには、HTML ファイルなどの Web ソース ファイルや Windows 2000 の Web フォルダーも含まれます。</span><span class="sxs-lookup"><span data-stu-id="de82c-p101">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server. Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="de82c-106">接続文字列パラメーター</span><span class="sxs-lookup"><span data-stu-id="de82c-106">Connection string parameters</span></span>

<span data-ttu-id="de82c-107">このプロバイダーに接続するには、*ConnectionString* プロパティの [Provider](connectionstring-property-ado.md) 引数を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="de82c-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="de82c-108">この値は、[Provider](provider-property-ado.md) プロパティを使用して設定または取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="de82c-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="de82c-109">一般的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="de82c-109">Typical connection string</span></span>

<span data-ttu-id="de82c-110">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="de82c-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="de82c-111">\-または -</span><span class="sxs-lookup"><span data-stu-id="de82c-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="de82c-112">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="de82c-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de82c-113">キーワード</span><span class="sxs-lookup"><span data-stu-id="de82c-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="de82c-114">説明</span><span class="sxs-lookup"><span data-stu-id="de82c-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de82c-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="de82c-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="de82c-116">OLE DB Provider for Internet Publishing を指定します。</span><span class="sxs-lookup"><span data-stu-id="de82c-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de82c-117"><strong>Data Source</strong> または <strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="de82c-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="de82c-118">ファイルまたは web フォルダーで公開されているディレクトリの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="de82c-118">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de82c-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="de82c-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="de82c-120">ユーザー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="de82c-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de82c-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="de82c-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="de82c-122">ユーザー パスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="de82c-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="de82c-p102">接続文字列の "URL=" の *ResourceURL* の値を無効な値に設定すると、既定では、Internet Publishing Provider により有効な値の入力を促すダイアログ ボックスが表示されます。この動作は、アプリケーションの中間層のコンポーネントでは好ましくありません。ダイアログ ボックスを閉じるまでプログラムの実行が中断され、このコンポーネントから応答がなく、クライアントがフリーズしたように見えるためです。</span><span class="sxs-lookup"><span data-stu-id="de82c-p102">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value. This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>

> [!NOTE]
> <span data-ttu-id="de82c-125">場合 MSDAIPP。DSO はプロバイダーの値として明示的に指定されたか、*プロバイダー*の接続文字列キーワードまたは**Provider**プロパティを使うことはできません"URL ="接続文字列にします。</span><span class="sxs-lookup"><span data-stu-id="de82c-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="de82c-126">"URL=" を使用すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="de82c-126">If you do, an error will occur.</span></span> <span data-ttu-id="de82c-127">代わりに、「 [OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md)」に示されているように URL のみを指定します。</span><span class="sxs-lookup"><span data-stu-id="de82c-127">Instead, simply specify the URL as shown in the topic [Using ADO with the OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).</span></span>

