---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0a9954319448a219d9683cfd8133929fb3d184d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476669"
---
# <a name="searchdirectionenum"></a><span data-ttu-id="56ea5-102">SearchDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="56ea5-102">SearchDirectionEnum</span></span>


<span data-ttu-id="56ea5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="56ea5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="56ea5-104">[Recordset](recordset-object-ado.md) 内のレコードの検索方向を表します。</span><span class="sxs-lookup"><span data-stu-id="56ea5-104">Specifies the direction of a record search within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56ea5-105">定数</span><span class="sxs-lookup"><span data-stu-id="56ea5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="56ea5-106">値</span><span class="sxs-lookup"><span data-stu-id="56ea5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="56ea5-107">説明</span><span class="sxs-lookup"><span data-stu-id="56ea5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56ea5-108"><strong>adSearchBackward</strong></span><span class="sxs-lookup"><span data-stu-id="56ea5-108"><strong>adSearchBackward</strong></span></span></p></td>
<td><p><span data-ttu-id="56ea5-109">-1</span><span class="sxs-lookup"><span data-stu-id="56ea5-109">-1</span></span></p></td>
<td><p><span data-ttu-id="56ea5-p101">後方検索をし、<strong>Recordset</strong> の先頭で終了します。一致するレコードが見つからない場合、レコード ポインターは <a href="bof-eof-properties-ado.md">BOF</a> に移動します。</span><span class="sxs-lookup"><span data-stu-id="56ea5-p101">Searches backward, stopping at the beginning of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">BOF</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56ea5-112"><strong>adSearchForward</strong></span><span class="sxs-lookup"><span data-stu-id="56ea5-112"><strong>adSearchForward</strong></span></span></p></td>
<td><p><span data-ttu-id="56ea5-113">1</span><span class="sxs-lookup"><span data-stu-id="56ea5-113">1</span></span></p></td>
<td><p><span data-ttu-id="56ea5-p102">前方検索をし、<strong>Recordset</strong> の末尾で終了します。一致するレコードが見つからない場合、レコード ポインターは <a href="bof-eof-properties-ado.md">EOF</a> に移動します。</span><span class="sxs-lookup"><span data-stu-id="56ea5-p102">Searches forward, stopping at the end of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">EOF</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="56ea5-116">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="56ea5-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="56ea5-117">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="56ea5-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56ea5-118">定数</span><span class="sxs-lookup"><span data-stu-id="56ea5-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56ea5-119">AdoEnums.SearchDirection.BACKWARD</span><span class="sxs-lookup"><span data-stu-id="56ea5-119">AdoEnums.SearchDirection.BACKWARD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56ea5-120">AdoEnums.SearchDirection.FORWARD</span><span class="sxs-lookup"><span data-stu-id="56ea5-120">AdoEnums.SearchDirection.FORWARD</span></span></p></td>
</tr>
</tbody>
</table>

