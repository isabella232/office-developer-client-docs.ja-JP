---
title: Recordset2.MoveLast メソッド (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 83db6ae8da804237222fc1f58e03058951d7ce41
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998988"
---
# <a name="recordset2movelast-method-dao"></a>Recordset2.MoveLast メソッド (DAO)

**適用されます**Access 2013、Office 2013。

指定された **Recordset** オブジェクトの最後のレコードに移動し、そのレコードをカレント レコードにします。

## <a name="syntax"></a>構文

*式*です。MoveLast (***オプション***)

*式***Recordset2**オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>長整数型 (Long)</strong></p></td>
<td><p><strong>MoveLast</strong> への呼び出しを非同期で実行する場合に <strong>dbRunAsync</strong> に設定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。

カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。

**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合、 **BOF** プロパティは **True** で、カレント レコードはありません。

**MoveFirst** または **MoveLast** を使用したときに、最初のレコードまたは最後のレコードが既にカレント レコードである場合、カレント レコードは変更されません。

レコード セットは、テーブル タイプ**のレコード セット**(Microsoft Access ワークスペースのみ) を参照している場合の移動は現在のインデックスに従います。 現在のインデックスを設定するには、 **Index** プロパティを使用します。 現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。

> [!NOTE]
> [!メモ] **MoveLast** メソッドを使用すると、ダイナセット タイプまたはスナップショット タイプの **Recordset** の末尾までデータを格納して、 **Recordset** に含まれる現在のレコード数を示すことができます。 ただし、このような目的で **MoveLast** を使用すると、アプリケーションのパフォーマンスが低下する場合があります。 **MoveLast** を使用してレコード数を取得するのは、新しく開かれた **Recordset** の正確なレコード数をどうしても取得する必要がある場合だけにしてください。 
>
> **MoveLast** で **dbRunAsync** 定数を使用すると、メソッドの呼び出しが非同期で実行されます。 **Recordset** の末尾までデータが格納されたことを確認するには **StillExecuting** プロパティを使用し、 **MoveLast** メソッドに対する非同期呼び出しの実行を終了するには **Cancel** メソッドを使用します。

前方のみタイプの**Recordset**オブジェクトでは、 **MoveFirst**、 **MoveLast**、および**MovePrevious**メソッドを使うことはできません。

**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、 **Move** メソッドを使用します。

