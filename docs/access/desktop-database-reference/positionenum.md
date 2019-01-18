---
title: PositionEnum (デスクトップ データベース参照のアクセス)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c791cbd31e346eef5ab8503cb55b0dec5e9fbbc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702839"
---
# <a name="positionenum"></a><span data-ttu-id="429ea-102">PositionEnum</span><span class="sxs-lookup"><span data-stu-id="429ea-102">PositionEnum</span></span>

<span data-ttu-id="429ea-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="429ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="429ea-104">[Recordset](recordset-object-ado.md) 内のレコード ポインターの現在の位置を表します。</span><span class="sxs-lookup"><span data-stu-id="429ea-104">Specifies the current position of the record pointer within a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="429ea-105">定数</span><span class="sxs-lookup"><span data-stu-id="429ea-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="429ea-106">値</span><span class="sxs-lookup"><span data-stu-id="429ea-106">Value</span></span></p></th>
<th><p><span data-ttu-id="429ea-107">説明</span><span class="sxs-lookup"><span data-stu-id="429ea-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="429ea-108"><strong>adPosBOF</strong></span><span class="sxs-lookup"><span data-stu-id="429ea-108"><strong>adPosBOF</strong></span></span></p></td>
<td><p><span data-ttu-id="429ea-109">-2</span><span class="sxs-lookup"><span data-stu-id="429ea-109">-2</span></span></p></td>
<td><p><span data-ttu-id="429ea-110">現在のレコード ポインターが BOF にあることを示します (<a href="bof-eof-properties-ado.md">BOF</a> プロパティが <strong>True</strong> です)。</span><span class="sxs-lookup"><span data-stu-id="429ea-110">Indicates that the current record pointer is at BOF (that is, the <a href="bof-eof-properties-ado.md">BOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="429ea-111"><strong>adPosEOF</strong></span><span class="sxs-lookup"><span data-stu-id="429ea-111"><strong>adPosEOF</strong></span></span></p></td>
<td><p><span data-ttu-id="429ea-112">-3</span><span class="sxs-lookup"><span data-stu-id="429ea-112">-3</span></span></p></td>
<td><p><span data-ttu-id="429ea-113">現在のレコード ポインターが EOF にあることを示します (<a href="bof-eof-properties-ado.md">EOF</a> プロパティが <strong>True</strong> です)。</span><span class="sxs-lookup"><span data-stu-id="429ea-113">Indicates that the current record pointer is at EOF (that is, the <a href="bof-eof-properties-ado.md">EOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="429ea-114"><strong>adPosUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="429ea-114"><strong>adPosUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="429ea-115">-1</span><span class="sxs-lookup"><span data-stu-id="429ea-115">-1</span></span></p></td>
<td><p><span data-ttu-id="429ea-116"><strong>Recordset</strong> が空であるか、現在の位置が不明か、またはプロバイダーが <a href="absolutepage-property-ado.md">AbsolutePage</a> プロパティまたは <a href="absoluteposition-property-ado.md">AbsolutePosition</a> プロパティをサポートしていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="429ea-116">Indicates that the <strong>Recordset</strong> is empty, the current position is unknown, or the provider does not support the <a href="absolutepage-property-ado.md">AbsolutePage</a> or <a href="absoluteposition-property-ado.md">AbsolutePosition</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="429ea-117">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="429ea-117">ADO/WFC equivalent</span></span>

<span data-ttu-id="429ea-118">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="429ea-118">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="429ea-119">定数</span><span class="sxs-lookup"><span data-stu-id="429ea-119">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="429ea-120">AdoEnums.Position.BOF</span><span class="sxs-lookup"><span data-stu-id="429ea-120">AdoEnums.Position.BOF</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="429ea-121">AdoEnums.Position.EOF</span><span class="sxs-lookup"><span data-stu-id="429ea-121">AdoEnums.Position.EOF</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="429ea-122">AdoEnums.Position.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="429ea-122">AdoEnums.Position.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

