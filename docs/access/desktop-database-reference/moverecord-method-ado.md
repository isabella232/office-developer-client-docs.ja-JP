---
title: MoveRecord メソッド (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 296232b05041c1e059b5134fdde11fceac4e3d43
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949895"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="2913a-102">MoveRecord メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="2913a-102">MoveRecord method (ADO)</span></span>

<span data-ttu-id="2913a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2913a-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="2913a-104">[Record](record-object-ado.md) で表されるエンティティを別の場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="2913a-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="2913a-105">構文</span><span class="sxs-lookup"><span data-stu-id="2913a-105">Syntax</span></span>

<span data-ttu-id="2913a-106">*レコード*です。関係 (*ソース*、*変換先*、*ユーザー名*、*パスワード*、*オプション*、*非同期*)</span><span class="sxs-lookup"><span data-stu-id="2913a-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="2913a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2913a-107">Parameters</span></span>

|<span data-ttu-id="2913a-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2913a-108">Parameter</span></span>|<span data-ttu-id="2913a-109">説明</span><span class="sxs-lookup"><span data-stu-id="2913a-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2913a-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="2913a-110">*Source*</span></span> |<span data-ttu-id="2913a-p101">省略可能です。移動する **Record** を示す URL を含む文字列型 (**String**) の値を指定します。*Source* を省略するか、または空文字列を指定すると、この **Record** で表されるオブジェクトが移動されます。たとえば、**Record** がファイルを表している場合は、ファイルの内容が *Destination* で指定した場所に移動されます。</span><span class="sxs-lookup"><span data-stu-id="2913a-p101">Optional. A **String** value that contains a URL identifying the **Record** to be moved. If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved. For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>|
|<span data-ttu-id="2913a-115">*Destination*</span><span class="sxs-lookup"><span data-stu-id="2913a-115">*Destination*</span></span> |<span data-ttu-id="2913a-116">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="2913a-116">Optional.</span></span> <span data-ttu-id="2913a-117">*ソース*の移動先の場所を指定する URL を含む**文字列**値。</span><span class="sxs-lookup"><span data-stu-id="2913a-117">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>|
|<span data-ttu-id="2913a-118">*UserName*</span><span class="sxs-lookup"><span data-stu-id="2913a-118">*UserName*</span></span> |<span data-ttu-id="2913a-p103">省略可能です。*Destination* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2913a-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="2913a-121">*Password*</span><span class="sxs-lookup"><span data-stu-id="2913a-121">*Password*</span></span> |<span data-ttu-id="2913a-p104">省略可能です。*UserName* を確認するためのパスワードを含む、文字列型 (**String**) を指定します。</span><span class="sxs-lookup"><span data-stu-id="2913a-p104">Optional. A **String** that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="2913a-124">*Options*</span><span class="sxs-lookup"><span data-stu-id="2913a-124">*Options*</span></span> |<span data-ttu-id="2913a-p105">省略可能です。[MoveRecordOptionsEnum](moverecordoptionsenum.md) 値を指定します。既定値は、 **adMoveUnspecified** です。このメソッドの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2913a-p105">Optional. A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="2913a-128">*Async*</span><span class="sxs-lookup"><span data-stu-id="2913a-128">*Async*</span></span> |<span data-ttu-id="2913a-129">省略可能。</span><span class="sxs-lookup"><span data-stu-id="2913a-129">Optional.</span></span> <span data-ttu-id="2913a-130">**ブール型**の値**true の場合**、この操作を非同期にする必要がありますを指定します。</span><span class="sxs-lookup"><span data-stu-id="2913a-130">A **Boolean** value that, when **True**, specifies this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="2913a-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="2913a-131">Return value</span></span>

<span data-ttu-id="2913a-132">文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="2913a-132">A **String** value.</span></span> <span data-ttu-id="2913a-133">通常、*送信先*の値が返されます。</span><span class="sxs-lookup"><span data-stu-id="2913a-133">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="2913a-134">ただし、実際に返される値はプロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2913a-134">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="2913a-135">解説</span><span class="sxs-lookup"><span data-stu-id="2913a-135">Remarks</span></span>

<span data-ttu-id="2913a-136">*送信元*と*送信先*の値いない必要があります同じです。それ以外の場合、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2913a-136">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="2913a-137">少なくともサーバー、パス、およびリソース名は異なる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2913a-137">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="2913a-p109">Internet Publishing Provider を使用して移動されるファイルでは、*Options* で特に指定のない限り、移動されるファイル内のすべてのハイパーテキスト リンクが更新されます。*Destination* に既存のオブジェクト (たとえば、ファイルまたはディレクトリ) を指定する場合、**adMoveOverWrite** が指定されていないと、このメソッドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="2913a-p109">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*. This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2913a-p110">[!メモ] <STRONG>adMoveOverWrite</STRONG> オプションは十分に注意して使用してください。たとえば、ファイルをディレクトリに移動するときにこのオプションを指定していると、移動先のディレクトリが "削除" され、移動元のファイルに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2913a-p110">Use the <STRONG>adMoveOverWrite</STRONG> option judiciously. For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span></P>



<span data-ttu-id="2913a-p111">この操作の終了後、 **Record** オブジェクトの一部の属性 ( [ParentURL](parenturl-property-ado.md) プロパティなど) は更新されなくなります。 **Record** オブジェクトのプロパティを更新するには、 **Record** を閉じ、そのファイルまたはディレクトリが移動された場所の URL でもう一度開いてください。</span><span class="sxs-lookup"><span data-stu-id="2913a-p111">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes. Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="2913a-p112">**Recordset** から取得した [Record](recordset-object-ado.md) の場合、ファイルまたはディレクトリの移動後の場所は、 **Recordset** にすぐには反映されません。反映するには、 **Recordset** をいったん閉じてもう一度開いてください。</span><span class="sxs-lookup"><span data-stu-id="2913a-p112">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**. Refresh the **Recordset** by closing and re-opening it.</span></span>


> [!NOTE]
> <span data-ttu-id="2913a-146">[!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2913a-146">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="2913a-147">詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2913a-147">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


