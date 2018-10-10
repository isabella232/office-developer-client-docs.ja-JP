---
title: Type プロパティ (ADO)
TOCTitle: Type Property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ac119b9582634e619455870c8a2e115f5e8dafa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477115"
---
# <a name="type-property-ado"></a><span data-ttu-id="cfcfc-102">Type プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="cfcfc-102">Type Property (ADO)</span></span>


<span data-ttu-id="cfcfc-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfcfc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cfcfc-104">[Parameter](parameter-object-ado.md) オブジェクト、 [Field](field-object-ado.md) オブジェクト、または [Property](property-object-ado.md) オブジェクトの操作の種類またはデータ型を示します。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-104">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="cfcfc-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="cfcfc-105">Settings and Return Values</span></span>

<span data-ttu-id="cfcfc-106">[DataTypeEnum](datatypeenum.md) 値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-106">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfcfc-107">解説</span><span class="sxs-lookup"><span data-stu-id="cfcfc-107">Remarks</span></span>

<span data-ttu-id="cfcfc-p101">**Parameter** オブジェクトの場合、 **Type** プロパティは値の取得および設定が可能です。 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されており、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合にのみ、 **Type** の値の設定および取得が可能になります。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="cfcfc-110">その他のすべてのオブジェクトでは、 **Type** プロパティは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-110">For all other objects, the **Type** property is read-only.</span></span>

