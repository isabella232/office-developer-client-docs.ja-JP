---
title: Recordset.MoveNext メソッド (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7675da7016044836bd2c8bf723ab6e1bc9a65b1b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477234"
---
# <a name="recordsetmovenext-method-dao"></a><span data-ttu-id="ff75b-102">Recordset.MoveNext メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="ff75b-102">Recordset.MoveNext Method (DAO)</span></span>


<span data-ttu-id="ff75b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff75b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ff75b-104">指定された **Recordset** オブジェクトの次のレコードに移動し、そのレコードをカレント レコードにします。</span><span class="sxs-lookup"><span data-stu-id="ff75b-104">Moves to the next record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff75b-105">構文</span><span class="sxs-lookup"><span data-stu-id="ff75b-105">Syntax</span></span>

<span data-ttu-id="ff75b-106">*式*です。MoveNext</span><span class="sxs-lookup"><span data-stu-id="ff75b-106">*expression* .MoveNext</span></span>

<span data-ttu-id="ff75b-107">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="ff75b-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff75b-108">注釈</span><span class="sxs-lookup"><span data-stu-id="ff75b-108">Remarks</span></span>

<span data-ttu-id="ff75b-109">**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。</span><span class="sxs-lookup"><span data-stu-id="ff75b-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="ff75b-p101">カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。</span><span class="sxs-lookup"><span data-stu-id="ff75b-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="ff75b-p102">**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合、 **BOF** プロパティは **True** で、カレント レコードはありません。</span><span class="sxs-lookup"><span data-stu-id="ff75b-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="ff75b-p103">最後のレコードがカレント レコードであるときに **MoveNext** を使用すると、 **EOF** プロパティは **True** となり、カレント レコードはなくなります。 **MoveNext** を再度使用すると、エラーが発生し、 **EOF** は **True** のままとなります。</span><span class="sxs-lookup"><span data-stu-id="ff75b-p103">If you use **MoveNext** when the last record is current, the **EOF** property is **True**, and there is no current record. If you use **MoveNext** again, an error occurs, and **EOF** remains **True**.</span></span>

<span data-ttu-id="ff75b-116">レコード セットは、テーブル タイプ**のレコード セット**(Microsoft Access ワークスペースのみ) を参照している場合の移動は現在のインデックスに従います。</span><span class="sxs-lookup"><span data-stu-id="ff75b-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="ff75b-117">現在のインデックスを設定するには、 **Index** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ff75b-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="ff75b-118">現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。</span><span class="sxs-lookup"><span data-stu-id="ff75b-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="ff75b-119">前方のみタイプの**Recordset**オブジェクトでは、 **MoveFirst**、 **MoveLast**、および**MovePrevious**メソッドを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="ff75b-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="ff75b-120">**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、 **Move** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ff75b-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

