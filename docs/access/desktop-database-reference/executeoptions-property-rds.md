---
title: executeoptions プロパティ (RDS)
TOCTitle: ExecuteOptions property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cf773090ccb37bf4cad4aff41499ad01f966479
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293253"
---
# <a name="executeoptions-property-rds"></a>executeoptions プロパティ (RDS)


**適用先:** Access 2013、Office 2013

非同期実行が有効かどうかを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

次のいずれかの値を設定または取得します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adcexecsync</strong></p></td>
<td><p>次回の <a href="recordset-object-ado.md">Recordset</a> の更新を同期的に実行します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adcExecAsync</strong></p></td>
<td><p>既定値です。 次回の <strong>Recordset</strong> の更新を非同期的に実行します。</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!メモ] これらの定数を使うクライアント側の各実行可能ファイルは、その定数を宣言する必要があります。C:\Program Files\Common Files\System\MSADC フォルダーの Adcvbs.inc ファイルから、定数の宣言を切り取って貼り付けることができます。

## <a name="remarks"></a>注釈

**ExecuteOptions** が **adcExecAsync** に設定されている場合、[RDS.DataControl](datacontrol-object-rds.md) オブジェクトの **Recordset** における次の **Refresh** 呼び出しは非同期的に実行されます。

[RDS.DataControl](datacontrol-object-rds.md) オブジェクトの **Recordset** に変更を行う可能性のある別の非同期操作の実行中に [Reset](reset-method-rds.md)、[Refresh](refresh-method-rds.md)、[SubmitChanges](submitchanges-method-rds.md)、[CancelUpdate](cancelupdate-method-ado.md)、または [Recordset](recordset-sourcerecordset-properties-rds.md) を呼び出そうとすると、エラーが発生します。

非同期操作中にエラーが発生した場合、**RDS.DataControl** オブジェクトの [ReadyState](readystate-property-rds.md) 値が **adcReadyStateLoaded** から **adcReadyStateComplete** に変更され、**Recordset** プロパティ値は *Nothing* のまま維持されます。

