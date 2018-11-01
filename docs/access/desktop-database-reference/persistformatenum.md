---
title: PersistFormatEnum (デスクトップ データベース参照のアクセス)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a1e980debebe6a38ed0c27eabba3abefcd8be152
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887153"
---
# <a name="persistformatenum"></a><span data-ttu-id="b9a7a-102">PersistFormatEnum</span><span class="sxs-lookup"><span data-stu-id="b9a7a-102">PersistFormatEnum</span></span>

<span data-ttu-id="b9a7a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b9a7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9a7a-104">[Recordset](recordset-object-ado.md) を保存するときの形式を表します。</span><span class="sxs-lookup"><span data-stu-id="b9a7a-104">Specifies the format in which to save a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9a7a-105">定数</span><span class="sxs-lookup"><span data-stu-id="b9a7a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b9a7a-106">値</span><span class="sxs-lookup"><span data-stu-id="b9a7a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b9a7a-107">説明</span><span class="sxs-lookup"><span data-stu-id="b9a7a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9a7a-108"><strong>adPersistADTG</strong></span><span class="sxs-lookup"><span data-stu-id="b9a7a-108"><strong>adPersistADTG</strong></span></span></p></td>
<td><p><span data-ttu-id="b9a7a-109">0</span><span class="sxs-lookup"><span data-stu-id="b9a7a-109">0</span></span></p></td>
<td><p><span data-ttu-id="b9a7a-110">Microsoft Advanced Data TableGram (ADTG) 形式であることを示します。</span><span class="sxs-lookup"><span data-stu-id="b9a7a-110">Indicates Microsoft Advanced Data TableGram (ADTG) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9a7a-111"><strong>adPersistADO</strong></span><span class="sxs-lookup"><span data-stu-id="b9a7a-111"><strong>adPersistADO</strong></span></span></p></td>
<td><p><span data-ttu-id="b9a7a-112">1</span><span class="sxs-lookup"><span data-stu-id="b9a7a-112">1</span></span></p></td>
<td><p><span data-ttu-id="b9a7a-p101">ADO 独自の拡張マークアップ言語 (XML) 形式が使用されることを示します。この値は adPersistXML と同じであり、以前のバージョンとの互換性は保たれます。</span><span class="sxs-lookup"><span data-stu-id="b9a7a-p101">Indicates that ADO's own Extensible Markup Language (XML) format will be used. This value is the same as adPersistXML and is included for backwards compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9a7a-115"><strong>adPersistXML</strong></span><span class="sxs-lookup"><span data-stu-id="b9a7a-115"><strong>adPersistXML</strong></span></span></p></td>
<td><p><span data-ttu-id="b9a7a-116">1</span><span class="sxs-lookup"><span data-stu-id="b9a7a-116">1</span></span></p></td>
<td><p><span data-ttu-id="b9a7a-117">拡張マークアップ言語 (XML) 形式であることを示します。</span><span class="sxs-lookup"><span data-stu-id="b9a7a-117">Indicates Extensible Markup Language (XML) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9a7a-118"><strong>adPersistProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="b9a7a-118"><strong>adPersistProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="b9a7a-119">2</span><span class="sxs-lookup"><span data-stu-id="b9a7a-119">2</span></span></p></td>
<td><p><span data-ttu-id="b9a7a-120">プロバイダーが独自の形式を使って <strong>Recordset</strong> を保持することを示します。</span><span class="sxs-lookup"><span data-stu-id="b9a7a-120">Indicates that the provider will persist the <strong>Recordset</strong> using its own format.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b9a7a-121">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="b9a7a-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="b9a7a-122">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b9a7a-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9a7a-123">定数</span><span class="sxs-lookup"><span data-stu-id="b9a7a-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9a7a-124">AdoEnums.PersistFormat.ADTG</span><span class="sxs-lookup"><span data-stu-id="b9a7a-124">AdoEnums.PersistFormat.ADTG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9a7a-125">AdoEnums.PersistFormat.XML</span><span class="sxs-lookup"><span data-stu-id="b9a7a-125">AdoEnums.PersistFormat.XML</span></span></p></td>
</tr>
</tbody>
</table>

