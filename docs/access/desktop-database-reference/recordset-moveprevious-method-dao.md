---
title: Recordset.MovePrevious メソッド (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 82a3bc3e-5221-9a1a-1350-47bc6759edeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196699(v=office.15)
ms:contentKeyID: 48545984
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052872
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2ee7bff8a5b7d17b714c4a52eff2eca5906c7135
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919872"
---
# <a name="recordsetmoveprevious-method-dao"></a><span data-ttu-id="2d258-102">Recordset.MovePrevious メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="2d258-102">Recordset.MovePrevious method (DAO)</span></span>


<span data-ttu-id="2d258-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2d258-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d258-104">指定された **Recordset** オブジェクトの前のレコードに移動し、そのレコードをカレント レコードにします。</span><span class="sxs-lookup"><span data-stu-id="2d258-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d258-105">構文</span><span class="sxs-lookup"><span data-stu-id="2d258-105">Syntax</span></span>

<span data-ttu-id="2d258-106">*式*です。MovePrevious</span><span class="sxs-lookup"><span data-stu-id="2d258-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="2d258-107">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="2d258-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d258-108">注釈</span><span class="sxs-lookup"><span data-stu-id="2d258-108">Remarks</span></span>

<span data-ttu-id="2d258-109">**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。</span><span class="sxs-lookup"><span data-stu-id="2d258-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="2d258-p101">カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。</span><span class="sxs-lookup"><span data-stu-id="2d258-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="2d258-p102">**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合、 **BOF** プロパティは **True** で、カレント レコードはありません。</span><span class="sxs-lookup"><span data-stu-id="2d258-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="2d258-p103">最初のレコードがカレント レコードであるときに **MovePrevious** を使用すると、 **BOF** プロパティは **True** となり、カレント レコードはなくなります。 **MovePrevious** を再度使用すると、エラーが発生し、 **BOF** は **True** のままとなります。</span><span class="sxs-lookup"><span data-stu-id="2d258-p103">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record. If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="2d258-116">レコード セットは、テーブル タイプ**のレコード セット**(Microsoft Access ワークスペースのみ) を参照している場合の移動は現在のインデックスに従います。</span><span class="sxs-lookup"><span data-stu-id="2d258-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="2d258-117">現在のインデックスを設定するには、 **Index** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="2d258-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="2d258-118">現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。</span><span class="sxs-lookup"><span data-stu-id="2d258-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="2d258-119">前方のみタイプの**Recordset**オブジェクトでは、 **MoveFirst**、 **MoveLast**、および**MovePrevious**メソッドを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="2d258-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="2d258-120">**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、 **Move** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2d258-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

