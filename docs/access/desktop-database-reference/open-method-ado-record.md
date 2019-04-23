---
title: Open メソッド (ADO Record)
TOCTitle: Open method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db8953cafc5ad266c81c51e59cbf92787d07cdfb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288379"
---
# <a name="open-method-ado-record"></a><span data-ttu-id="1cb3d-102">Open メソッド (ADO Record)</span><span class="sxs-lookup"><span data-stu-id="1cb3d-102">Open method (ADO Record)</span></span>

<span data-ttu-id="1cb3d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cb3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1cb3d-104">既存の [Record](record-object-ado.md) オブジェクトを開くか、または **Record** で表される新しいアイテム (ファイル、ディレクトリなど) を作成します。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-104">Opens an existing [Record](record-object-ado.md) object, or creates a new item represented by the **Record** (such as a file or directory).</span></span>

## <a name="syntax"></a><span data-ttu-id="1cb3d-105">構文</span><span class="sxs-lookup"><span data-stu-id="1cb3d-105">Syntax</span></span>

<span data-ttu-id="1cb3d-106">Open *Source*、 *ActiveConnection*、 *Mode*、 *createoptions*、 *options*、 *UserName*、 *Password*</span><span class="sxs-lookup"><span data-stu-id="1cb3d-106">Open *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *UserName*, *Password*</span></span>

## <a name="parameters"></a><span data-ttu-id="1cb3d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1cb3d-107">Parameters</span></span>

|<span data-ttu-id="1cb3d-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1cb3d-108">Parameter</span></span>|<span data-ttu-id="1cb3d-109">説明</span><span class="sxs-lookup"><span data-stu-id="1cb3d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1cb3d-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="1cb3d-110">*Source*</span></span> |<span data-ttu-id="1cb3d-p101">省略可能です。 **Record** オブジェクトで表されるエンティティの URL、 **Command** 、開かれた **Recordset** または別の [Record](recordset-object-ado.md) オブジェクト、SQL SELECT ステートメントを含む文字列、またはテーブル名を表すバリアント型 ( **Variant** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-p101">Optional. A **Variant** that may represent the URL of the entity to be represented by this **Record** object, a **Command**, an open [Recordset](recordset-object-ado.md) or another **Record** object, a string containing a SQL SELECT statement or a table name.</span></span>|
|<span data-ttu-id="1cb3d-113">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="1cb3d-113">*ActiveConnection*</span></span> | <span data-ttu-id="1cb3d-p102">省略可能です。接続文字列または開かれた **Connection** オブジェクトを表すバリアント型 ( [Variant](connection-object-ado.md) ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-p102">Optional. A **Variant** that represents the connect string or open [Connection](connection-object-ado.md) object.</span></span>|
|<span data-ttu-id="1cb3d-116">*Mode*</span><span class="sxs-lookup"><span data-stu-id="1cb3d-116">*Mode*</span></span> |<span data-ttu-id="1cb3d-p103">省略可能です。結果の [Record](connectmodeenum.md) オブジェクトのアクセス モードを **ConnectModeEnum** 値で指定します。既定値は **adModeUnknown** です。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-p103">Optional. A [ConnectModeEnum](connectmodeenum.md) value, whose default value is **adModeUnknown**, that specifies the access mode for the resultant **Record** object.</span></span>|
|<span data-ttu-id="1cb3d-119">*createoptions*</span><span class="sxs-lookup"><span data-stu-id="1cb3d-119">*CreateOptions*</span></span> |<span data-ttu-id="1cb3d-p104">省略可能です。既存のファイルまたはディレクトリを開くか、新しいファイルまたはディレクトリを作成するかを、[RecordCreateOptionsEnum](recordcreateoptionsenum.md) 値で指定します。既定値は **adFailIfNotExists** です。既定値の場合、アクセス モードは [Mode](mode-property-ado.md) プロパティから取得されます。このパラメーターは、*Source* パラメーターに URL が含まれていないと無視されます。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-p104">Optional. A [RecordCreateOptionsEnum](recordcreateoptionsenum.md) value, whose default value is **adFailIfNotExists**, that specifies whether an existing file or directory should be opened, or a new file or directory should be created. If set to the default value, the access mode is obtained from the [Mode](mode-property-ado.md) property. This parameter is ignored when the *Source* parameter doesnt contain a URL.</span></span>|
|<span data-ttu-id="1cb3d-124">*Options*</span><span class="sxs-lookup"><span data-stu-id="1cb3d-124">*Options*</span></span> |<span data-ttu-id="1cb3d-p105">省略可能です。 [Record](recordopenoptionsenum.md) を開くときのオプションを **RecordOpenOptionsEnum** 値で指定します。既定値は **adOpenRecordUnspecified** です。これらの値は組み合わせることもできます。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-p105">Optional. A [RecordOpenOptionsEnum](recordopenoptionsenum.md) value, whose default value is **adOpenRecordUnspecified**, that specifies options for opening the **Record**. These values may be combined.</span></span>|
|<span data-ttu-id="1cb3d-128">*UserName*</span><span class="sxs-lookup"><span data-stu-id="1cb3d-128">*UserName*</span></span> |<span data-ttu-id="1cb3d-129">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-129">Optional.</span></span> <span data-ttu-id="1cb3d-130">*Source* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-130">A **String** value that contains the user ID that, if needed, authorizes access to *Source*.</span></span>|
|<span data-ttu-id="1cb3d-131">*Password*</span><span class="sxs-lookup"><span data-stu-id="1cb3d-131">*Password*</span></span> |<span data-ttu-id="1cb3d-132">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-132">Optional.</span></span> <span data-ttu-id="1cb3d-133">*UserName* を確認するためのパスワードを含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-133">A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1cb3d-134">注釈</span><span class="sxs-lookup"><span data-stu-id="1cb3d-134">Remarks</span></span>

<span data-ttu-id="1cb3d-135">*Source* には、次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-135">*Source* may be:</span></span>

- <span data-ttu-id="1cb3d-p108">URL。URL のプロトコルが http の場合、既定ではインターネット プロバイダーが呼び出されます。URL が実行可能スクリプト (拡張子が .ASP のページなど) を含むノードを指している場合、既定では実行されたコンテンツではなく、そのソースを含む **Record** が開かれます。この動作は *Options* 引数を使用して修正します。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-p108">A URL. If the protocol for the URL is http, then the Internet Provider will be invoked by default. If the URL points to a node that contains an executable script (such as an .ASP page), then a **Record** containing the source rather than the executed contents is opened by default. Use the *Options* argument to modify this behavior.</span></span>

- <span data-ttu-id="1cb3d-p109">**Record** オブジェクト。別の **Record** から開かれた **Record** オブジェクトは、元の **Record** オブジェクトを複製します。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-p109">A **Record** object. A **Record** object opened from another **Record** will clone the original **Record** object.</span></span>

- <span data-ttu-id="1cb3d-p110">**Command** オブジェクト。開かれた **Record** オブジェクトは、 **Command** を実行することによって返された単一の行を表します。結果に複数の行が含まれる場合、レコードには最初の行の内容が入り、 **Errors** コレクションにエラーが追加されることがあります。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-p110">A **Command** object. The opened **Record** object represents the single row returned by executing the **Command**. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

- <span data-ttu-id="1cb3d-p111">SQL SELECT ステートメント。開かれた **Record** オブジェクトは、文字列の内容を実行することによって返された単一の行を表します。結果に複数の行が含まれる場合、レコードには最初の行の内容が入り、 **Errors** コレクションにエラーが追加されることがあります。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-p111">A SQL SELECT statement. The opened **Record** object represents the single row returned by executing the contents of the string. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

- <span data-ttu-id="1cb3d-148">テーブル名。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-148">A table name.</span></span>

<span data-ttu-id="1cb3d-149">**Record** オブジェクトが、URL でアクセスできないエンティティ (データベースから派生した **Recordset** の行など) を表す場合、 [ParentURL](parenturl-property-ado.md) プロパティの値、および **adRecordURL** 定数でアクセスするフィールドの値はいずれも Null になります。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-149">If the **Record** object represents an entity that cannot be accessed with a URL (for example, a row of a **Recordset** derived from a database), then the values of both the [ParentURL](parenturl-property-ado.md) property and the field accessed with the **adRecordURL** constant are null.</span></span>

> [!NOTE]
> <span data-ttu-id="1cb3d-150">[!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-150">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="1cb3d-151">詳細については、「[絶対 url と相対 url](absolute-and-relative-urls.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1cb3d-151">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


