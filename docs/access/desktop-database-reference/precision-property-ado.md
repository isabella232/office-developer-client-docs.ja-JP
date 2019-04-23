---
title: Precision プロパティ (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 662e5e9287da1ccfb81c727f5d5e5dfedce2969b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287476"
---
# <a name="precision-property-ado"></a><span data-ttu-id="01d59-102">Precision プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="01d59-102">Precision property (ADO)</span></span>


<span data-ttu-id="01d59-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="01d59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01d59-104">[Parameter](parameter-object-ado.md) オブジェクト内の数値または数値型の [Field](field-object-ado.md) オブジェクトの精度を示します。</span><span class="sxs-lookup"><span data-stu-id="01d59-104">Indicates the degree of precision for numeric values in a [Parameter](parameter-object-ado.md) object or for numeric [Field](field-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="01d59-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="01d59-105">Settings and return values</span></span>

<span data-ttu-id="01d59-106">値を表すために使用する最大桁数を示すバイト型 (**Byte**) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="01d59-106">Sets or returns a **Byte** value that indicates the maximum number of digits used to represent values.</span></span>

## <a name="remarks"></a><span data-ttu-id="01d59-107">注釈</span><span class="sxs-lookup"><span data-stu-id="01d59-107">Remarks</span></span>

<span data-ttu-id="01d59-108">数値型の **Parameter** オブジェクトまたは **Field** オブジェクトの値を表すために使用する最大桁数を調べるには、**Precision** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="01d59-108">Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="01d59-109">**Parameter** オブジェクトでは、値の設定および取得が可能です。</span><span class="sxs-lookup"><span data-stu-id="01d59-109">The value is read/write on a **Parameter** object.</span></span>

<span data-ttu-id="01d59-p101">**Field** オブジェクトの場合は、 **Precision** は通常、値の取得のみ可能です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されており、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合にのみ、 **Precision** の値の設定および取得が可能になります。</span><span class="sxs-lookup"><span data-stu-id="01d59-p101">For a **Field** object, **Precision** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Precision** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

