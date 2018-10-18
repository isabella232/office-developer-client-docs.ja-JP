---
title: Status プロパティ (ADO Recordset)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1979ad721a01ef72c08da1531a8826ec320915e5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604618"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="a4d10-102">Status プロパティ (ADO Recordset)</span><span class="sxs-lookup"><span data-stu-id="a4d10-102">Status Property (ADO Recordset)</span></span>


<span data-ttu-id="a4d10-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4d10-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a4d10-104">一括更新またはその他の一括操作に関して現在のレコードのステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="a4d10-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

<span data-ttu-id="a4d10-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="a4d10-105"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="a4d10-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="a4d10-106">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="a4d10-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="a4d10-107">Return value</span></span>
>>>>>>> <span data-ttu-id="a4d10-108">master</span><span class="sxs-lookup"><span data-stu-id="a4d10-108">master</span></span>

<span data-ttu-id="a4d10-109">[RecordStatusEnum](recordstatusenum.md) 値の合計を返します。</span><span class="sxs-lookup"><span data-stu-id="a4d10-109">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4d10-110">解説</span><span class="sxs-lookup"><span data-stu-id="a4d10-110">Remarks</span></span>

<span data-ttu-id="a4d10-p101">一括更新中に変更されたレコードの保留中の変更を調べるには、 **Status** プロパティを使用します。また、 **Status** プロパティを使用して、 [Recordset](resync-method-ado.md) オブジェクトで [Resync](updatebatch-method-ado.md) メソッド、 [UpdateBatch](cancelbatch-method-ado.md) メソッド、または [CancelBatch](recordset-object-ado.md) メソッドなどを呼び出したときや、 [Recordset](filter-property-ado.md) オブジェクトの **Filter** プロパティをブックマークの配列に設定したときのように、一括操作中に処理されなかったレコードの状態を確認することもできます。このプロパティを使用すると、特定のレコードが処理されなかった原因を調べて、問題を解決することができます。</span><span class="sxs-lookup"><span data-stu-id="a4d10-p101">Use the **Status** property to see what changes are pending for records modified during batch updating. You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks. With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

