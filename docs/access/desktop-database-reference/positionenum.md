---
title: PositionEnum (デスクトップ データベース参照のアクセス)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c2ef44c804a413b85bcf393e1487ff4423c40f0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476716"
---
# <a name="positionenum"></a><span data-ttu-id="3b8fe-102">PositionEnum</span><span class="sxs-lookup"><span data-stu-id="3b8fe-102">PositionEnum</span></span>


<span data-ttu-id="3b8fe-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b8fe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3b8fe-104">[Recordset](recordset-object-ado.md) 内のレコード ポインターの現在の位置を表します。</span><span class="sxs-lookup"><span data-stu-id="3b8fe-104">Specifies the current position of the record pointer within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b8fe-105">定数</span><span class="sxs-lookup"><span data-stu-id="3b8fe-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3b8fe-106">値</span><span class="sxs-lookup"><span data-stu-id="3b8fe-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3b8fe-107">説明</span><span class="sxs-lookup"><span data-stu-id="3b8fe-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b8fe-108"><strong>adPosBOF</strong></span><span class="sxs-lookup"><span data-stu-id="3b8fe-108"><strong>adPosBOF</strong></span></span></p></td>
<td><p><span data-ttu-id="3b8fe-109">-2</span><span class="sxs-lookup"><span data-stu-id="3b8fe-109">-2</span></span></p></td>
<td><p><span data-ttu-id="3b8fe-110">現在のレコード ポインターが BOF にあることを示します (<a href="bof-eof-properties-ado.md">BOF</a> プロパティが <strong>True</strong> です)。</span><span class="sxs-lookup"><span data-stu-id="3b8fe-110">Indicates that the current record pointer is at BOF (that is, the <a href="bof-eof-properties-ado.md">BOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b8fe-111"><strong>adPosEOF</strong></span><span class="sxs-lookup"><span data-stu-id="3b8fe-111"><strong>adPosEOF</strong></span></span></p></td>
<td><p><span data-ttu-id="3b8fe-112">-3</span><span class="sxs-lookup"><span data-stu-id="3b8fe-112">-3</span></span></p></td>
<td><p><span data-ttu-id="3b8fe-113">現在のレコード ポインターが EOF にあることを示します (<a href="bof-eof-properties-ado.md">EOF</a> プロパティが <strong>True</strong> です)。</span><span class="sxs-lookup"><span data-stu-id="3b8fe-113">Indicates that the current record pointer is at EOF (that is, the <a href="bof-eof-properties-ado.md">EOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b8fe-114"><strong>adPosUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="3b8fe-114"><strong>adPosUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="3b8fe-115">-1</span><span class="sxs-lookup"><span data-stu-id="3b8fe-115">-1</span></span></p></td>
<td><p><span data-ttu-id="3b8fe-116"><strong>Recordset</strong> が空であるか、現在の位置が不明か、またはプロバイダーが <a href="absolutepage-property-ado.md">AbsolutePage</a> プロパティまたは <a href="absoluteposition-property-ado.md">AbsolutePosition</a> プロパティをサポートしていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="3b8fe-116">Indicates that the <strong>Recordset</strong> is empty, the current position is unknown, or the provider does not support the <a href="absolutepage-property-ado.md">AbsolutePage</a> or <a href="absoluteposition-property-ado.md">AbsolutePosition</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b8fe-117">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="3b8fe-117">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="3b8fe-118">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="3b8fe-118">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b8fe-119">定数</span><span class="sxs-lookup"><span data-stu-id="3b8fe-119">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b8fe-120">AdoEnums.Position.BOF</span><span class="sxs-lookup"><span data-stu-id="3b8fe-120">AdoEnums.Position.BOF</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b8fe-121">AdoEnums.Position.EOF</span><span class="sxs-lookup"><span data-stu-id="3b8fe-121">AdoEnums.Position.EOF</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b8fe-122">AdoEnums.Position.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="3b8fe-122">AdoEnums.Position.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

