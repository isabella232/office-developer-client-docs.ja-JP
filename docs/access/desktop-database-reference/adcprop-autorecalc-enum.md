---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc02e8cde556a70ca6b2c72f056d218904c31ec2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479247"
---
# <a name="adcpropautorecalcenum"></a><span data-ttu-id="0453a-102">ADCPROP\_AUTORECALC\_列挙型</span><span class="sxs-lookup"><span data-stu-id="0453a-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="0453a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0453a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0453a-104">階層 Recordset の集計列と計算列を [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) プロバイダーがいつ再計算するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0453a-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="0453a-105">これらの定数に対してのみ使用**MSDataShape**プロバイダーと、**レコード セット**"**自動再計算**"動的プロパティが、 [ADO の動的プロパティ インデックス](ado-dynamic-property-index.md)で参照されているカーソル サービスをマイクロソフトの[に記載されている OLEDB](microsoft-cursor-service-for-ole-db-ado-service-component.md)や[Microsoft データ シェイプ サービス](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)のドキュメントです。</span><span class="sxs-lookup"><span data-stu-id="0453a-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0453a-106">定数</span><span class="sxs-lookup"><span data-stu-id="0453a-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="0453a-107">値</span><span class="sxs-lookup"><span data-stu-id="0453a-107">Value</span></span></p></th>
<th><p><span data-ttu-id="0453a-108">説明</span><span class="sxs-lookup"><span data-stu-id="0453a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0453a-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="0453a-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="0453a-110">1</span><span class="sxs-lookup"><span data-stu-id="0453a-110">1</span></span></p></td>
<td><p><span data-ttu-id="0453a-p101">既定値です。計算列が依存する値が変更されたと <strong>MSDataShape</strong> プロバイダーが判断したときに再計算します。</span><span class="sxs-lookup"><span data-stu-id="0453a-p101">Default. Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0453a-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="0453a-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="0453a-114">0</span><span class="sxs-lookup"><span data-stu-id="0453a-114">0</span></span></p></td>
<td><p><span data-ttu-id="0453a-115">階層 <strong>Recordset</strong> の最初の作成時のみ計算します。</span><span class="sxs-lookup"><span data-stu-id="0453a-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0453a-116">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="0453a-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="0453a-117">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="0453a-117">These constants do not have ADO/WFC equivalents.</span></span>
