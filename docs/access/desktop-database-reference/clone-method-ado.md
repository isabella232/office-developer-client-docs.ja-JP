---
title: メソッドを ActiveX データ オブジェクト (ADO) の複製します。
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c72902c4ed1d1d2657bfa6e2b4c5f84d76dfefa3
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950259"
---
# <a name="clone-method-ado"></a><span data-ttu-id="e03c9-102">Clone メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="e03c9-102">Clone method (ADO)</span></span>

<span data-ttu-id="e03c9-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e03c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e03c9-p101">既存の [Recordset](recordset-object-ado.md) オブジェクトから **Recordset** オブジェクトの複製を作成します。必要に応じて、複製を読み取り専用に指定できます。</span><span class="sxs-lookup"><span data-stu-id="e03c9-p101">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object. Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e03c9-106">書式</span><span class="sxs-lookup"><span data-stu-id="e03c9-106">Syntax</span></span>

<span data-ttu-id="e03c9-107">**設定\*\*\*rstDuplicate* =  *rstOriginal*。クローン (*LockType\*)</span><span class="sxs-lookup"><span data-stu-id="e03c9-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="e03c9-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="e03c9-108">Return value</span></span>

<span data-ttu-id="e03c9-109">**Recordset** オブジェクトの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="e03c9-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="e03c9-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e03c9-110">Parameters</span></span>

|<span data-ttu-id="e03c9-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e03c9-111">Parameter</span></span>|<span data-ttu-id="e03c9-112">説明</span><span class="sxs-lookup"><span data-stu-id="e03c9-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e03c9-113">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="e03c9-113">*rstDuplicate*</span></span> |<span data-ttu-id="e03c9-114">作成する **Recordset** オブジェクトの複製を示すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="e03c9-114">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>|
|<span data-ttu-id="e03c9-115">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="e03c9-115">*rstOriginal*</span></span> |<span data-ttu-id="e03c9-116">複製元の **Recordset** オブジェクトを示すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="e03c9-116">An object variable that identifies the **Recordset** object to be duplicated.</span></span>|
|<span data-ttu-id="e03c9-117">*ロック。*</span><span class="sxs-lookup"><span data-stu-id="e03c9-117">*LockType*</span></span> |<span data-ttu-id="e03c9-p102">省略可能です。複製元 [Recordset](locktypeenum.md) のロックの種類にするか、または読み取り専用 **Recordset** にするかを指定する、 **LockTypeEnum** の値です。有効な値は、 **adLockUnspecified** または **adLockReadOnly** です。</span><span class="sxs-lookup"><span data-stu-id="e03c9-p102">Optional. A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**. Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e03c9-121">解説</span><span class="sxs-lookup"><span data-stu-id="e03c9-121">Remarks</span></span>

<span data-ttu-id="e03c9-p103">**Clone** メソッドは、 **Recordset** オブジェクトの複製を複数作成する場合に使用します。特に、レコードセットの複数のカレント レコードを保持したい場合には、このメソッドを使用します。 **Clone** メソッドを使用した方が、元の **Recordset** オブジェクトと同じ定義で新しいオブジェクトを作成して開くよりも効率的です。</span><span class="sxs-lookup"><span data-stu-id="e03c9-p103">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="e03c9-p104">元の [Recordset](filter-property-ado.md) で **Filter** プロパティが設定されていても、複製には適用されません。結果をフィルターするには、新しい **Recordset** の **Filter** プロパティを設定する必要があります。既存の **Filter** 値をコピーする最も簡単な方法は、</span><span class="sxs-lookup"><span data-stu-id="e03c9-p104">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone. Set the **Filter** property of the new **Recordset** in order to filter the results. The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="e03c9-127">のように値を直接代入することです。</span><span class="sxs-lookup"><span data-stu-id="e03c9-127">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="e03c9-p105">1 つの **Recordset** オブジェクトに加えた変更は、カーソルの種類に関係なく、すべての複製で表示できます。ただし、複製元の [Recordset](requery-method-ado.md) で **Requery** を実行した後は、複製は複製元の Recordset とは同期しなくなります。</span><span class="sxs-lookup"><span data-stu-id="e03c9-p105">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="e03c9-130">複製元の **Recordset** を閉じても、その複製は開いたままです。また、1 つの複製を閉じても、複製元または他の複製は開いたままになります。</span><span class="sxs-lookup"><span data-stu-id="e03c9-130">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="e03c9-p106">複製できるのは、ブックマークをサポートする **Recordset** オブジェクトだけです。ブックマークの値は交換可能です。つまり、1 つの **Recordset** オブジェクトのブックマーク参照は、すべての複製の同じレコードを参照します。</span><span class="sxs-lookup"><span data-stu-id="e03c9-p106">You can only clone a **Recordset** object that supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="e03c9-p107">発生する **Recordset** イベントの中には、すべての **Recordset** 複製において発生するものがあります。ただし、複製された **Recordset** によってカレント レコードが異なる可能性があるため、複製ではイベントが無効である場合もあります。</span><span class="sxs-lookup"><span data-stu-id="e03c9-p107">Some **Recordset** events that are triggered will also fire in all **Recordset** clones. However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="e03c9-135">たとえば、あるフィールドの値を変更すると、変更された [Recordset](willchangefield-and-fieldchangecomplete-events-ado.md) とすべての複製で、 **WillChangeField** イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="e03c9-135">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="e03c9-136">**WillChangeField**イベント (変更ありませんが行われた) クローンとして作成された**レコード セット**の*フィールド*・ パラメーターという用語を現在よりも別のレコードがありますクローンの現在のレコードのフィールドのレコード、元の**レコード セット**の変更が発生しました。</span><span class="sxs-lookup"><span data-stu-id="e03c9-136">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="e03c9-137">次の表は、すべての **Recordset** イベントの一覧と、 **Clone** メソッドを使用して生成されたすべてのレコードセット複製に対してそのイベントが有効で発生するかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="e03c9-137">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e03c9-138">イベント</span><span class="sxs-lookup"><span data-stu-id="e03c9-138">Event</span></span></p></th>
<th><p><span data-ttu-id="e03c9-139">複製で発生するか</span><span class="sxs-lookup"><span data-stu-id="e03c9-139">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e03c9-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e03c9-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e03c9-141">いいえ</span><span class="sxs-lookup"><span data-stu-id="e03c9-141">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03c9-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="e03c9-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e03c9-143">いいえ</span><span class="sxs-lookup"><span data-stu-id="e03c9-143">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03c9-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="e03c9-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="e03c9-145">いいえ</span><span class="sxs-lookup"><span data-stu-id="e03c9-145">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03c9-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e03c9-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e03c9-147">はい</span><span class="sxs-lookup"><span data-stu-id="e03c9-147">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03c9-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="e03c9-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e03c9-149">いいえ</span><span class="sxs-lookup"><span data-stu-id="e03c9-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03c9-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e03c9-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e03c9-151">はい</span><span class="sxs-lookup"><span data-stu-id="e03c9-151">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03c9-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e03c9-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e03c9-153">いいえ</span><span class="sxs-lookup"><span data-stu-id="e03c9-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03c9-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="e03c9-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="e03c9-155">はい</span><span class="sxs-lookup"><span data-stu-id="e03c9-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03c9-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="e03c9-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e03c9-157">はい</span><span class="sxs-lookup"><span data-stu-id="e03c9-157">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e03c9-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e03c9-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e03c9-159">いいえ</span><span class="sxs-lookup"><span data-stu-id="e03c9-159">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e03c9-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="e03c9-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="e03c9-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="e03c9-161">No</span></span></p></td>
</tr>
</tbody>
</table>

