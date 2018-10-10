---
title: レコードセットを配置する
TOCTitle: Recordset Positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10586c711b9931c1cac93401111f4d477ca8a987
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479323"
---
# <a name="recordset-positioning"></a><span data-ttu-id="6a76d-102">レコードセットを配置する</span><span class="sxs-lookup"><span data-stu-id="6a76d-102">Recordset Positioning</span></span>


<span data-ttu-id="6a76d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a76d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6a76d-p101">**Recordset** オブジェクト内での、順序に基づくレコードの移動、および現在のレコードの順序の確認には、 **AbsolutePosition** プロパティを使用します。このプロパティを使用するには、プロバイダーで該当する機能がサポートされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a76d-p101">Use the **AbsolutePosition** property to move to a record, based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="6a76d-p102">**AbsolutePosition** は 1 から始まり、現在のレコードが **Recordset** 内の最初のレコードの場合は、値が 1 になります。前に説明したように、 **Recordset** オブジェクト内のレコードの合計数は、 **RecordCount** プロパティで取得できます。</span><span class="sxs-lookup"><span data-stu-id="6a76d-p102">**AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. As mentioned previously, you can obtain the total number of records in the **Recordset** object from the **RecordCount** property.</span></span>

<span data-ttu-id="6a76d-p103">**AbsolutePosition** プロパティを設定すると、現在のキャッシュに存在するレコードが対象であっても、指定したレコードで始まる新しいレコード グループがキャッシュに再読み込みされます。 **CacheSize** プロパティにより、このグループのサイズが決定されます。</span><span class="sxs-lookup"><span data-stu-id="6a76d-p103">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The **CacheSize** property determines the size of this group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6a76d-p104">[!メモ] 代替レコード番号として <STRONG>AbsolutePosition</STRONG> プロパティを使用することはできません。特定のレコードの位置は、前のレコードを削除すると変更されます。また、 <STRONG>Recordset</STRONG> オブジェクトを再クエリした場合、または再び開いた場合は、特定のレコードの <STRONG>AbsolutePosition</STRONG> が同じ値になるとは限りません。特定の位置を保持し、その位置に戻るためにお勧めする方法、そしてすべての種類の <STRONG>Recordset</STRONG> オブジェクトで位置を決定できる唯一の方法は、ブックマークを使用することです。</span><span class="sxs-lookup"><span data-stu-id="6a76d-p104">You should not use the <STRONG>AbsolutePosition</STRONG> property as a surrogate record number. The position of a given record changes when you delete a preceding record. There also is no assurance that a given record will have the same <STRONG>AbsolutePosition</STRONG> if the <STRONG>Recordset</STRONG> object is requeried or reopened. Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <STRONG>Recordset</STRONG> objects.</span></span></P>


