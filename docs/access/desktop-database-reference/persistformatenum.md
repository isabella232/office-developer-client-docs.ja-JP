---
title: PersistFormatEnum (デスクトップ データベース参照のアクセス)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3254d60c6daa032857227b1f16f9a9c085164dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477429"
---
# <a name="persistformatenum"></a><span data-ttu-id="be795-102">PersistFormatEnum</span><span class="sxs-lookup"><span data-stu-id="be795-102">PersistFormatEnum</span></span>


<span data-ttu-id="be795-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="be795-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="be795-104">[Recordset](recordset-object-ado.md) を保存するときの形式を表します。</span><span class="sxs-lookup"><span data-stu-id="be795-104">Specifies the format in which to save a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be795-105">定数</span><span class="sxs-lookup"><span data-stu-id="be795-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="be795-106">値</span><span class="sxs-lookup"><span data-stu-id="be795-106">Value</span></span></p></th>
<th><p><span data-ttu-id="be795-107">説明</span><span class="sxs-lookup"><span data-stu-id="be795-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be795-108"><strong>adPersistADTG</strong></span><span class="sxs-lookup"><span data-stu-id="be795-108"><strong>adPersistADTG</strong></span></span></p></td>
<td><p><span data-ttu-id="be795-109">0</span><span class="sxs-lookup"><span data-stu-id="be795-109">0</span></span></p></td>
<td><p><span data-ttu-id="be795-110">Microsoft Advanced Data TableGram (ADTG) 形式であることを示します。</span><span class="sxs-lookup"><span data-stu-id="be795-110">Indicates Microsoft Advanced Data TableGram (ADTG) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be795-111"><strong>adPersistADO</strong></span><span class="sxs-lookup"><span data-stu-id="be795-111"><strong>adPersistADO</strong></span></span></p></td>
<td><p><span data-ttu-id="be795-112">1</span><span class="sxs-lookup"><span data-stu-id="be795-112">1</span></span></p></td>
<td><p><span data-ttu-id="be795-p101">ADO 独自の拡張マークアップ言語 (XML) 形式が使用されることを示します。この値は adPersistXML と同じであり、以前のバージョンとの互換性は保たれます。</span><span class="sxs-lookup"><span data-stu-id="be795-p101">Indicates that ADO's own Extensible Markup Language (XML) format will be used. This value is the same as adPersistXML and is included for backwards compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be795-115"><strong>adPersistXML</strong></span><span class="sxs-lookup"><span data-stu-id="be795-115"><strong>adPersistXML</strong></span></span></p></td>
<td><p><span data-ttu-id="be795-116">1</span><span class="sxs-lookup"><span data-stu-id="be795-116">1</span></span></p></td>
<td><p><span data-ttu-id="be795-117">拡張マークアップ言語 (XML) 形式であることを示します。</span><span class="sxs-lookup"><span data-stu-id="be795-117">Indicates Extensible Markup Language (XML) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be795-118"><strong>adPersistProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="be795-118"><strong>adPersistProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="be795-119">2</span><span class="sxs-lookup"><span data-stu-id="be795-119">2</span></span></p></td>
<td><p><span data-ttu-id="be795-120">プロバイダーが独自の形式を使って <strong>Recordset</strong> を保持することを示します。</span><span class="sxs-lookup"><span data-stu-id="be795-120">Indicates that the provider will persist the <strong>Recordset</strong> using its own format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be795-121">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="be795-121">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="be795-122">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="be795-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be795-123">定数</span><span class="sxs-lookup"><span data-stu-id="be795-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be795-124">AdoEnums.PersistFormat.ADTG</span><span class="sxs-lookup"><span data-stu-id="be795-124">AdoEnums.PersistFormat.ADTG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be795-125">AdoEnums.PersistFormat.XML</span><span class="sxs-lookup"><span data-stu-id="be795-125">AdoEnums.PersistFormat.XML</span></span></p></td>
</tr>
</tbody>
</table>
