---
title: AbsolutePosition プロパティ (ADO)
TOCTitle: AbsolutePosition Property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3258ffcab87b16e4931c9881a8e8d1cd2143262f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479148"
---
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="23ed1-102">AbsolutePosition プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="23ed1-102">AbsolutePosition Property (ADO)</span></span>


<span data-ttu-id="23ed1-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="23ed1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="23ed1-104">[Recordset](recordset-object-ado.md) オブジェクト内のカレント レコードの位置を表す値を示します。</span><span class="sxs-lookup"><span data-stu-id="23ed1-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="23ed1-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="23ed1-105">Settings and Return Values</span></span>

<span data-ttu-id="23ed1-106">1 から **Recordset** オブジェクトのレコード数 ([RecordCount](recordcount-property-ado.md)) までの長整数型 (**Long**) の値を設定するか、または [PositionEnum](positionenum.md) 値の 1 つを取得します。</span><span class="sxs-lookup"><span data-stu-id="23ed1-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="23ed1-107">解説</span><span class="sxs-lookup"><span data-stu-id="23ed1-107">Remarks</span></span>

<span data-ttu-id="23ed1-108">ADO の **AbsolutePosition** プロパティを設定するには、使用する OLE DB プロバイダーが IRowsetLocate インターフェイスを実装している必要があります。</span><span class="sxs-lookup"><span data-stu-id="23ed1-108">In order to set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="23ed1-109">**AbsolutePosition**をアクセスするか、前方のみまたは動的カーソルで開かれた**レコード セット**のプロパティは、エラー **adErrFeatureNotAvailable**を発生します。</span><span class="sxs-lookup"><span data-stu-id="23ed1-109">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**.</span></span> <span data-ttu-id="23ed1-110">他のカーソル型では、プロバイダーが IRowsetScroll インターフェイスをサポートしている限り、正しい位置が返されます。</span><span class="sxs-lookup"><span data-stu-id="23ed1-110">With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface.</span></span> <span data-ttu-id="23ed1-111">プロバイダーが*IRowsetScroll*インターフェイスをサポートしていない場合、プロパティは**adPosUnknown**に設定します。</span><span class="sxs-lookup"><span data-stu-id="23ed1-111">If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**.</span></span> <span data-ttu-id="23ed1-112">*IRowsetScroll*をサポートしているかどうかは、プロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="23ed1-112">See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="23ed1-p102">**AbsolutePosition** プロパティを使用すると、 **Recordset** オブジェクトでのレコードの順序位置に基づいて特定のレコードに移動したり、カレント レコードの順序位置を調べたりできます。このプロパティを使用するには、プロバイダーが必要な機能をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="23ed1-p102">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="23ed1-p103">[AbsolutePosition](absolutepage-property-ado.md) は、 **AbsolutePage** プロパティと同じく 1 から始まる値で、 **Recordset** の先頭レコードがカレント レコードの場合に 1 になります。 **Recordset** オブジェクトのレコード総数は、 [RecordCount](recordcount-property-ado.md) プロパティから取得できます。</span><span class="sxs-lookup"><span data-stu-id="23ed1-p103">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="23ed1-p104">**AbsolutePosition** プロパティを設定すると、たとえ現在のキャッシュ内のレコードに設定した場合でも、ADO は指定されたレコードから始まる新しいレコード群をキャッシュに再読み込みします。読み込まれるレコード数は、 [CacheSize](cachesize-property-ado.md) プロパティにより決まります。</span><span class="sxs-lookup"><span data-stu-id="23ed1-p104">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="23ed1-p105">[!メモ] <STRONG>AbsolutePosition</STRONG> プロパティをレコード番号の代わりに使用しないでください。レコードの位置は、それより前のレコードが削除されると変わります。また、 <STRONG>Recordset</STRONG> オブジェクトを照会し直したり、開き直したりした場合、同じレコードの <STRONG>AbsolutePosition</STRONG> が以前と同じになる保証はありません。ブックマークが、特定の位置を保持してその位置に戻るための推奨手段であり、すべての種類の <STRONG>Recordset</STRONG> オブジェクトで位置を指定するための唯一の手段です。</span><span class="sxs-lookup"><span data-stu-id="23ed1-p105">You should not use the <STRONG>AbsolutePosition</STRONG> property as a surrogate record number. The position of a given record changes when you delete a preceding record. There is also no assurance that a given record will have the same <STRONG>AbsolutePosition</STRONG> if the <STRONG>Recordset</STRONG> object is requeried or reopened. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <STRONG>Recordset</STRONG> objects.</span></span></P>


