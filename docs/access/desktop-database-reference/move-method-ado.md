---
title: メソッドを ActiveX データ オブジェクト (ADO) の移動します。
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 30feb9aabeb84c577b415b2872ce407cf3fc0f44
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950007"
---
# <a name="move-method-ado"></a><span data-ttu-id="63cc2-102">Move メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="63cc2-102">Move method (ADO)</span></span>

<span data-ttu-id="63cc2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="63cc2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63cc2-104">[Recordset](recordset-object-ado.md) オブジェクトでカレント レコードの位置を移動します。</span><span class="sxs-lookup"><span data-stu-id="63cc2-104">Moves the position of the current record in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="63cc2-105">構文</span><span class="sxs-lookup"><span data-stu-id="63cc2-105">Syntax</span></span>

<span data-ttu-id="63cc2-106">*レコード セット*です。*NumRecords*、*起動*に移動します。</span><span class="sxs-lookup"><span data-stu-id="63cc2-106">*recordset*.Move *NumRecords*, *Start*</span></span>

## <a name="parameters"></a><span data-ttu-id="63cc2-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63cc2-107">Parameters</span></span>

|<span data-ttu-id="63cc2-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63cc2-108">Parameter</span></span>|<span data-ttu-id="63cc2-109">説明</span><span class="sxs-lookup"><span data-stu-id="63cc2-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="63cc2-110">*NumRecords*</span><span class="sxs-lookup"><span data-stu-id="63cc2-110">*NumRecords*</span></span> |<span data-ttu-id="63cc2-111">カレント レコードの位置を移動するレコード数を指定する、符号付きの長整数型 ( **Long** ) の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="63cc2-111">A signed **Long** expression that specifies the number of records that the current record position moves.</span></span>|
|<span data-ttu-id="63cc2-112">*Start*</span><span class="sxs-lookup"><span data-stu-id="63cc2-112">*Start*</span></span> |<span data-ttu-id="63cc2-p101">省略可能です。ブックマークとして評価される文字列型 ( **String** ) の値またはバリアント型 ( **Variant** ) を指定します。 [BookmarkEnum](bookmarkenum.md) 値を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="63cc2-p101">Optional. A **String** value or **Variant** that evaluates to a bookmark. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|

## <a name="remarks"></a><span data-ttu-id="63cc2-116">解説</span><span class="sxs-lookup"><span data-stu-id="63cc2-116">Remarks</span></span>

<span data-ttu-id="63cc2-117">**Move** メソッドは、すべての **Recordset** オブジェクトでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="63cc2-117">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="63cc2-p102">*NumRecords* 引数がゼロより大きい場合、現在のレコードの位置は前方 (**Recordset** の末尾方向) に移動します。*NumRecords* がゼロより小さい場合、現在のレコードの位置は後方 (**Recordset** の先頭方向) に移動します。</span><span class="sxs-lookup"><span data-stu-id="63cc2-p102">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="63cc2-120">**Move**メソッドを呼び出しては、最初のレコードよりも前にカレント レコードの位置を移動すると、現在のレコードに設定 (されます[BOF](bof-eof-properties-ado.md)が**True**になる)、レコード セットの最初のレコードより前に位置します。</span><span class="sxs-lookup"><span data-stu-id="63cc2-120">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset ([BOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="63cc2-121">**BOF** プロパティが既に **True** の場合、後方へ移動しようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="63cc2-121">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="63cc2-122">**Move**メソッドを呼び出しては、最後のレコードの後のポイントにカレント レコードの位置を移動に設定され、現在のレコード位置 ([EOF](bof-eof-properties-ado.md)は**True**)、レコード セットの最後のレコードより後にします。</span><span class="sxs-lookup"><span data-stu-id="63cc2-122">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset ([EOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="63cc2-123">**EOF** プロパティが既に **True** の場合、前方へ移動しようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="63cc2-123">An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="63cc2-124">空の **Recordset** オブジェクトから **Move** メソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="63cc2-124">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="63cc2-125">*起動*引数を渡すと、移動は、 **Recordset**オブジェクトがブックマークをサポートするいると仮定して、このブックマークを持つレコードを基準にしては。</span><span class="sxs-lookup"><span data-stu-id="63cc2-125">If you pass the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="63cc2-126">指定しない場合は、カレント レコードが移動の基準となります。</span><span class="sxs-lookup"><span data-stu-id="63cc2-126">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="63cc2-127">*NumRecords*引数を現在のレコード位置が現在キャッシュされているレコード グループの範囲外に移動する、プロバイダーからのレコードをローカルにキャッシュ、 [CacheSize](cachesize-property-ado.md)プロパティを使用する場合、レコードの新しいグループを取得するために ADO を強制的に移動先のレコードから開始しています。</span><span class="sxs-lookup"><span data-stu-id="63cc2-127">If you are using the [CacheSize](cachesize-property-ado.md) property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="63cc2-128">新しく取り込まれるグループのサイズは **CacheSize** プロパティによって決まり、移動先のレコードが最初に取得されるレコードになります。</span><span class="sxs-lookup"><span data-stu-id="63cc2-128">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

<span data-ttu-id="63cc2-129">場合は、 **Recordset**オブジェクトが前方スクロールのみ、ユーザー渡すこともできます、 *NumRecords*引数より小さい値 0、リンク先が現在キャッシュされているレコードのセット内では。</span><span class="sxs-lookup"><span data-stu-id="63cc2-129">If the **Recordset** object is forward only, a user can still pass a *NumRecords* argument less than zero, provided the destination is within the current set of cached records.</span></span> <span data-ttu-id="63cc2-130">**Move** メソッドを呼び出して、カレント レコードの位置を、キャッシュされている最初のレコードより前のレコードに移動しようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="63cc2-130">If the **Move** call would move the current record position to a record before the first cached record, an error will occur.</span></span> <span data-ttu-id="63cc2-131">このように、前方スクロールのみをサポートするプロバイダーで、完全スクロールをサポートするレコード キャッシュを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="63cc2-131">Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling.</span></span> <span data-ttu-id="63cc2-132">キャッシュされたレコードはメモリに読み込まれるため、必要以上のレコードのキャッシュは避けてください。</span><span class="sxs-lookup"><span data-stu-id="63cc2-132">Because cached records are loaded into memory, you should avoid caching more records than is necessary.</span></span> <span data-ttu-id="63cc2-133">前方スクロールのみ可能な **Recordset** オブジェクトでも、この方法で後方への移動をサポートできますが、前方スクロールのみ可能な [Recordset](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) オブジェクトで **MovePrevious** メソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="63cc2-133">Even if a forward-only **Recordset** object supports backward moves in this way, calling the [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method on any forward-only **Recordset** object will still generate an error.</span></span>


> [!NOTE]
> <span data-ttu-id="63cc2-p108">[!メモ] 前方スクロールのみ可能な **Recordset** で後方への移動がサポートされているかどうかは、プロバイダーによります。カレント レコードが **Recordset** の最後のレコードの後にある場合、後方への **Move** を実行しても現在の位置が正しく示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="63cc2-p108">Support for moving backwards in a forward-only **Recordset** is not predictable, depending upon your provider. If the current record has been postioned after the last record in the **Recordset**, **Move** backwards may not result in the correct current position.</span></span>


