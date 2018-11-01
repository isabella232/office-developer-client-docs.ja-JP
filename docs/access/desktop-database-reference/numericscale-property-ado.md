---
title: NumericScale プロパティ (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb2c799fd7c9d1cc74c6081c10f7a8d356e79faf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876016"
---
# <a name="numericscale-property-ado"></a><span data-ttu-id="8868e-102">NumericScale プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="8868e-102">NumericScale property (ADO)</span></span>


<span data-ttu-id="8868e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8868e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8868e-104">[Parameter](parameter-object-ado.md) オブジェクトまたは [Field](field-object-ado.md) オブジェクトの数値の桁数を示します。</span><span class="sxs-lookup"><span data-stu-id="8868e-104">Indicates the scale of numeric values in a [Parameter](parameter-object-ado.md) or [Field](field-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8868e-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="8868e-105">Settings and return values</span></span>

<span data-ttu-id="8868e-106">数値の小数点以下の桁数を示すバイト型 ( **Byte** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="8868e-106">Sets or returns a **Byte** value that indicates the number of decimal places to which numeric values will be resolved.</span></span>

## <a name="remarks"></a><span data-ttu-id="8868e-107">解説</span><span class="sxs-lookup"><span data-stu-id="8868e-107">Remarks</span></span>

<span data-ttu-id="8868e-108">**NumericScale** プロパティは、数値型の **Parameter** オブジェクトまたは **Field** オブジェクトの値の小数点以下の桁数を取得するために使用します。</span><span class="sxs-lookup"><span data-stu-id="8868e-108">Use the **NumericScale** property to determine how many digits to the right of the decimal point will be used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="8868e-109">**Parameter** オブジェクトでは、 **NumericScale** は読み取り/書き込み可能です。</span><span class="sxs-lookup"><span data-stu-id="8868e-109">For **Parameter** objects, the **NumericScale** property is read/write.</span></span>

<span data-ttu-id="8868e-p101">**Field** オブジェクトの場合、 **NumericScale** は一般には読み取り専用です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されていて、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合に限り、 **NumericScale** は読み取り/書き込み可能になります。</span><span class="sxs-lookup"><span data-stu-id="8868e-p101">For a **Field** object, **NumericScale** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **NumericScale** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

