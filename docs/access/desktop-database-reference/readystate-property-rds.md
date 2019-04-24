---
title: ReadyState プロパティ (RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 71dd674e90e2438c616f0973c4f9948f1b20b1f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300820"
---
# <a name="readystate-property-rds"></a>ReadyState プロパティ (RDS)

**適用先:** Access 2013、Office 2013

[DataControl](datacontrol-object-rds.md) オブジェクトがデータを取得して [Recordset](recordset-object-ado.md) オブジェクトに格納するときの進行状況を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

次のいずれかの値を設定または取得します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adcReadyStateLoaded</strong></p></td>
<td><p>現在のクエリが実行中で、行はまだ取得されていません。 <strong>DataControl</strong> オブジェクトの <strong>Recordset</strong> は使用できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adcreadystateinteractive</strong></p></td>
<td><p>現在のクエリによって取得された最初の行セットが <strong>DataControl</strong> オブジェクトの <strong>Recordset</strong> に格納され、使用できます。残りの行はまだ取得中です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcReadyStateComplete</strong></p></td>
<td><p>現在のクエリによって取得されたすべての行が <strong>DataControl</strong> オブジェクトの <strong>Recordset</strong> に格納され、使用できます。 エラーで処理が中止された場合や、<strong>Recordset</strong> オブジェクトが初期化されていない場合も、この状態になります。</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!メモ] これらの定数を使用するクライアント側の各実行可能ファイルで、使用する定数を宣言する必要があります。定数の宣言は、C:\Program Files\Common Files\System\MSADC フォルダーにある Adcvbs.inc ファイルからコピーして貼り付けることができます。

## <a name="remarks"></a>注釈

非同期クエリの処理中に **ReadyState** プロパティの変更を監視するには、[onReadyStateChange](onreadystatechange-event-rds.md) イベントを使用します。この方法は、定期的にプロパティの値を確認するよりも効率的です。

非同期操作中にエラーが発生した場合、 **ReadyState**プロパティは**adcReadyStateComplete**に変更され、 [State](state-property-ado.md)プロパティは**adstateexecuting**から**adStateClosed**、および**Recordset**に変更されます。オブジェクトの[Value](value-property-ado.md)プロパティは*Nothing*のままです。

