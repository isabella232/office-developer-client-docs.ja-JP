---
title: Move メソッド-ActiveX データオブジェクト (ADO)
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c7db661e590bc21605d9c289b1de6d4ae9f46e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288835"
---
# <a name="move-method-ado"></a><span data-ttu-id="53aaf-102">Move メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="53aaf-102">Move method (ADO)</span></span>

<span data-ttu-id="53aaf-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="53aaf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53aaf-104">[Recordset](recordset-object-ado.md) オブジェクトでカレント レコードの位置を移動します。</span><span class="sxs-lookup"><span data-stu-id="53aaf-104">Moves the position of the current record in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="53aaf-105">構文</span><span class="sxs-lookup"><span data-stu-id="53aaf-105">Syntax</span></span>

<span data-ttu-id="53aaf-106">*recordset*。Move *NumRecords*, *Start*</span><span class="sxs-lookup"><span data-stu-id="53aaf-106">*recordset*.Move *NumRecords*, *Start*</span></span>

## <a name="parameters"></a><span data-ttu-id="53aaf-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="53aaf-107">Parameters</span></span>

|<span data-ttu-id="53aaf-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="53aaf-108">Parameter</span></span>|<span data-ttu-id="53aaf-109">説明</span><span class="sxs-lookup"><span data-stu-id="53aaf-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="53aaf-110">*NumRecords*</span><span class="sxs-lookup"><span data-stu-id="53aaf-110">*NumRecords*</span></span> |<span data-ttu-id="53aaf-111">カレント レコードの位置を移動するレコード数を指定する、符号付きの長整数型 ( **Long** ) の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="53aaf-111">A signed **Long** expression that specifies the number of records that the current record position moves.</span></span>|
|<span data-ttu-id="53aaf-112">*Start*</span><span class="sxs-lookup"><span data-stu-id="53aaf-112">*Start*</span></span> |<span data-ttu-id="53aaf-p101">省略可能です。ブックマークとして評価される文字列型 ( **String** ) の値またはバリアント型 ( **Variant** ) を指定します。 [BookmarkEnum](bookmarkenum.md) 値を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="53aaf-p101">Optional. A **String** value or **Variant** that evaluates to a bookmark. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|

## <a name="remarks"></a><span data-ttu-id="53aaf-116">注釈</span><span class="sxs-lookup"><span data-stu-id="53aaf-116">Remarks</span></span>

<span data-ttu-id="53aaf-117">**Move** メソッドは、すべての **Recordset** オブジェクトでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="53aaf-117">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="53aaf-p102">*NumRecords* 引数がゼロより大きい場合、現在のレコードの位置は前方 (**Recordset** の末尾方向) に移動します。*NumRecords* がゼロより小さい場合、現在のレコードの位置は後方 (**Recordset** の先頭方向) に移動します。</span><span class="sxs-lookup"><span data-stu-id="53aaf-p102">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="53aaf-120">**move**メソッドを呼び出して、カレントレコードの位置を最初のレコードの前に移動すると、ADO は現在のレコードを recordset の最初のレコードの前の位置 ([BOF](bof-eof-properties-ado.md)が**True**) に設定します。</span><span class="sxs-lookup"><span data-stu-id="53aaf-120">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset ([BOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="53aaf-121">**BOF** プロパティが既に **True** の場合、後方へ移動しようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="53aaf-121">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="53aaf-p104">**Move** メソッドを呼び出してカレント レコードの位置を最後のレコードの後に移動しようとすると、カレント レコードがレコードセットの最後のレコードの後に設定され、[EOF](bof-eof-properties-ado.md) が **True** になります。**EOF** プロパティが既に **True** の場合、前方へ移動しようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="53aaf-p104">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset ([EOF](bof-eof-properties-ado.md) is **True**). An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="53aaf-124">空の **Recordset** オブジェクトから **Move** メソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="53aaf-124">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="53aaf-p105">*Start* 引数を指定した場合、**Recordset** オブジェクトではブックマークがサポートされていると見なされ、このブックマークを持つレコードが移動の基準となります。指定しない場合は、カレント レコードが移動の基準となります。</span><span class="sxs-lookup"><span data-stu-id="53aaf-p105">If you pass the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks. If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="53aaf-p106">[CacheSize](cachesize-property-ado.md) プロパティを使用してプロバイダーからのレコードをローカルにキャッシュしている場合、*NumRecords* 引数を渡して、現在キャッシュされているレコード グループの範囲外に現在のレコード位置を移動すると、移動先のレコードから始まる新規レコード グループが強制的に取得されます。**CacheSize** プロパティが、新規に取得されるグループのサイズを決定し、移動先のレコードが最初に取得されるレコードになります。</span><span class="sxs-lookup"><span data-stu-id="53aaf-p106">If you are using the [CacheSize](cachesize-property-ado.md) property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record. The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

<span data-ttu-id="53aaf-p107">**Recordset** オブジェクトが前方スクロールのみ可能な場合でも、移動先が現在キャッシュされているレコードセットの範囲内であれば、*NumRecords* 引数に 0 より小さい値を指定できます。**Move** メソッドを呼び出して、カレント レコードの位置を、キャッシュされている最初のレコードより前のレコードに移動しようとすると、エラーが発生します。このように、前方スクロールのみをサポートするプロバイダーで、完全スクロールをサポートするレコード キャッシュを使用することができます。キャッシュされたレコードはメモリに読み込まれるため、必要以上のレコードのキャッシュは避けてください。前方スクロールのみ可能な **Recordset** オブジェクトでも、この方法で後方への移動をサポートできますが、前方スクロールのみ可能な **Recordset** オブジェクトで [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) メソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="53aaf-p107">If the **Recordset** object is forward only, a user can still pass a *NumRecords* argument less than zero, provided the destination is within the current set of cached records. If the **Move** call would move the current record position to a record before the first cached record, an error will occur. Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling. Because cached records are loaded into memory, you should avoid caching more records than is necessary. Even if a forward-only **Recordset** object supports backward moves in this way, calling the [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method on any forward-only **Recordset** object will still generate an error.</span></span>


> [!NOTE]
> <span data-ttu-id="53aaf-p108">[!メモ] 前方スクロールのみ可能な **Recordset** で後方への移動がサポートされているかどうかは、プロバイダーによります。カレント レコードが **Recordset** の最後のレコードの後にある場合、後方への **Move** を実行しても現在の位置が正しく示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="53aaf-p108">Support for moving backwards in a forward-only **Recordset** is not predictable, depending upon your provider. If the current record has been postioned after the last record in the **Recordset**, **Move** backwards may not result in the correct current position.</span></span>


