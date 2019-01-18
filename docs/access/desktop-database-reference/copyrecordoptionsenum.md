---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb1637d1757a8507c6b6abb2a0c71867e3d1177b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703847"
---
# <a name="copyrecordoptionsenum"></a>CopyRecordOptionsEnum


**適用されます**Access 2013、Office 2013。

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
<td><p>4</p></td>
<td><p><em>同期元</em>プロバイダーがダウンロードを使用してコピーをシミュレートし、このメソッドは、<em>リンク先</em>が別のサーバー上にあるもののために障害が発生したり、<em>ソース</em>以外のプロバイダーがサービスを提供、アップロード操作をしようとすることを示します。 プロバイダーの機能のさまざまなパフォーマンスが低下したりデータが失われることに注意してください。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyNonRecursive</strong></p></td>
<td><p>2</p></td>
<td><p>コピー先に現在のディレクトリをコピーしますが、サブディレクトリはコピーしません。コピー操作は再帰的ではありません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCopyOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p><em>宛先</em>は、既存のファイルまたはディレクトリを指している場合は、ファイルまたはディレクトリを上書きします。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>既定値。既定のコピー操作を実行します。コピー操作は再帰的に行われ、コピー先のファイルやディレクトリが既に存在する場合は操作が失敗します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

これらの定数に ADO/WFC 等価はありません。

