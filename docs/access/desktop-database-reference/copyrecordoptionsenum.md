---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2417cde334d540866718407f6b2cfaedfc79e9a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589842"
---
# <a name="copyrecordoptionsenum"></a>CopyRecordOptionsEnum


**適用先**: Access 2013、Office 2013

[CopyRecord](copyrecord-method-ado.md) メソッドの動作を表します。

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
<td><p><strong>adCopyAllowEmulation</strong></p></td>
<td><p>4 </p></td>
<td><p>"コピー先" が別のサーバーにあるか、"コピー元" 以外のプロバイダーのサービスを受けているためにこのメソッドが失敗した場合、"コピー元" プロバイダーがダウンロード操作とアップロード操作を行ってコピーをシミュレートしようとすることを示します。プロバイダーの機能が異なると、パフォーマンスが低下したりデータが失われることがあります。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyNonRecursive</strong></p></td>
<td><p>2</p></td>
<td><p>コピー先に現在のディレクトリをコピーしますが、サブディレクトリはコピーしません。コピー操作は再帰的ではありません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCopyOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>"コピー先" が既存のファイルやディレクトリを指す場合、そのファイルやディレクトリを上書きします。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>既定値。既定のコピー操作を実行します。コピー操作は再帰的に行われ、コピー先のファイルやディレクトリが既に存在する場合は操作が失敗します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

これらの定数に ADO/WFC 等価はありません。

