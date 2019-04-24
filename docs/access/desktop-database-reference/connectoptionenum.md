---
title: ConnectOptionEnum (Access デスクトップデータベースリファレンス)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95b622d2216b085ffd0f76c8a26533187c17bd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295682"
---
# <a name="connectoptionenum"></a>ConnectOptionEnum

**適用先:** Access 2013、Office 2013

[Connection](connection-object-ado.md) オブジェクトの [Open](open-method-ado-connection.md) メソッドから制御が戻るのが、接続確立の後 (同期) か前 (非同期) かを表します。

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
<td><p><strong>adAsyncConnect</strong></p></td>
<td><p>16</p></td>
<td><p>接続を非同期で開きます。接続可能かをどうかを判別するために、<a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> イベントが使用される場合があります。</p></td>
</tr>
<tr class="even">
<td><p><strong>adの指定</strong></p></td>
<td><p>-1</p></td>
<td><p>既定値。接続を同期で開きます。</p></td>
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
<td><p>ConnectOption 接続</p></td>
</tr>
<tr class="even">
<td><p>指定された ConnectOption AdoEnums</p></td>
</tr>
</tbody>
</table>

