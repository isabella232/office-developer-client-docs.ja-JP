---
title: positionenum (Access デスクトップデータベースリファレンス)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c791cbd31e346eef5ab8503cb55b0dec5e9fbbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287504"
---
# <a name="positionenum"></a><span data-ttu-id="adfc8-102">PositionEnum</span><span class="sxs-lookup"><span data-stu-id="adfc8-102">PositionEnum</span></span>

<span data-ttu-id="adfc8-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="adfc8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="adfc8-104">[Recordset](recordset-object-ado.md) 内のレコード ポインターの現在の位置を表します。</span><span class="sxs-lookup"><span data-stu-id="adfc8-104">Specifies the current position of the record pointer within a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adfc8-105">定数</span><span class="sxs-lookup"><span data-stu-id="adfc8-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="adfc8-106">値</span><span class="sxs-lookup"><span data-stu-id="adfc8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="adfc8-107">説明</span><span class="sxs-lookup"><span data-stu-id="adfc8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adfc8-108"><strong>adposbof</strong></span><span class="sxs-lookup"><span data-stu-id="adfc8-108"><strong>adPosBOF</strong></span></span></p></td>
<td><p><span data-ttu-id="adfc8-109">-2</span><span class="sxs-lookup"><span data-stu-id="adfc8-109">-2</span></span></p></td>
<td><p><span data-ttu-id="adfc8-110">現在のレコード ポインターが BOF にあることを示します (<a href="bof-eof-properties-ado.md">BOF</a> プロパティが <strong>True</strong> です)。</span><span class="sxs-lookup"><span data-stu-id="adfc8-110">Indicates that the current record pointer is at BOF (that is, the <a href="bof-eof-properties-ado.md">BOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adfc8-111"><strong>adPosEOF</strong></span><span class="sxs-lookup"><span data-stu-id="adfc8-111"><strong>adPosEOF</strong></span></span></p></td>
<td><p><span data-ttu-id="adfc8-112">-3</span><span class="sxs-lookup"><span data-stu-id="adfc8-112">-3</span></span></p></td>
<td><p><span data-ttu-id="adfc8-113">現在のレコード ポインターが EOF にあることを示します (<a href="bof-eof-properties-ado.md">EOF</a> プロパティが <strong>True</strong> です)。</span><span class="sxs-lookup"><span data-stu-id="adfc8-113">Indicates that the current record pointer is at EOF (that is, the <a href="bof-eof-properties-ado.md">EOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adfc8-114"><strong>adposunknown</strong></span><span class="sxs-lookup"><span data-stu-id="adfc8-114"><strong>adPosUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="adfc8-115">-1</span><span class="sxs-lookup"><span data-stu-id="adfc8-115">-1</span></span></p></td>
<td><p><span data-ttu-id="adfc8-116"><strong>Recordset</strong> が空であるか、現在の位置が不明か、またはプロバイダーが <a href="absolutepage-property-ado.md">AbsolutePage</a> プロパティまたは <a href="absoluteposition-property-ado.md">AbsolutePosition</a> プロパティをサポートしていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="adfc8-116">Indicates that the <strong>Recordset</strong> is empty, the current position is unknown, or the provider does not support the <a href="absolutepage-property-ado.md">AbsolutePage</a> or <a href="absoluteposition-property-ado.md">AbsolutePosition</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="adfc8-117">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="adfc8-117">ADO/WFC equivalent</span></span>

<span data-ttu-id="adfc8-118">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="adfc8-118">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adfc8-119">定数</span><span class="sxs-lookup"><span data-stu-id="adfc8-119">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adfc8-120">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="adfc8-120">AdoEnums.Position.BOF</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adfc8-121">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="adfc8-121">AdoEnums.Position.EOF</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adfc8-122">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="adfc8-122">AdoEnums.Position.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

