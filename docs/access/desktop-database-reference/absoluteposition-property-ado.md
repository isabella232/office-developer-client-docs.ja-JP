---
title: AbsolutePosition プロパティ (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b5e25e014c6e93d35e3621bb9b5b3c21d5e77f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281978"
---
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="dae13-102">AbsolutePosition プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="dae13-102">AbsolutePosition property (ADO)</span></span>

<span data-ttu-id="dae13-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="dae13-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dae13-104">[Recordset](recordset-object-ado.md) オブジェクト内のカレント レコードの位置を表す値を示します。</span><span class="sxs-lookup"><span data-stu-id="dae13-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="dae13-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="dae13-105">Settings and return values</span></span>

<span data-ttu-id="dae13-106">1 から **Recordset** オブジェクトのレコード数 ([RecordCount](recordcount-property-ado.md)) までの長整数型 (**Long**) の値を設定するか、または [PositionEnum](positionenum.md) 値の 1 つを取得します。</span><span class="sxs-lookup"><span data-stu-id="dae13-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="dae13-107">注釈</span><span class="sxs-lookup"><span data-stu-id="dae13-107">Remarks</span></span>

<span data-ttu-id="dae13-108">ADO で**AbsolutePosition**プロパティを設定するには、使用する OLE DB プロバイダーが IRowsetLocate インターフェイスを実装している必要があります。</span><span class="sxs-lookup"><span data-stu-id="dae13-108">To set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="dae13-109">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**.</span><span class="sxs-lookup"><span data-stu-id="dae13-109">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**.</span></span> <span data-ttu-id="dae13-110">With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface.</span><span class="sxs-lookup"><span data-stu-id="dae13-110">With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface.</span></span> <span data-ttu-id="dae13-111">プロバイダーが*IRowsetScroll*インターフェイスをサポートしていない場合、このプロパティは**adposunknown**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="dae13-111">If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**.</span></span> <span data-ttu-id="dae13-112">*IRowsetScroll*をサポートしているかどうかについては、プロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dae13-112">See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="dae13-p102">**AbsolutePosition** プロパティを使用すると、 **Recordset** オブジェクトでのレコードの順序位置に基づいて特定のレコードに移動したり、カレント レコードの順序位置を調べたりできます。このプロパティを使用するには、プロバイダーが必要な機能をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="dae13-p102">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="dae13-p103">[AbsolutePosition](absolutepage-property-ado.md) は、 **AbsolutePage** プロパティと同じく 1 から始まる値で、 **Recordset** の先頭レコードがカレント レコードの場合に 1 になります。 **Recordset** オブジェクトのレコード総数は、 [RecordCount](recordcount-property-ado.md) プロパティから取得できます。</span><span class="sxs-lookup"><span data-stu-id="dae13-p103">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="dae13-117">**AbsolutePosition**プロパティを設定すると、現在のキャッシュ内のレコードに設定されている場合でも、ADO は指定されたレコードから始まる新しいレコードグループをキャッシュに再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="dae13-117">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record that you specified.</span></span> <span data-ttu-id="dae13-118">[CacheSize](cachesize-property-ado.md) プロパティにより、このグループのサイズが決定されます。</span><span class="sxs-lookup"><span data-stu-id="dae13-118">The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <span data-ttu-id="dae13-119">[!メモ] 代替レコード番号として **AbsolutePosition** プロパティを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="dae13-119">You should not use the **AbsolutePosition** property as a surrogate record number.</span></span> <span data-ttu-id="dae13-120">レコードの位置は、それより前のレコードが削除されると変わります。</span><span class="sxs-lookup"><span data-stu-id="dae13-120">The position of a given record changes when you delete a preceding record.</span></span> <span data-ttu-id="dae13-121">また、 **Recordset** オブジェクトを照会し直したり、開き直したりした場合、同じレコードの **AbsolutePosition** が以前と同じになる保証はありません。</span><span class="sxs-lookup"><span data-stu-id="dae13-121">There is also no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened.</span></span> <span data-ttu-id="dae13-122">ブックマークは、特定の位置を保持してその位置に戻るための推奨手段であり、すべての種類の**Recordset**オブジェクトで位置を指定するための唯一の方法です。</span><span class="sxs-lookup"><span data-stu-id="dae13-122">Bookmarks are still the recommended way of retaining and returning to a given position, and are the only way of positioning across all types of **Recordset** objects.</span></span>


