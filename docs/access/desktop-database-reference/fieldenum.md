---
title: FieldEnum (デスクトップ データベース参照のアクセス)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5efcdbd9da4214d7f2b78ffbcfb81fb13265087e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476383"
---
# <a name="fieldenum"></a><span data-ttu-id="4c7de-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="4c7de-102">FieldEnum</span></span>


<span data-ttu-id="4c7de-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c7de-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4c7de-104">[Record](record-object-ado.md) オブジェクトの [Fields](fields-collection-ado.md) コレクションで参照される特定のフィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="4c7de-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

<span data-ttu-id="4c7de-105">**解説**</span><span class="sxs-lookup"><span data-stu-id="4c7de-105">**Remarks**</span></span>

<span data-ttu-id="4c7de-p101">これらの定数は、 **Record** に関連付けられた特定のフィールドにアクセスするための "ショートカット" として利用できます。 [Fields](field-object-ado.md) コレクションから **Field** オブジェクトを取得し、 **Field** オブジェクトの [Value](value-property-ado.md) プロパティを使用してその内容を取り出します。</span><span class="sxs-lookup"><span data-stu-id="4c7de-p101">These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c7de-108">定数</span><span class="sxs-lookup"><span data-stu-id="4c7de-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="4c7de-109">値</span><span class="sxs-lookup"><span data-stu-id="4c7de-109">Value</span></span></p></th>
<th><p><span data-ttu-id="4c7de-110">説明</span><span class="sxs-lookup"><span data-stu-id="4c7de-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c7de-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="4c7de-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="4c7de-112">-1</span><span class="sxs-lookup"><span data-stu-id="4c7de-112">-1</span></span></p></td>
<td><p><span data-ttu-id="4c7de-113"><strong>Record</strong> に関連付けられた既定の <a href="stream-object-ado.md">Stream</a> オブジェクトを含むフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="4c7de-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c7de-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="4c7de-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="4c7de-115">-2</span><span class="sxs-lookup"><span data-stu-id="4c7de-115">-2</span></span></p></td>
<td><p><span data-ttu-id="4c7de-116">現在の <strong>Record</strong> の絶対 URL 文字列を含むフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="4c7de-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

