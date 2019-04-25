---
title: Recordset.MoveFirst メソッド (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 338f7e86-6997-b80a-fc7a-a395d10b4a62
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192329(v=office.15)
ms:contentKeyID: 48544109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 31d003d7ae98bf509aca8f24da9c37f0276af6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300239"
---
# <a name="recordsetmovefirst-method-dao"></a><span data-ttu-id="26c74-102">Recordset.MoveFirst メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="26c74-102">Recordset.MoveFirst Method (DAO)</span></span>


<span data-ttu-id="26c74-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="26c74-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26c74-104">指定した **Recordset** オブジェクトの最初のレコードに移動して、そのレコードをカレント レコードにします。</span><span class="sxs-lookup"><span data-stu-id="26c74-104">Moves to the first record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c74-105">構文</span><span class="sxs-lookup"><span data-stu-id="26c74-105">Syntax</span></span>

<span data-ttu-id="26c74-106">*式* .MoveFirst</span><span class="sxs-lookup"><span data-stu-id="26c74-106">expression  . MoveFirst</span></span>

<span data-ttu-id="26c74-107">*式* **Recordset** オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="26c74-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="26c74-108">注釈</span><span class="sxs-lookup"><span data-stu-id="26c74-108">Remarks</span></span>

<span data-ttu-id="26c74-109">
            \*\*Move\*\* メソッドは、条件を適用せずにレコード間を移動するために使用します。</span><span class="sxs-lookup"><span data-stu-id="26c74-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="26c74-p101">カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。</span><span class="sxs-lookup"><span data-stu-id="26c74-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="26c74-p102">
            \*\*Recordset\*\* を開いた時点では、最初のレコードがカレント レコードで、**BOF\*\* プロパティは *\*False\*\* です。\*\*Recordset\*\* にレコードが含まれていない場合、**BOF\*\* プロパティは \*\*True\*\* で、カレント レコードはありません。</span><span class="sxs-lookup"><span data-stu-id="26c74-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="26c74-114">
            \*\*MoveFirst\*\* または \*\*MoveLast\*\* を使用したときに、最初のレコードまたは最後のレコードが既にカレント レコードである場合、カレント レコードは変更されません。</span><span class="sxs-lookup"><span data-stu-id="26c74-114">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="26c74-115">recordset がテーブル タイプの **Recordset** である場合 (Microsoft Access ワークスペースのみ)、現在のインデックスに従って移動が行われます。</span><span class="sxs-lookup"><span data-stu-id="26c74-115">If  recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="26c74-116">現在のインデックスを設定するには、 **Index** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="26c74-116">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="26c74-117">現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。</span><span class="sxs-lookup"><span data-stu-id="26c74-117">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="26c74-118">
            **MoveFirst*\*、\*\*MoveLast\*\*、および **MovePrevious\*\* の各メソッドは、前方スクロール タイプの \*\*Recordset\*\* オブジェクトでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="26c74-118">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="26c74-119">
            \*\*Recordset\*\* オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、\*\*Move** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="26c74-119">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

