---
title: Type プロパティ (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 34a5d1cb1750dc9803c62202a06feccc2d464f9b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698254"
---
# <a name="type-property-ado"></a><span data-ttu-id="ef599-102">Type プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="ef599-102">Type property (ADO)</span></span>


<span data-ttu-id="ef599-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ef599-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef599-104">[Parameter](parameter-object-ado.md) オブジェクト、 [Field](field-object-ado.md) オブジェクト、または [Property](property-object-ado.md) オブジェクトの操作の種類またはデータ型を示します。</span><span class="sxs-lookup"><span data-stu-id="ef599-104">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ef599-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="ef599-105">Settings and return values</span></span>

<span data-ttu-id="ef599-106">[DataTypeEnum](datatypeenum.md) 値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ef599-106">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef599-107">解説</span><span class="sxs-lookup"><span data-stu-id="ef599-107">Remarks</span></span>

<span data-ttu-id="ef599-p101">**Parameter** オブジェクトの場合、 **Type** プロパティは値の取得および設定が可能です。 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されており、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合にのみ、 **Type** の値の設定および取得が可能になります。</span><span class="sxs-lookup"><span data-stu-id="ef599-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="ef599-110">その他のすべてのオブジェクトでは、 **Type** プロパティは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="ef599-110">For all other objects, the **Type** property is read-only.</span></span>

