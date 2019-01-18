---
title: FieldEnum (デスクトップ データベース参照のアクセス)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e42dcfe63194364986e5b235c59b011231307a7c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726086"
---
# <a name="fieldenum"></a><span data-ttu-id="6d1d4-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="6d1d4-102">FieldEnum</span></span>

<span data-ttu-id="6d1d4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6d1d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d1d4-104">[Record](record-object-ado.md) オブジェクトの [Fields](fields-collection-ado.md) コレクションで参照される特定のフィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="6d1d4-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d1d4-105">注釈</span><span class="sxs-lookup"><span data-stu-id="6d1d4-105">Remarks</span></span>

<span data-ttu-id="6d1d4-p101">これらの定数は、 **Record** に関連付けられた特定のフィールドにアクセスするための "ショートカット" として利用できます。 [Fields](field-object-ado.md) コレクションから **Field** オブジェクトを取得し、 **Field** オブジェクトの [Value](value-property-ado.md) プロパティを使用してその内容を取り出します。</span><span class="sxs-lookup"><span data-stu-id="6d1d4-p101">These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d1d4-108">定数</span><span class="sxs-lookup"><span data-stu-id="6d1d4-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="6d1d4-109">値</span><span class="sxs-lookup"><span data-stu-id="6d1d4-109">Value</span></span></p></th>
<th><p><span data-ttu-id="6d1d4-110">説明</span><span class="sxs-lookup"><span data-stu-id="6d1d4-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d1d4-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="6d1d4-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="6d1d4-112">-1</span><span class="sxs-lookup"><span data-stu-id="6d1d4-112">-1</span></span></p></td>
<td><p><span data-ttu-id="6d1d4-113"><strong>Record</strong> に関連付けられた既定の <a href="stream-object-ado.md">Stream</a> オブジェクトを含むフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="6d1d4-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1d4-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="6d1d4-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="6d1d4-115">-2</span><span class="sxs-lookup"><span data-stu-id="6d1d4-115">-2</span></span></p></td>
<td><p><span data-ttu-id="6d1d4-116">現在の <strong>Record</strong> の絶対 URL 文字列を含むフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="6d1d4-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

