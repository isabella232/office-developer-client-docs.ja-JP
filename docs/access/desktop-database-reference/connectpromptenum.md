---
title: ConnectPromptEnum (Access デスクトップデータベースリファレンス)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54643a66316d7f534553c20ecc3aafdf755fb857
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295668"
---
# <a name="connectpromptenum"></a>ConnectPromptEnum

**適用先:** Access 2013、Office 2013

データ ソースとの接続を開くときに、不足しているパラメーターを要求するダイアログ ボックスを表示するかどうかを表します。

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
<td><p><strong>adpromptalways</strong></p></td>
<td><p>1-d</p></td>
<td><p>常に要求します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adpromptcomplete</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>さらに情報が必要な場合に要求します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPromptCompleteRequired</strong></p></td>
<td><p>1/3</p></td>
<td><p>さらに情報が必要だが、任意のパラメーターが禁止されている場合に要求します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adpromptnever</strong></p></td>
<td><p>2/4</p></td>
<td><p>要求しません。</p></td>
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
<td><p>AdoEnums。常に</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の完全なメッセージ</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums COMPLETEREQUIRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums のメッセージを表示しない</p></td>
</tr>
</tbody>
</table>

