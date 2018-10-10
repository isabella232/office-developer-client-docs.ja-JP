---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b018402f6a2d48819a3f97c69e2a8db77fa9e84c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479671"
---
# <a name="adcpropupdatecriteriaenum"></a>ADCPROP\_UPDATECRITERIA\_列挙型

**適用されます**Access 2013 |。Office 2013

[Recordset](recordset-object-ado.md) オブジェクトを使用してデータ ソース行の共有的更新を行う際に、競合の検出に使用するフィールドを表します。

これらの定数は、**Recordset** "**Update Criteria**" 動的プロパティで使用されます。このプロパティについては、「[ADO の動的プロパティ インデックス](ado-dynamic-property-index.md)」を参照してください。また、「[Microsoft Cursor Service for OLE DB (ADO サービス コンポーネント)](microsoft-cursor-service-for-ole-db-ado-service-component.md)」でも説明されています。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adCriteriaAllCols</strong></p></td>
<td><p>1</p></td>
<td><p>データ ソース行の列が変更された場合に競合を検出します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaKey</strong></p></td>
<td><p>0</p></td>
<td><p>データ ソース行のキー列が変更された場合、つまり行が削除された場合に競合を検出します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCriteriaTimeStamp</strong></p></td>
<td><p>3</p></td>
<td><p>データ ソース行のタイムスタンプが変更された場合、つまり <strong>Recordset</strong> を取得した後に行にアクセスがあった場合に競合を検出します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaUpdCols</strong></p></td>
<td><p>2</p></td>
<td><p><strong>Recordset</strong> の更新されたフィールドに対応するデータ ソース行の列が変更された場合に競合を検出します。</p></td>
</tr>
</tbody>
</table>


**ADO/WFC 等価**

パッケージ: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.AdcPropUpdateCriteria.ALLCOLS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropUpdateCriteria.KEY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropUpdateCriteria.UPDCOLS</p></td>
</tr>
</tbody>
</table>

