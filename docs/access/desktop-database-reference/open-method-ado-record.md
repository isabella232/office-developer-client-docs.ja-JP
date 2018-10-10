---
title: Open メソッド (ADO Record)
TOCTitle: Open Method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d56fbf28cd878a8a8fd803bf550d81bc9ac2c96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476722"
---
# <a name="open-method-ado-record"></a><span data-ttu-id="ec7c5-102">Open メソッド (ADO Record)</span><span class="sxs-lookup"><span data-stu-id="ec7c5-102">Open Method (ADO Record)</span></span>


<span data-ttu-id="ec7c5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec7c5-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="ec7c5-104">既存の [Record](record-object-ado.md) オブジェクトを開くか、または **Record** で表される新しいアイテム (ファイル、ディレクトリなど) を作成します。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-104">Opens an existing [Record](record-object-ado.md) object, or creates a new item represented by the **Record** (such as a file or directory).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7c5-105">構文</span><span class="sxs-lookup"><span data-stu-id="ec7c5-105">Syntax</span></span>

<span data-ttu-id="ec7c5-106">*ソース*、 *ActiveConnection*、*モード*、 *CreateOptions*、*オプション*、*ユーザー名*、*パスワード*を開く</span><span class="sxs-lookup"><span data-stu-id="ec7c5-106">Open *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *UserName*, *Password*</span></span>

## <a name="parameters"></a><span data-ttu-id="ec7c5-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ec7c5-107">Parameters</span></span>

  - <span data-ttu-id="ec7c5-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="ec7c5-108">*Source*</span></span>

  - <span data-ttu-id="ec7c5-p101">省略可能です。 **Record** オブジェクトで表されるエンティティの URL、 **Command** 、開かれた **Recordset** または別の [Record](recordset-object-ado.md) オブジェクト、SQL SELECT ステートメントを含む文字列、またはテーブル名を表すバリアント型 ( **Variant** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-p101">Optional. A **Variant** that may represent the URL of the entity to be represented by this **Record** object, a **Command**, an open [Recordset](recordset-object-ado.md) or another **Record** object, a string containing a SQL SELECT statement or a table name.</span></span>

  - <span data-ttu-id="ec7c5-111">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="ec7c5-111">*ActiveConnection*</span></span>

  - <span data-ttu-id="ec7c5-p102">省略可能です。接続文字列または開かれた **Connection** オブジェクトを表すバリアント型 ( [Variant](connection-object-ado.md) ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-p102">Optional. A **Variant** that represents the connect string or open [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="ec7c5-114">*Mode*</span><span class="sxs-lookup"><span data-stu-id="ec7c5-114">*Mode*</span></span>

  - <span data-ttu-id="ec7c5-p103">省略可能です。結果の [Record](connectmodeenum.md) オブジェクトのアクセス モードを **ConnectModeEnum** 値で指定します。既定値は **adModeUnknown** です。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-p103">Optional. A [ConnectModeEnum](connectmodeenum.md) value, whose default value is **adModeUnknown**, that specifies the access mode for the resultant **Record** object.</span></span>

  - <span data-ttu-id="ec7c5-117">*CreateOptions*</span><span class="sxs-lookup"><span data-stu-id="ec7c5-117">*CreateOptions*</span></span>

  - <span data-ttu-id="ec7c5-118">省略可能。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-118">Optional.</span></span> <span data-ttu-id="ec7c5-119">[RecordCreateOptionsEnum](recordcreateoptionsenum.md)の値、既定値を持つ**adFailIfNotExists**、既存のファイルまたはディレクトリを開く必要があるかどうかを指定するか、新しいファイルまたはディレクトリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-119">A [RecordCreateOptionsEnum](recordcreateoptionsenum.md) value, whose default value is **adFailIfNotExists**, that specifies whether an existing file or directory should be opened, or a new file or directory should be created.</span></span> <span data-ttu-id="ec7c5-120">アクセス モード、既定値に設定は、 [Mode](mode-property-ado.md)プロパティから取得されます。 場合、</span><span class="sxs-lookup"><span data-stu-id="ec7c5-120">If set to the default value, the access mode is obtained from the [Mode](mode-property-ado.md) property.</span></span> <span data-ttu-id="ec7c5-121">*Source*パラメーターには、URL が含まれていない場合、このパラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-121">This parameter is ignored when the *Source* parameter doesnt contain a URL.</span></span>

  - <span data-ttu-id="ec7c5-122">*Options*</span><span class="sxs-lookup"><span data-stu-id="ec7c5-122">*Options*</span></span>

  - <span data-ttu-id="ec7c5-p105">省略可能です。 [Record](recordopenoptionsenum.md) を開くときのオプションを **RecordOpenOptionsEnum** 値で指定します。既定値は **adOpenRecordUnspecified** です。これらの値は組み合わせることもできます。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-p105">Optional. A [RecordOpenOptionsEnum](recordopenoptionsenum.md) value, whose default value is **adOpenRecordUnspecified**, that specifies options for opening the **Record**. These values may be combined.</span></span>

  - <span data-ttu-id="ec7c5-126">*UserName*</span><span class="sxs-lookup"><span data-stu-id="ec7c5-126">*UserName*</span></span>

  - <span data-ttu-id="ec7c5-p106">省略可能です。*Source* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-p106">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Source*.</span></span>

  - <span data-ttu-id="ec7c5-129">*Password*</span><span class="sxs-lookup"><span data-stu-id="ec7c5-129">*Password*</span></span>

  - <span data-ttu-id="ec7c5-p107">省略可能です。*UserName* を確認するためのパスワードを含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-p107">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec7c5-132">備考</span><span class="sxs-lookup"><span data-stu-id="ec7c5-132">Remarks</span></span>

<span data-ttu-id="ec7c5-133">*ソース*があります。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-133">*Source* may be:</span></span>

  - <span data-ttu-id="ec7c5-134">URL。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-134">A URL.</span></span> <span data-ttu-id="ec7c5-135">URL のプロトコルが http の場合、既定ではインターネット プロバイダーが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-135">If the protocol for the URL is http, then the Internet Provider will be invoked by default.</span></span> <span data-ttu-id="ec7c5-136">URL が実行可能スクリプト (拡張子が .ASP のページなど) を含むノードを指している場合、既定では実行されたコンテンツではなく、そのソースを含む **Record** が開かれます。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-136">If the URL points to a node that contains an executable script (such as an .ASP page), then a **Record** containing the source rather than the executed contents is opened by default.</span></span> <span data-ttu-id="ec7c5-137">この動作を変更するのにには、*オプション*の引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-137">Use the *Options* argument to modify this behavior.</span></span>

  - <span data-ttu-id="ec7c5-p109">**Record** オブジェクト。別の **Record** から開かれた **Record** オブジェクトは、元の **Record** オブジェクトを複製します。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-p109">A **Record** object. A **Record** object opened from another **Record** will clone the original **Record** object.</span></span>

  - <span data-ttu-id="ec7c5-p110">**Command** オブジェクト。開かれた **Record** オブジェクトは、 **Command** を実行することによって返された単一の行を表します。結果に複数の行が含まれる場合、レコードには最初の行の内容が入り、 **Errors** コレクションにエラーが追加されることがあります。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-p110">A **Command** object. The opened **Record** object represents the single row returned by executing the **Command**. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="ec7c5-p111">SQL SELECT ステートメント。開かれた **Record** オブジェクトは、文字列の内容を実行することによって返された単一の行を表します。結果に複数の行が含まれる場合、レコードには最初の行の内容が入り、 **Errors** コレクションにエラーが追加されることがあります。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-p111">A SQL SELECT statement. The opened **Record** object represents the single row returned by executing the contents of the string. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="ec7c5-146">テーブル名。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-146">A table name.</span></span>

<span data-ttu-id="ec7c5-147">**Record** オブジェクトが、URL でアクセスできないエンティティ (データベースから派生した **Recordset** の行など) を表す場合、 [ParentURL](parenturl-property-ado.md) プロパティの値、および **adRecordURL** 定数でアクセスするフィールドの値はいずれも Null になります。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-147">If the **Record** object represents an entity that cannot be accessed with a URL (for example, a row of a **Recordset** derived from a database), then the values of both the [ParentURL](parenturl-property-ado.md) property and the field accessed with the **adRecordURL** constant are null.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ec7c5-p112">[!メモ] http 体系を使用している URL は、<A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A> を自動的に呼び出します。詳細については、「 <A href="absolute-and-relative-urls.md">絶対 URL と相対 URL</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec7c5-p112">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>

