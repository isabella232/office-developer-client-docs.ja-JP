---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2567d07ad33670fcd68be4513d7a409ffdcd599c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864047"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="89b01-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="89b01-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="89b01-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="89b01-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="89b01-104">[Property](property-object-ado.md) オブジェクトの属性を表します。</span><span class="sxs-lookup"><span data-stu-id="89b01-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89b01-105">定数</span><span class="sxs-lookup"><span data-stu-id="89b01-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="89b01-106">値</span><span class="sxs-lookup"><span data-stu-id="89b01-106">Value</span></span></p></th>
<th><p><span data-ttu-id="89b01-107">説明</span><span class="sxs-lookup"><span data-stu-id="89b01-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89b01-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="89b01-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="89b01-109">0</span><span class="sxs-lookup"><span data-stu-id="89b01-109">0</span></span></p></td>
<td><p><span data-ttu-id="89b01-110">プロバイダーがプロパティをサポートしていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="89b01-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89b01-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="89b01-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="89b01-112">1</span><span class="sxs-lookup"><span data-stu-id="89b01-112">1</span></span></p></td>
<td><p><span data-ttu-id="89b01-113">データ ソースを初期化するには、ユーザーがこのプロパティ値を指定する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="89b01-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89b01-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="89b01-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="89b01-115">2</span><span class="sxs-lookup"><span data-stu-id="89b01-115">2</span></span></p></td>
<td><p><span data-ttu-id="89b01-116">ユーザーがこのプロパティ値を指定しなくてもデータ ソースを初期化できることを表します。</span><span class="sxs-lookup"><span data-stu-id="89b01-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89b01-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="89b01-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="89b01-118">512</span><span class="sxs-lookup"><span data-stu-id="89b01-118">512</span></span></p></td>
<td><p><span data-ttu-id="89b01-119">ユーザーがプロパティを読み取り可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="89b01-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89b01-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="89b01-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="89b01-121">1024</span><span class="sxs-lookup"><span data-stu-id="89b01-121">1024</span></span></p></td>
<td><p><span data-ttu-id="89b01-122">ユーザーがプロパティを設定できることを示します。</span><span class="sxs-lookup"><span data-stu-id="89b01-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="89b01-123">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="89b01-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="89b01-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="89b01-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89b01-125">定数</span><span class="sxs-lookup"><span data-stu-id="89b01-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89b01-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="89b01-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89b01-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="89b01-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89b01-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="89b01-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89b01-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="89b01-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89b01-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="89b01-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

