---
title: Recordset2.MoveFirst メソッド (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 74b186d0-8f6a-d136-a563-04f58d67b122
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195879(v=office.15)
ms:contentKeyID: 48545667
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 580ea981653eec3a1997b2c48376448032cd0fa2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883863"
---
# <a name="recordset2movefirst-method-dao"></a><span data-ttu-id="9ca5b-102">Recordset2.MoveFirst メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="9ca5b-102">Recordset2.MoveFirst Method (DAO)</span></span>


<span data-ttu-id="9ca5b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ca5b-104">指定した **Recordset** オブジェクトの最初のレコードに移動して、そのレコードをカレント レコードにします。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-104">Moves to the first record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca5b-105">構文</span><span class="sxs-lookup"><span data-stu-id="9ca5b-105">Syntax</span></span>

<span data-ttu-id="9ca5b-106">*式*です。MoveFirst</span><span class="sxs-lookup"><span data-stu-id="9ca5b-106">*expression* .MoveFirst</span></span>

<span data-ttu-id="9ca5b-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca5b-108">注釈</span><span class="sxs-lookup"><span data-stu-id="9ca5b-108">Remarks</span></span>

<span data-ttu-id="9ca5b-109">**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="9ca5b-p101">カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="9ca5b-p102">**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合、 **BOF** プロパティは **True** で、カレント レコードはありません。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="9ca5b-114">**MoveFirst** または **MoveLast** を使用したときに、最初のレコードまたは最後のレコードが既にカレント レコードである場合、カレント レコードは変更されません。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-114">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="9ca5b-115">レコード セットは、テーブル タイプ**のレコード セット**(Microsoft Access ワークスペースのみ) を参照している場合の移動は現在のインデックスに従います。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-115">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="9ca5b-116">現在のインデックスを設定するには、 **Index** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-116">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="9ca5b-117">現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-117">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="9ca5b-118">前方のみタイプの**Recordset**オブジェクトでは、 **MoveFirst**、 **MoveLast**、および**MovePrevious**メソッドを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-118">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="9ca5b-119">**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、 **Move** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9ca5b-119">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

