---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: b1ebc5cf8df4a0eab125f788544dba40ec373d02
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880650"
---
# <a name="adcpropupdatecriteriaenum"></a><span data-ttu-id="36aa6-102">ADCPROP\_UPDATECRITERIA\_列挙型</span><span class="sxs-lookup"><span data-stu-id="36aa6-102">ADCPROP\_UPDATECRITERIA\_ENUM</span></span>

<span data-ttu-id="36aa6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="36aa6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="36aa6-104">[Recordset](recordset-object-ado.md) オブジェクトを使用してデータ ソース行の共有的更新を行う際に、競合の検出に使用するフィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="36aa6-104">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="36aa6-105">これらの定数は、**Recordset** "**Update Criteria**" 動的プロパティで使用されます。このプロパティについては、「[ADO の動的プロパティ インデックス](ado-dynamic-property-index.md)」を参照してください。また、「[Microsoft Cursor Service for OLE DB (ADO サービス コンポーネント)](microsoft-cursor-service-for-ole-db-ado-service-component.md)」でも説明されています。</span><span class="sxs-lookup"><span data-stu-id="36aa6-105">Use these constants with the **Recordset** "**Update Criteria**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36aa6-106">定数</span><span class="sxs-lookup"><span data-stu-id="36aa6-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="36aa6-107">値</span><span class="sxs-lookup"><span data-stu-id="36aa6-107">Value</span></span></p></th>
<th><p><span data-ttu-id="36aa6-108">説明</span><span class="sxs-lookup"><span data-stu-id="36aa6-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36aa6-109"><strong>adCriteriaAllCols</strong></span><span class="sxs-lookup"><span data-stu-id="36aa6-109"><strong>adCriteriaAllCols</strong></span></span></p></td>
<td><p><span data-ttu-id="36aa6-110">1</span><span class="sxs-lookup"><span data-stu-id="36aa6-110">1</span></span></p></td>
<td><p><span data-ttu-id="36aa6-111">データ ソース行の列が変更された場合に競合を検出します。</span><span class="sxs-lookup"><span data-stu-id="36aa6-111">Detects conflicts if any column of the data source row has been changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36aa6-112"><strong>adCriteriaKey</strong></span><span class="sxs-lookup"><span data-stu-id="36aa6-112"><strong>adCriteriaKey</strong></span></span></p></td>
<td><p><span data-ttu-id="36aa6-113">0</span><span class="sxs-lookup"><span data-stu-id="36aa6-113">0</span></span></p></td>
<td><p><span data-ttu-id="36aa6-114">データ ソース行のキー列が変更された場合、つまり行が削除された場合に競合を検出します。</span><span class="sxs-lookup"><span data-stu-id="36aa6-114">Detects conflicts if the key column of the data source row has been changed, which means that the row has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36aa6-115"><strong>adCriteriaTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="36aa6-115"><strong>adCriteriaTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="36aa6-116">3</span><span class="sxs-lookup"><span data-stu-id="36aa6-116">3</span></span></p></td>
<td><p><span data-ttu-id="36aa6-117">データ ソース行のタイムスタンプが変更された場合、つまり <strong>Recordset</strong> を取得した後に行にアクセスがあった場合に競合を検出します。</span><span class="sxs-lookup"><span data-stu-id="36aa6-117">Detects conflicts if the timestamp of the data source row has been changed, which means the row has been accessed after the <strong>Recordset</strong> was obtained.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36aa6-118"><strong>adCriteriaUpdCols</strong></span><span class="sxs-lookup"><span data-stu-id="36aa6-118"><strong>adCriteriaUpdCols</strong></span></span></p></td>
<td><p><span data-ttu-id="36aa6-119">2</span><span class="sxs-lookup"><span data-stu-id="36aa6-119">2</span></span></p></td>
<td><p><span data-ttu-id="36aa6-120"><strong>Recordset</strong> の更新されたフィールドに対応するデータ ソース行の列が変更された場合に競合を検出します。</span><span class="sxs-lookup"><span data-stu-id="36aa6-120">Detects conflicts if any of the columns of the data source row that correspond to updated fields of the <strong>Recordset</strong> have been changed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="36aa6-121">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="36aa6-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="36aa6-122">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="36aa6-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36aa6-123">定数</span><span class="sxs-lookup"><span data-stu-id="36aa6-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36aa6-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span><span class="sxs-lookup"><span data-stu-id="36aa6-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36aa6-125">AdoEnums.AdcPropUpdateCriteria.KEY</span><span class="sxs-lookup"><span data-stu-id="36aa6-125">AdoEnums.AdcPropUpdateCriteria.KEY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36aa6-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="36aa6-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36aa6-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span><span class="sxs-lookup"><span data-stu-id="36aa6-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span></span></p></td>
</tr>
</tbody>
</table>

