---
title: Name プロパティ (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f6fbfbd7008919cc4d784a4d0468d8471d102708
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721548"
---
# <a name="name-property-ado"></a><span data-ttu-id="692c8-102">Name プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="692c8-102">Name property (ADO)</span></span>


<span data-ttu-id="692c8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="692c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="692c8-104">オブジェクトの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="692c8-104">Indicates the name of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="692c8-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="692c8-105">Settings and return values</span></span>

<span data-ttu-id="692c8-106">オブジェクトの名前を示す文字列型 ( **String** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="692c8-106">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="692c8-107">解説</span><span class="sxs-lookup"><span data-stu-id="692c8-107">Remarks</span></span>

<span data-ttu-id="692c8-108">**Name** プロパティは、 **Command** オブジェクト、 **Property** オブジェクト、 **Field** オブジェクト、または **Parameter** オブジェクトの名前を設定または取得するために使用します。</span><span class="sxs-lookup"><span data-stu-id="692c8-108">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="692c8-109">値は、 **Command** オブジェクトでは読み取り/書き込み可能で、 **Property** オブジェクトでは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="692c8-109">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="692c8-p101">**Field** オブジェクトの場合、 **Name** は一般には読み取り専用です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されていて、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合に限り、 **Name** は読み取り/書き込み可能になります。</span><span class="sxs-lookup"><span data-stu-id="692c8-p101">For a **Field** object, **Name** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="692c8-p102">**Parameters** コレクションに追加されていない [Parameter](parameters-collection-ado.md) オブジェクトでは、 **Name** プロパティは読み取り/書き込み可能です。追加された **Parameter** オブジェクトとその他のオブジェクトでは、 **Name** プロパティは読み取り専用です。名前はコレクション内で一意でなくてもかまいません。</span><span class="sxs-lookup"><span data-stu-id="692c8-p102">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write. For appended **Parameter** objects and all other objects, the **Name** property is read-only. Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="692c8-115">オブジェクトの **Name** は、序数参照で取得でき、その後は、その名前で直接オブジェクトを参照できます。</span><span class="sxs-lookup"><span data-stu-id="692c8-115">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="692c8-116">などの場合は rstMain.Properties(20) です。名には、更新機能が得られます、このプロパティは更新の結果が、後で参照できる、rstMain.Properties("Updatability") としてこのプロパティを後で参照できます。</span><span class="sxs-lookup"><span data-stu-id="692c8-116">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>

