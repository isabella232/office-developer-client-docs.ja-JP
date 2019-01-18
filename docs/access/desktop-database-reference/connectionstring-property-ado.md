---
title: ConnectionString プロパティ (ADO)
TOCTitle: ConnectionString property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3612652f3473c0794dbfe9be60f84ea2e3fee252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712730"
---
# <a name="connectionstring-property-ado"></a><span data-ttu-id="18215-102">ConnectionString プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="18215-102">ConnectionString property (ADO)</span></span>


<span data-ttu-id="18215-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="18215-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18215-104">データ ソースとの接続を確立するために使用される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="18215-104">Indicates the information used to establish a connection to a data source.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="18215-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="18215-105">Settings and return values</span></span>

<span data-ttu-id="18215-106">文字列型 ( **String** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="18215-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18215-107">解説</span><span class="sxs-lookup"><span data-stu-id="18215-107">Remarks</span></span>

<span data-ttu-id="18215-108">**ConnectionString**プロパティを使用すると、一連のセミコロンで区切られた*引数\*\*の値を =* ステートメントを含む詳細な接続文字列を渡すことによってデータ ソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="18215-108">Use the **ConnectionString** property to specify a data source by passing a detailed connection string containing a series of *argument* *= value* statements separated by semicolons.</span></span>

<span data-ttu-id="18215-p101">ADO では、 **ConnectionString** プロパティに対して 5 種類の引数がサポートされます。その他の引数は ADO で処理されずに直接プロバイダーに渡されます。ADO でサポートされる引数を次に示します。</span><span class="sxs-lookup"><span data-stu-id="18215-p101">ADO supports five arguments for the **ConnectionString** property; any other arguments pass directly to the provider without any processing by ADO. The arguments ADO supports are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18215-111">引数</span><span class="sxs-lookup"><span data-stu-id="18215-111">Argument</span></span></p></th>
<th><p><span data-ttu-id="18215-112">説明</span><span class="sxs-lookup"><span data-stu-id="18215-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18215-113"><em>Provider=</em></span><span class="sxs-lookup"><span data-stu-id="18215-113"><em>Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="18215-114">接続に使用するプロバイダーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="18215-114">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18215-115"><em>ファイル名 =</em></span><span class="sxs-lookup"><span data-stu-id="18215-115"><em>File Name=</em></span></span></p></td>
<td><p><span data-ttu-id="18215-116">設定済みの接続情報を格納したプロバイダー固有のファイル (たとえば、持続的なデータ ソース オブジェクト) の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="18215-116">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18215-117"><em>リモート プロバイダー =</em></span><span class="sxs-lookup"><span data-stu-id="18215-117"><em>Remote Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="18215-p102">クライアント側の接続を開くときに使用するプロバイダーの名前を指定します (Remote Data Service のみ)。</span><span class="sxs-lookup"><span data-stu-id="18215-p102">Specifies the name of a provider to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18215-120"><em>リモート サーバー =</em></span><span class="sxs-lookup"><span data-stu-id="18215-120"><em>Remote Server=</em></span></span></p></td>
<td><p><span data-ttu-id="18215-p103">クライアント側の接続を開くときに使用するサーバーのパス名を指定します (リモート データ サービスのみ)。</span><span class="sxs-lookup"><span data-stu-id="18215-p103">Specifies the path name of the server to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18215-123"><em>URL=</em></span><span class="sxs-lookup"><span data-stu-id="18215-123"><em>URL=</em></span></span></p></td>
<td><p><span data-ttu-id="18215-124">接続文字列を、ファイルやディレクトリなどのリソースを識別する絶対 URL として指定します。</span><span class="sxs-lookup"><span data-stu-id="18215-124">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18215-125">**ConnectionString** プロパティを設定して [Connection](connection-object-ado.md) オブジェクトを開いた後、ADO によって定義された引数名がプロバイダーの対応する引数名にマップされるなど、プロバイダーによってプロパティの内容が変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="18215-125">After you set the **ConnectionString** property and open the [Connection](connection-object-ado.md) object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their provider equivalents.</span></span>

<span data-ttu-id="18215-126">**ConnectionString**プロパティは、 **Open**メソッドの呼び出し中に、現在の**接続文字列**プロパティをオーバーライドするために、 [Open](open-method-ado-connection.md)メソッドの*ConnectionString*引数に対して使用する値を自動的に継承します。</span><span class="sxs-lookup"><span data-stu-id="18215-126">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method, so you can override the current **ConnectionString** property during the **Open** method call.</span></span>

<span data-ttu-id="18215-127">*ファイル名*引数には、関連付けられているプロバイダーをロードするのには ADO が発生するため、*プロバイダー*と*ファイル名*の両方の引数を渡すことはできません。</span><span class="sxs-lookup"><span data-stu-id="18215-127">Because the *File Name* argument causes ADO to load the associated provider, you cannot pass both the *Provider* and *File Name* arguments.</span></span>

<span data-ttu-id="18215-128">**ConnectionString** プロパティは、接続が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="18215-128">The **ConnectionString** property is read/write when the connection is closed and read-only when it is open.</span></span>

<span data-ttu-id="18215-p104">**ConnectionString** プロパティにおいて重複している引数は無視されます。引数の最後のインスタンスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="18215-p104">Duplicates of an argument in the **ConnectionString** property are ignored. The last instance of any argument is used.</span></span>

<span data-ttu-id="18215-131">**リモート データ サービスの使用法**使用すると、クライアント側の**Connection**オブジェクトの**ConnectionString**プロパティは*リモート プロバイダー*と*リモート サーバー*のパラメーターのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="18215-131">**Remote Data Service Usage**When used on a client-side **Connection** object, the **ConnectionString** property can include only the *Remote Provider* and *Remote Server* parameters.</span></span>

