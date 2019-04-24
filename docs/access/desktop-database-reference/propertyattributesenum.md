---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c929bcf5dc7f5267c2e7d3a8dac5ed6bfb55b20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302878"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="fe6f6-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="fe6f6-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="fe6f6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe6f6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe6f6-104">[Property](property-object-ado.md) オブジェクトの属性を表します。</span><span class="sxs-lookup"><span data-stu-id="fe6f6-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe6f6-105">定数</span><span class="sxs-lookup"><span data-stu-id="fe6f6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="fe6f6-106">値</span><span class="sxs-lookup"><span data-stu-id="fe6f6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fe6f6-107">説明</span><span class="sxs-lookup"><span data-stu-id="fe6f6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="fe6f6-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6f6-109">.0</span><span class="sxs-lookup"><span data-stu-id="fe6f6-109">0</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-110">プロバイダーがプロパティをサポートしていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="fe6f6-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6f6-111"><strong>adproprequired</strong></span><span class="sxs-lookup"><span data-stu-id="fe6f6-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6f6-112">1-d</span><span class="sxs-lookup"><span data-stu-id="fe6f6-112">1</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-113">データ ソースを初期化するには、ユーザーがこのプロパティ値を指定する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="fe6f6-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-114"><strong>adpropoptional すべて</strong></span><span class="sxs-lookup"><span data-stu-id="fe6f6-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6f6-115">pbm-2</span><span class="sxs-lookup"><span data-stu-id="fe6f6-115">2</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-116">ユーザーがこのプロパティ値を指定しなくてもデータ ソースを初期化できることを表します。</span><span class="sxs-lookup"><span data-stu-id="fe6f6-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6f6-117"><strong>adpropread</strong></span><span class="sxs-lookup"><span data-stu-id="fe6f6-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6f6-118">512</span><span class="sxs-lookup"><span data-stu-id="fe6f6-118">512</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-119">ユーザーがプロパティを読み取り可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="fe6f6-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-120"><strong>adpropwrite</strong></span><span class="sxs-lookup"><span data-stu-id="fe6f6-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6f6-121">1024</span><span class="sxs-lookup"><span data-stu-id="fe6f6-121">1024</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-122">ユーザーがプロパティを設定できることを示します。</span><span class="sxs-lookup"><span data-stu-id="fe6f6-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="fe6f6-123">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="fe6f6-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="fe6f6-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="fe6f6-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe6f6-125">定数</span><span class="sxs-lookup"><span data-stu-id="fe6f6-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-126">AdoEnums NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="fe6f6-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6f6-127">AdoEnums 属性。必須</span><span class="sxs-lookup"><span data-stu-id="fe6f6-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-128">AdoEnums 属性。省略可能</span><span class="sxs-lookup"><span data-stu-id="fe6f6-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6f6-129">AdoEnums 属性を取得します。</span><span class="sxs-lookup"><span data-stu-id="fe6f6-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-130">AdoEnums の作成</span><span class="sxs-lookup"><span data-stu-id="fe6f6-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

