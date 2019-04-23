---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 53e51f2386658ee975ec8847f7e5550ac22bbd8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281902"
---
# <a name="adcpropasyncthreadpriorityenum"></a>ADCPROP\_ASYNCTHREADPRIORITY\_列挙型

**適用先:** Access 2013、Office 2013

RDS の [Recordset](recordset-object-ado.md) オブジェクトに対して、データを取得する非同期スレッドの実行優先度を表します。

これらの定数は、ADO の動的プロパティ インデックスで参照される **Recordset** "**Background Thread Priority**" 動的プロパティで使用し、「[Microsoft Cursor Service for OLE DB (ADO サービス コンポーネント)](microsoft-cursor-service-for-ole-db-ado-service-component.md)」で説明されています。

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
<td><p><strong>adPriorityAboveNormal</strong></p></td>
<td><p>2/4</p></td>
<td><p>優先度を標準と最高の間に設定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adPriorityBelowNormal</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>優先度を最低と標準の間に設定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>ad優先度: 最高</strong></p></td>
<td><p>5</p></td>
<td><p>優先度を可能な最高レベルに設定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>ad優先順位の最も低い</strong></p></td>
<td><p>1-d</p></td>
<td><p>優先度を可能な最低レベルに設定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>ad優先順位標準</strong></p></td>
<td><p>1/3</p></td>
<td><p>優先度を標準に設定します。</p></td>
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
<td><p>ABOVENORMAL を AdoEnums します。</p></td>
</tr>
<tr class="even">
<td><p>BELOWNORMAL を AdoEnums します。</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の優先度が最も高い</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums、またはそれより小さい</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums を行います。標準</p></td>
</tr>
</tbody>
</table>

