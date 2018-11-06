---
title: Recordset2.MoveLast メソッド (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 83db6ae8da804237222fc1f58e03058951d7ce41
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998988"
---
# <a name="recordset2movelast-method-dao"></a><span data-ttu-id="d8311-102">Recordset2.MoveLast メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="d8311-102">Recordset2.MoveLast method (DAO)</span></span>

<span data-ttu-id="d8311-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d8311-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8311-104">指定された **Recordset** オブジェクトの最後のレコードに移動し、そのレコードをカレント レコードにします。</span><span class="sxs-lookup"><span data-stu-id="d8311-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8311-105">構文</span><span class="sxs-lookup"><span data-stu-id="d8311-105">Syntax</span></span>

<span data-ttu-id="d8311-106">*式*です。MoveLast (***オプション***)</span><span class="sxs-lookup"><span data-stu-id="d8311-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="d8311-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="d8311-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d8311-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d8311-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8311-109">名前</span><span class="sxs-lookup"><span data-stu-id="d8311-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d8311-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="d8311-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d8311-111">データ型</span><span class="sxs-lookup"><span data-stu-id="d8311-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d8311-112">説明</span><span class="sxs-lookup"><span data-stu-id="d8311-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8311-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="d8311-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="d8311-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="d8311-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="d8311-115"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="d8311-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="d8311-116"><strong>MoveLast</strong> への呼び出しを非同期で実行する場合に <strong>dbRunAsync</strong> に設定します。</span><span class="sxs-lookup"><span data-stu-id="d8311-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d8311-117">注釈</span><span class="sxs-lookup"><span data-stu-id="d8311-117">Remarks</span></span>

<span data-ttu-id="d8311-118">**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。</span><span class="sxs-lookup"><span data-stu-id="d8311-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="d8311-p101">カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。</span><span class="sxs-lookup"><span data-stu-id="d8311-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="d8311-p102">**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合、 **BOF** プロパティは **True** で、カレント レコードはありません。</span><span class="sxs-lookup"><span data-stu-id="d8311-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="d8311-123">**MoveFirst** または **MoveLast** を使用したときに、最初のレコードまたは最後のレコードが既にカレント レコードである場合、カレント レコードは変更されません。</span><span class="sxs-lookup"><span data-stu-id="d8311-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="d8311-124">レコード セットは、テーブル タイプ**のレコード セット**(Microsoft Access ワークスペースのみ) を参照している場合の移動は現在のインデックスに従います。</span><span class="sxs-lookup"><span data-stu-id="d8311-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="d8311-125">現在のインデックスを設定するには、 **Index** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d8311-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="d8311-126">現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。</span><span class="sxs-lookup"><span data-stu-id="d8311-126">If you don't set the current index, the order of returned records is undefined.</span></span>

> [!NOTE]
> <span data-ttu-id="d8311-127">[!メモ] **MoveLast** メソッドを使用すると、ダイナセット タイプまたはスナップショット タイプの **Recordset** の末尾までデータを格納して、 **Recordset** に含まれる現在のレコード数を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="d8311-127">You can use the **MoveLast** method to fully populate a dynaset- or snapshot-type **Recordset** to provide the current number of records in the **Recordset**.</span></span> <span data-ttu-id="d8311-128">ただし、このような目的で **MoveLast** を使用すると、アプリケーションのパフォーマンスが低下する場合があります。</span><span class="sxs-lookup"><span data-stu-id="d8311-128">However, if you use **MoveLast** in this way, you can slow down your application's performance.</span></span> <span data-ttu-id="d8311-129">**MoveLast** を使用してレコード数を取得するのは、新しく開かれた **Recordset** の正確なレコード数をどうしても取得する必要がある場合だけにしてください。</span><span class="sxs-lookup"><span data-stu-id="d8311-129">You should only use **MoveLast** to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened **Recordset**.</span></span> 
>
> <span data-ttu-id="d8311-130">**MoveLast** で **dbRunAsync** 定数を使用すると、メソッドの呼び出しが非同期で実行されます。</span><span class="sxs-lookup"><span data-stu-id="d8311-130">If you use the **dbRunAsync** constant with **MoveLast**, the method call is asynchronous.</span></span> <span data-ttu-id="d8311-131">**Recordset** の末尾までデータが格納されたことを確認するには **StillExecuting** プロパティを使用し、 **MoveLast** メソッドに対する非同期呼び出しの実行を終了するには **Cancel** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d8311-131">You can use the **StillExecuting** property to determine when the **Recordset** is fully populated, and you can use the **Cancel** method to terminate execution of the asynchronous **MoveLast** method call.</span></span>

<span data-ttu-id="d8311-132">前方のみタイプの**Recordset**オブジェクトでは、 **MoveFirst**、 **MoveLast**、および**MovePrevious**メソッドを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="d8311-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="d8311-133">**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、 **Move** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d8311-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

