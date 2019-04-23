---
title: persistformatenum (Access デスクトップデータベースリファレンス)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4954c09c3eff67bb6f55dfc9e49464ad58fad5e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287609"
---
# <a name="persistformatenum"></a>PersistFormatEnum

**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) を保存するときの形式を表します。

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
<td><p><strong>adPersistADTG</strong></p></td>
<td><p>.0</p></td>
<td><p>Microsoft Advanced Data TableGram (ADTG) 形式であることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adpersistado</strong></p></td>
<td><p>1-d</p></td>
<td><p>ADO 独自の拡張マークアップ言語 (XML) 形式が使用されることを示します。この値は adPersistXML と同じであり、以前のバージョンとの互換性は保たれます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adpersistxml</strong></p></td>
<td><p>1-d</p></td>
<td><p>拡張マークアップ言語 (XML) 形式であることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adpersistproviderspecific</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>プロバイダーが独自の形式を使って <strong>Recordset</strong> を保持することを示します。</p></td>
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
<td><p>AdoEnums ADTG</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums 形式の XML</p></td>
</tr>
</tbody>
</table>

