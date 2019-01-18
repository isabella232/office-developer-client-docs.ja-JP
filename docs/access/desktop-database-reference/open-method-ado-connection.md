---
title: Open メソッド (ADO Connection)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b83eb87b181320c86e1aea91ede70cd173a5ce
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717567"
---
# <a name="open-method-ado-connection"></a><span data-ttu-id="0f5db-102">Open メソッド (ADO Connection)</span><span class="sxs-lookup"><span data-stu-id="0f5db-102">Open method (ADO Connection)</span></span>

<span data-ttu-id="0f5db-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0f5db-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="0f5db-104">データ ソースへの接続を開きます。</span><span class="sxs-lookup"><span data-stu-id="0f5db-104">Opens a connection to a data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f5db-105">構文</span><span class="sxs-lookup"><span data-stu-id="0f5db-105">Syntax</span></span>

<span data-ttu-id="0f5db-106">*接続*します。*接続文字列*、*ユーザー Id*、*パスワード\*\*のオプション*を開く</span><span class="sxs-lookup"><span data-stu-id="0f5db-106">*connection*.Open*ConnectionString*, *UserID*, *Password*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="0f5db-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f5db-107">Parameters</span></span>

|<span data-ttu-id="0f5db-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f5db-108">Parameter</span></span>|<span data-ttu-id="0f5db-109">説明</span><span class="sxs-lookup"><span data-stu-id="0f5db-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0f5db-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="0f5db-110">*ConnectionString*</span></span> |<span data-ttu-id="0f5db-p101">省略可能です。接続情報を含む文字列型 ( **String** ) の値です。有効な設定値の詳細については、 [ConnectionString](connectionstring-property-ado.md) プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f5db-p101">Optional. A **String** value that contains connection information. See the [ConnectionString](connectionstring-property-ado.md) property for details on valid settings.</span></span>|
|<span data-ttu-id="0f5db-114">*UserID*</span><span class="sxs-lookup"><span data-stu-id="0f5db-114">*UserID*</span></span> |<span data-ttu-id="0f5db-p102">省略可能です。接続を確立するときに使用するユーザー名を含む、文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="0f5db-p102">Optional. A **String** value that contains a user name to use when establishing the connection.</span></span>|
|<span data-ttu-id="0f5db-117">*Password*</span><span class="sxs-lookup"><span data-stu-id="0f5db-117">*Password*</span></span> |<span data-ttu-id="0f5db-p103">省略可能です。接続を確立するときに使用するパスワードを含む、文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="0f5db-p103">Optional. A **String** value that contains a password to use when establishing the connection.</span></span>|
|<span data-ttu-id="0f5db-120">*Options*</span><span class="sxs-lookup"><span data-stu-id="0f5db-120">*Options*</span></span> |<span data-ttu-id="0f5db-p104">省略可能です。接続が確立された後 (同期) または接続が確立される前 (非同期) のどちらでこのメソッドが返るかを指定する [ConnectOptionEnum](connectoptionenum.md) 値です。</span><span class="sxs-lookup"><span data-stu-id="0f5db-p104">Optional. A [ConnectOptionEnum](connectoptionenum.md) value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0f5db-123">解説</span><span class="sxs-lookup"><span data-stu-id="0f5db-123">Remarks</span></span>

<span data-ttu-id="0f5db-p105">**Connection** オブジェクトで [Open](connection-object-ado.md) メソッドを使用すると、データ ソースへの物理的な接続が確立されます。このメソッドが正常に終了すると、接続が有効になり、接続に対してコマンドを発行して、その結果を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5db-p105">Using the **Open** method on a [Connection](connection-object-ado.md) object establishes the physical connection to a data source. After this method successfully completes, the connection is live and you can issue commands against it and process the results.</span></span>

<span data-ttu-id="0f5db-126">一連の*引数* *= 値*ステートメントを指定するセミコロン、またはファイルまたは URL で識別されるリソースはディレクトリを含む接続文字列を指定するのに省略可能な*ConnectionString*引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="0f5db-126">Use the optional *ConnectionString* argument to specify either a connection string containing a series of *argument* *= value* statements separated by semicolons, or a file or directory resource identified with a URL.</span></span> <span data-ttu-id="0f5db-127">**ConnectionString**プロパティは、 *ConnectionString*引数に対して使用する値を自動的に継承します。</span><span class="sxs-lookup"><span data-stu-id="0f5db-127">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument.</span></span> <span data-ttu-id="0f5db-128">したがって、開く前に**Connection**オブジェクトの**ConnectionString**プロパティを設定するか、 **Open**メソッドの呼び出し時に現在の接続パラメーターのオーバーライドを設定または*接続文字列*の引数を使用して.</span><span class="sxs-lookup"><span data-stu-id="0f5db-128">Therefore, you can either set the **ConnectionString** property of the **Connection** object before opening it, or use the *ConnectionString* argument to set or override the current connection parameters during the **Open** method call.</span></span>

<span data-ttu-id="0f5db-129">ユーザーとパスワードの情報を、*ConnectionString* 引数と、省略可能な *UserID* 引数および *Password* 引数の両方で渡すと、*UserID* 引数と *Password* 引数の方が、*ConnectionString* で指定した値より優先されます。</span><span class="sxs-lookup"><span data-stu-id="0f5db-129">If you pass user and password information both in the *ConnectionString* argument and in the optional *UserID* and *Password* arguments, the *UserID* and *Password* arguments will override the values specified in *ConnectionString*.</span></span>

<span data-ttu-id="0f5db-p107">開いている **Connection** オブジェクトに対する操作が完了したら、[Close](close-method-ado.md) メソッドを使用して関連するすべてのシステム リソースを解放します。オブジェクトを閉じても、オブジェクトはメモリから削除されません。オブジェクトのプロパティ設定を変更し、**Open** メソッドを使用して、後で再度開くことができます。オブジェクトをメモリから完全に削除するには、オブジェクト変数に *Nothing* を設定します。</span><span class="sxs-lookup"><span data-stu-id="0f5db-p107">When you have concluded your operations over an open **Connection**, use the [Close](close-method-ado.md) method to free any associated system resources. Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later. To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="0f5db-133">**リモート データ サービスの使用法**クライアント側の**接続**オブジェクトを使用する場合は、**接続**オブジェクトの[レコード セット](recordset-object-ado.md)が開かれるまで、 **Open**メソッドは実際には、サーバーへの接続を確立されません。</span><span class="sxs-lookup"><span data-stu-id="0f5db-133">**Remote Data Service Usage**When used on a client-side **Connection** object, the **Open** method doesn't actually establish a connection to the server until a [Recordset](recordset-object-ado.md) is opened on the **Connection** object.</span></span>

> [!NOTE]
> <span data-ttu-id="0f5db-134">[!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0f5db-134">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="0f5db-135">詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f5db-135">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


