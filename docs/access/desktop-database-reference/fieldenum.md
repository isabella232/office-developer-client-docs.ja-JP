---
title: FieldEnum (デスクトップ データベース参照のアクセス)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9ab46fc7c3817cbfa83c78816a42472e425d2d71
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860050"
---
# <a name="fieldenum"></a><span data-ttu-id="0723b-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="0723b-102">FieldEnum</span></span>

<span data-ttu-id="0723b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0723b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0723b-104">[Record](record-object-ado.md) オブジェクトの [Fields](fields-collection-ado.md) コレクションで参照される特定のフィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="0723b-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="0723b-105">備考</span><span class="sxs-lookup"><span data-stu-id="0723b-105">Remarks</span></span>

<span data-ttu-id="0723b-p101">これらの定数は、 **Record** に関連付けられた特定のフィールドにアクセスするための "ショートカット" として利用できます。 [Fields](field-object-ado.md) コレクションから **Field** オブジェクトを取得し、 **Field** オブジェクトの [Value](value-property-ado.md) プロパティを使用してその内容を取り出します。</span><span class="sxs-lookup"><span data-stu-id="0723b-p101">These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0723b-108">定数</span><span class="sxs-lookup"><span data-stu-id="0723b-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="0723b-109">値</span><span class="sxs-lookup"><span data-stu-id="0723b-109">Value</span></span></p></th>
<th><p><span data-ttu-id="0723b-110">説明</span><span class="sxs-lookup"><span data-stu-id="0723b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0723b-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="0723b-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="0723b-112">-1</span><span class="sxs-lookup"><span data-stu-id="0723b-112">-1</span></span></p></td>
<td><p><span data-ttu-id="0723b-113"><strong>Record</strong> に関連付けられた既定の <a href="stream-object-ado.md">Stream</a> オブジェクトを含むフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="0723b-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0723b-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="0723b-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="0723b-115">-2</span><span class="sxs-lookup"><span data-stu-id="0723b-115">-2</span></span></p></td>
<td><p><span data-ttu-id="0723b-116">現在の <strong>Record</strong> の絶対 URL 文字列を含むフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="0723b-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

