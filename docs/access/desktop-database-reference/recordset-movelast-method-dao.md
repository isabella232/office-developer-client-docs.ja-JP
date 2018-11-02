---
title: Recordset.MoveLast メソッド (DAO)
TOCTitle: MoveLast Method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44b38825ad2757be1cb17bfc7f7a6721bc073968
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920096"
---
# <a name="recordsetmovelast-method-dao"></a><span data-ttu-id="2899d-102">Recordset.MoveLast メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="2899d-102">Recordset.MoveLast method (DAO)</span></span>


<span data-ttu-id="2899d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2899d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2899d-104">指定された **Recordset** オブジェクトの最後のレコードに移動し、そのレコードをカレント レコードにします。</span><span class="sxs-lookup"><span data-stu-id="2899d-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2899d-105">構文</span><span class="sxs-lookup"><span data-stu-id="2899d-105">Syntax</span></span>

<span data-ttu-id="2899d-106">*式*です。MoveLast (***オプション***)</span><span class="sxs-lookup"><span data-stu-id="2899d-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="2899d-107">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="2899d-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="2899d-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2899d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2899d-109">名前</span><span class="sxs-lookup"><span data-stu-id="2899d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2899d-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="2899d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="2899d-111">データ型</span><span class="sxs-lookup"><span data-stu-id="2899d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="2899d-112">説明</span><span class="sxs-lookup"><span data-stu-id="2899d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2899d-113">オプション</span><span class="sxs-lookup"><span data-stu-id="2899d-113">Options</span></span></p></td>
<td><p><span data-ttu-id="2899d-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="2899d-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="2899d-115"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="2899d-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="2899d-116"><strong>MoveLast</strong> への呼び出しを非同期で実行する場合に <strong>dbRunAsync</strong> に設定します。</span><span class="sxs-lookup"><span data-stu-id="2899d-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2899d-117">注釈</span><span class="sxs-lookup"><span data-stu-id="2899d-117">Remarks</span></span>

<span data-ttu-id="2899d-118">**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。</span><span class="sxs-lookup"><span data-stu-id="2899d-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="2899d-p101">カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。</span><span class="sxs-lookup"><span data-stu-id="2899d-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="2899d-p102">**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合、 **BOF** プロパティは **True** で、カレント レコードはありません。</span><span class="sxs-lookup"><span data-stu-id="2899d-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="2899d-123">**MoveFirst** または **MoveLast** を使用したときに、最初のレコードまたは最後のレコードが既にカレント レコードである場合、カレント レコードは変更されません。</span><span class="sxs-lookup"><span data-stu-id="2899d-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="2899d-124">レコード セットは、テーブル タイプ**のレコード セット**(Microsoft Access ワークスペースのみ) を参照している場合の移動は現在のインデックスに従います。</span><span class="sxs-lookup"><span data-stu-id="2899d-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="2899d-125">現在のインデックスを設定するには、 **Index** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="2899d-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="2899d-126">現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。</span><span class="sxs-lookup"><span data-stu-id="2899d-126">If you don't set the current index, the order of returned records is undefined.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2899d-p104">[!メモ] <STRONG>MoveLast</STRONG> メソッドを使用すると、ダイナセット タイプまたはスナップショット タイプの <STRONG>Recordset</STRONG> の末尾までデータを格納して、 <STRONG>Recordset</STRONG> に含まれる現在のレコード数を示すことができます。ただし、このような目的で <STRONG>MoveLast</STRONG> を使用すると、アプリケーションのパフォーマンスが低下する場合があります。 <STRONG>MoveLast</STRONG> を使用してレコード数を取得するのは、新しく開かれた <STRONG>Recordset</STRONG> の正確なレコード数をどうしても取得する必要がある場合だけにしてください。 <STRONG>MoveLast</STRONG> で <STRONG>dbRunAsync</STRONG> 定数を使用すると、メソッドの呼び出しが非同期で実行されます。 <STRONG>Recordset</STRONG> の末尾までデータが格納されたことを確認するには <STRONG>StillExecuting</STRONG> プロパティを使用し、 <STRONG>MoveLast</STRONG> メソッドに対する非同期呼び出しの実行を終了するには <STRONG>Cancel</STRONG> メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2899d-p104">You can use the <STRONG>MoveLast</STRONG> method to fully populate a dynaset- or snapshot-type <STRONG>Recordset</STRONG> to provide the current number of records in the <STRONG>Recordset</STRONG>. However, if you use <STRONG>MoveLast</STRONG> in this way, you can slow down your application's performance. You should only use <STRONG>MoveLast</STRONG> to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened <STRONG>Recordset</STRONG>. If you use the <STRONG>dbRunAsync</STRONG> constant with <STRONG>MoveLast</STRONG>, the method call is asynchronous. You can use the <STRONG>StillExecuting</STRONG> property to determine when the <STRONG>Recordset</STRONG> is fully populated, and you can use the <STRONG>Cancel</STRONG> method to terminate execution of the asynchronous <STRONG>MoveLast</STRONG> method call.</span></span></P>



<span data-ttu-id="2899d-132">前方のみタイプの**Recordset**オブジェクトでは、 **MoveFirst**、 **MoveLast**、および**MovePrevious**メソッドを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="2899d-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="2899d-133">**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、 **Move** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2899d-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

