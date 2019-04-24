---
title: フィールドに関連するエラー情報
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a0d0362b8f0ff9570a92a3c1c364061d1f9a584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292973"
---
# <a name="field-related-error-information"></a><span data-ttu-id="21e06-102">フィールドに関連するエラー情報</span><span class="sxs-lookup"><span data-stu-id="21e06-102">Field-related error information</span></span>


<span data-ttu-id="21e06-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="21e06-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21e06-p101">エラーがフィールドに直接関係するものである場合 (データが存在しない場合やデータがフィールドの型と一致しない場合など) は、 **Field** オブジェクトの **Status** プロパティを調べることで、問題の原因に関するより詳細な情報を得ることができます。このプロパティは、問題に関する具体的な情報を示すよう拡張されています。このため、たとえば **UpdateBatch** の呼び出しが失敗したときに、影響を受けた各レコードに含まれる **Field** の **Status** プロパティを調べることにより、問題の原因を確認できます。このプロパティには、 **FieldStatusEnum** 定数の値のうち 1 つが含まれます。エラー発生時に特に関係のある値を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="21e06-p101">If an error is directly related to a field — for example, if the data is missing or if it is the wrong type for the field — you can retrieve more information about the cause of the problem by examining the **Field** object's **Status** property. This property has been enhanced to provide specific information about the problem. So, for example, when a call to **UpdateBatch** fails, the cause of the problem can be determined by examining the **Status** property of the **Fields** in each of the effected records. The property will contain one of the values in the **FieldStatusEnum** constant. The following table includes those values that are of particular interest when an error occurs.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21e06-109">定数</span><span class="sxs-lookup"><span data-stu-id="21e06-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="21e06-110">値</span><span class="sxs-lookup"><span data-stu-id="21e06-110">Value</span></span></p></th>
<th><p><span data-ttu-id="21e06-111">説明</span><span class="sxs-lookup"><span data-stu-id="21e06-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21e06-112"><strong>adfieldcantconvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="21e06-112"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="21e06-113">pbm-2</span><span class="sxs-lookup"><span data-stu-id="21e06-113">2</span></span></p></td>
<td><p><span data-ttu-id="21e06-114">フィールドの取得または保存を行うときにデータが失われてしまうことを示します。</span><span class="sxs-lookup"><span data-stu-id="21e06-114">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e06-115"><strong>adfielddataoverflow</strong></span><span class="sxs-lookup"><span data-stu-id="21e06-115"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="21e06-116">シックス</span><span class="sxs-lookup"><span data-stu-id="21e06-116">6</span></span></p></td>
<td><p><span data-ttu-id="21e06-117">プロバイダーから返されたデータがフィールドのデータ型をオーバーフローしたことを示します。</span><span class="sxs-lookup"><span data-stu-id="21e06-117">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e06-118"><strong>adfielddefault</strong></span><span class="sxs-lookup"><span data-stu-id="21e06-118"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="21e06-119">スリー</span><span class="sxs-lookup"><span data-stu-id="21e06-119">13</span></span></p></td>
<td><p><span data-ttu-id="21e06-120">データの設定時にフィールドの既定値が使われたことを示します。</span><span class="sxs-lookup"><span data-stu-id="21e06-120">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e06-121"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="21e06-121"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="21e06-122">約</span><span class="sxs-lookup"><span data-stu-id="21e06-122">15</span></span></p></td>
<td><p><span data-ttu-id="21e06-p102">ソースのデータ値が設定されたときにこのフィールドがスキップされたことを示します。プロバイダーによって値が設定されていません。</span><span class="sxs-lookup"><span data-stu-id="21e06-p102">Indicates that this field was skipped when setting data values in the source. No value was set by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e06-125"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="21e06-125"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="21e06-126">個</span><span class="sxs-lookup"><span data-stu-id="21e06-126">10</span></span></p></td>
<td><p><span data-ttu-id="21e06-127">計算エンティティまたは派生エンティティであるため、フィールドを編集できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="21e06-127">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e06-128"><strong>ad' disnull</strong></span><span class="sxs-lookup"><span data-stu-id="21e06-128"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="21e06-129">1/3</span><span class="sxs-lookup"><span data-stu-id="21e06-129">3</span></span></p></td>
<td><p><span data-ttu-id="21e06-130">プロバイダーが Null 値を返したことを示します。</span><span class="sxs-lookup"><span data-stu-id="21e06-130">Indicates that the provider returned a null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e06-131"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="21e06-131"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="21e06-132">×</span><span class="sxs-lookup"><span data-stu-id="21e06-132">22</span></span></p></td>
<td><p><span data-ttu-id="21e06-133">移動またはコピー操作を実行するために必要な記憶域をプロバイダーが確保できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="21e06-133">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
</tbody>
</table>

