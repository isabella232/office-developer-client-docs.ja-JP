---
title: Recordset2.MovePrevious メソッド (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 8c433810-4b19-e7c1-3cee-a0bc50b23e8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197336(v=office.15)
ms:contentKeyID: 48546235
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9753d3bbb586e2c1bd44755deb529758d8eab060
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712891"
---
# <a name="recordset2moveprevious-method-dao"></a><span data-ttu-id="0d103-102">Recordset2.MovePrevious メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="0d103-102">Recordset2.MovePrevious method (DAO)</span></span>


<span data-ttu-id="0d103-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0d103-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d103-104">指定された **Recordset** オブジェクトの前のレコードに移動し、そのレコードをカレント レコードにします。</span><span class="sxs-lookup"><span data-stu-id="0d103-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d103-105">構文</span><span class="sxs-lookup"><span data-stu-id="0d103-105">Syntax</span></span>

<span data-ttu-id="0d103-106">*式*です。MovePrevious</span><span class="sxs-lookup"><span data-stu-id="0d103-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="0d103-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="0d103-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d103-108">注釈</span><span class="sxs-lookup"><span data-stu-id="0d103-108">Remarks</span></span>

<span data-ttu-id="0d103-109">**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。</span><span class="sxs-lookup"><span data-stu-id="0d103-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="0d103-p101">カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。</span><span class="sxs-lookup"><span data-stu-id="0d103-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="0d103-p102">**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合、 **BOF** プロパティは **True** で、カレント レコードはありません。</span><span class="sxs-lookup"><span data-stu-id="0d103-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="0d103-p103">最初のレコードがカレント レコードであるときに **MovePrevious** を使用すると、 **BOF** プロパティは **True** となり、カレント レコードはなくなります。 **MovePrevious** を再度使用すると、エラーが発生し、 **BOF** は **True** のままとなります。</span><span class="sxs-lookup"><span data-stu-id="0d103-p103">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record. If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="0d103-116">レコード セットは、テーブル タイプ**のレコード セット**(Microsoft Access ワークスペースのみ) を参照している場合の移動は現在のインデックスに従います。</span><span class="sxs-lookup"><span data-stu-id="0d103-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="0d103-117">現在のインデックスを設定するには、 **Index** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d103-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="0d103-118">現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。</span><span class="sxs-lookup"><span data-stu-id="0d103-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="0d103-119">前方のみタイプの**Recordset**オブジェクトでは、 **MoveFirst**、 **MoveLast**、および**MovePrevious**メソッドを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="0d103-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="0d103-120">**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、 **Move** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d103-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

