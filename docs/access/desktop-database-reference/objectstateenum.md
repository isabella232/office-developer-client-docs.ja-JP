---
title: ObjectStateEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712268"
---
# <a name="objectstateenum"></a>ObjectStateEnum

**適用されます**Access 2013、Office 2013。

オブジェクトが開いているか閉じているか、データ ソースに接続中か、コマンドを実行中か、またはデータを取得中かを表します。

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
<td><p><strong>取得のみ</strong></p></td>
<td><p>0</p></td>
<td><p>オブジェクトが閉じていることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>可能です。</strong></p></td>
<td><p>1</p></td>
<td><p>オブジェクトが開いていることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStateConnecting</strong></p></td>
<td><p>2</p></td>
<td><p>オブジェクトが接続中であることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adStateExecuting</strong></p></td>
<td><p>4</p></td>
<td><p>オブジェクトがコマンドを実行中であることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStateFetching</strong></p></td>
<td><p>8</p></td>
<td><p>オブジェクトの行を取得中であることを示します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

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
<td><p>AdoEnums.ObjectState.CLOSED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ObjectState.OPEN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ObjectState.CONNECTING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ObjectState.EXECUTING</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ObjectState.FETCHING</p></td>
</tr>
</tbody>
</table>

