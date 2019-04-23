---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8be93b0b7e4b32e3c040e871ff7d97a95f1e247e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282853"
---
# <a name="adcpropupdatecriteriaenum"></a>ADCPROP\_UPDATECRITERIA\_列挙

**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクトを使用してデータ ソース行の共有的更新を行う際に、競合の検出に使用するフィールドを表します。

これらの定数は、**Recordset** "**Update Criteria**" 動的プロパティで使用されます。このプロパティについては、「[ADO の動的プロパティ インデックス](ado-dynamic-property-index.md)」を参照してください。また、「[Microsoft Cursor Service for OLE DB (ADO サービス コンポーネント)](microsoft-cursor-service-for-ole-db-ado-service-component.md)」でも説明されています。

<br/>

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
<td><p><strong>adの基準 aallcols</strong></p></td>
<td><p>1-d</p></td>
<td><p>データ ソース行の列が変更された場合に競合を検出します。</p></td>
</tr>
<tr class="even">
<td><p><strong>ad基準 akey</strong></p></td>
<td><p>.0</p></td>
<td><p>データ ソース行のキー列が変更された場合、つまり行が削除された場合に競合を検出します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>(adme) スタンプ</strong></p></td>
<td><p>1/3</p></td>
<td><p>データ ソース行のタイムスタンプが変更された場合、つまり <strong>Recordset</strong> を取得した後に行にアクセスがあった場合に競合を検出します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adます。</strong></p></td>
<td><p>pbm-2</p></td>
<td><p><strong>Recordset</strong> の更新されたフィールドに対応するデータ ソース行の列が変更された場合に競合を検出します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

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
<td><p>AdoEnums AdcPropUpdateCriteria</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums AdcPropUpdateCriteria</p></td>
</tr>
</tbody>
</table>

