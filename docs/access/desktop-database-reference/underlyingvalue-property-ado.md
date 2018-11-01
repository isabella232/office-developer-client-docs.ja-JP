---
title: UnderlyingValue プロパティ (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d91dccb88ff39ad344ffa0e59e7ccdaaa9f1565
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867784"
---
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="8d593-102">UnderlyingValue プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="8d593-102">UnderlyingValue property (ADO)</span></span>


<span data-ttu-id="8d593-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8d593-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="8d593-104">データベース内の [Field](field-object-ado.md) オブジェクトの現在の値を示します。</span><span class="sxs-lookup"><span data-stu-id="8d593-104">Indicates a [Field](field-object-ado.md) object's current value in the database.</span></span>

## <a name="return-value"></a><span data-ttu-id="8d593-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="8d593-105">Return value</span></span>

<span data-ttu-id="8d593-106">**Field** の値を示すバリアント型 ( **Variant** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="8d593-106">Returns a **Variant** value that indicates the value of the **Field**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d593-107">解説</span><span class="sxs-lookup"><span data-stu-id="8d593-107">Remarks</span></span>

<span data-ttu-id="8d593-p101">データベースから現在のフィールド値を返すには、 **UnderlyingValue** プロパティを使用します。 **UnderlyingValue** プロパティ内のフィールド値は、トランザクションで参照できる値であり、別のトランザクションによる最近の更新の結果である可能性があります。この値は、 [Recordset](originalvalue-property-ado.md) に最初に返された値を反映する [OriginalValue](recordset-object-ado.md) プロパティとは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="8d593-p101">Use the **UnderlyingValue** property to return the current field value from the database. The field value in the **UnderlyingValue** property is the value that is visible to your transaction and may be the result of a recent update by another transaction. This may differ from the [OriginalValue](originalvalue-property-ado.md) property, which reflects the value that was originally returned to the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="8d593-p102">これは [Resync](resync-method-ado.md) メソッドを使用した場合と似ていますが、 **UnderlyingValue** プロパティは現在のレコードから特定のフィールドの値のみを返します。この値は、 [Resync](resync-method-ado.md) メソッドが [Value](value-property-ado.md) プロパティを置き換えるために使用する値と同じです。</span><span class="sxs-lookup"><span data-stu-id="8d593-p102">This is similar to using the [Resync](resync-method-ado.md) method, but the **UnderlyingValue** property returns only the value for a specific field from the current record. This is the same value that the [Resync](resync-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="8d593-113">このプロパティを **OriginalValue** プロパティと共に使用すると、一括更新で発生する競合を解消できます。</span><span class="sxs-lookup"><span data-stu-id="8d593-113">When you use this property with the **OriginalValue** property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="8d593-114">Record</span><span class="sxs-lookup"><span data-stu-id="8d593-114">Record</span></span>

<span data-ttu-id="8d593-115">[Record](record-object-ado.md) オブジェクトの場合、 [Update](update-method-ado.md) が呼び出される前に追加されたフィールドについては、このプロパティは空になります。</span><span class="sxs-lookup"><span data-stu-id="8d593-115">For [Record](record-object-ado.md) objects, this property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

