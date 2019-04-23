---
title: ObjectStateEnum (Access デスクトップデータベースリファレンス)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288526"
---
# <a name="objectstateenum"></a>ObjectStateEnum

**適用先:** Access 2013、Office 2013

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
<td><p><strong>adStateClosed</strong></p></td>
<td><p>.0</p></td>
<td><p>オブジェクトが閉じていることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adstateopen</strong></p></td>
<td><p>1-d</p></td>
<td><p>オブジェクトが開いていることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStateConnecting</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>オブジェクトが接続中であることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adStateExecuting</strong></p></td>
<td><p>2/4</p></td>
<td><p>オブジェクトがコマンドを実行中であることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adstatefetching</strong></p></td>
<td><p>~</p></td>
<td><p>オブジェクトの行を取得中であることを示します。</p></td>
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
<td><p>AdoEnums を閉じた状態にします。</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums を開きます。</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums 接続</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の実行</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の状態</p></td>
</tr>
</tbody>
</table>

