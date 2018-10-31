---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc621f620a7d55571aa55296a4d294fff9566bf5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862241"
---
# <a name="moverecordoptionsenum"></a>MoveRecordOptionsEnum


**適用されます**Access 2013 |。Office 2013

[Record](record-object-ado.md) オブジェクトの [MoveRecord](moverecord-method-ado.md) メソッドの動作を表します。

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
<td><p><strong>adMoveUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>既定値。既定の移動操作を実行します。既存の宛先ファイルまたはディレクトリがある場合は操作が失敗し、ハイパーテキスト リンクが更新されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>既存の宛先ファイルまたはディレクトリがあっても上書きします。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adMoveDontUpdateLinks</strong></p></td>
<td><p>2</p></td>
<td><p>ソース <strong>Record</strong> のハイパーテキスト リンクを更新しないことで、<strong>MoveRecord</strong> メソッドの既定動作を変更します。既定動作はプロバイダーの機能によって異なります。プロバイダーがサポートしていれば、移動操作でリンクが更新されます。プロバイダーがリンクの修正をサポートしていない場合、またはこの値が指定されていない場合、リンクを修正しなくても移動は成功します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveAllowEmulation</strong></p></td>
<td><p>4</p></td>
<td><p>プロバイダーによる移動 (ダウンロード、アップロード、削除の操作を使用) のシミュレーションを要求します。宛先 URL がソースとは別のサーバーにあったり、別のプロバイダーがサービスを提供しているために <strong>Record</strong> の移動が失敗すると、プロバイダー間でリソースを移動するときのプロバイダーの機能の違いにより、遅延時間の増加やデータの損失が起きることがあります。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

これらの定数に ADO/WFC 等価はありません。

