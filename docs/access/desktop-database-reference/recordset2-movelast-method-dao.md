---
title: Recordset2.MoveLast メソッド (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1cd29fe99db3cdf3e00556b389328d46d06a6f82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601934"
---
# <a name="recordset2movelast-method-dao"></a>Recordset2.MoveLast メソッド (DAO)

**適用先**: Access 2013、Office 2013

指定された **Recordset** オブジェクトの最後のレコードに移動し、そのレコードをカレント レコードにします。

## <a name="syntax"></a>構文

*式* .MoveLast(***Options***)

*式* Recordset2 オブジェクトを **表す変数** 。

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
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>オプション</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Long</strong></p></td>
<td><p><strong>MoveLast</strong> への呼び出しを非同期で実行する場合に <strong>dbRunAsync</strong> に設定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈


            **Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。

カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。


            **Recordset** を開いた時点では、最初のレコードがカレント レコードで、**BOF** プロパティは **False** です。**Recordset** にレコードが含まれていない場合、**BOF** プロパティは **True** で、カレント レコードはありません。


            **MoveFirst** または **MoveLast** を使用したときに、最初のレコードまたは最後のレコードが既にカレント レコードである場合、カレント レコードは変更されません。

recordset がテーブル タイプの **Recordset** である場合 (Microsoft Access ワークスペースのみ)、現在のインデックスに従って移動が行われます。 現在のインデックスを設定するには、 **Index** プロパティを使用します。 現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。

> [!NOTE]
> [!メモ] **MoveLast** メソッドを使用すると、ダイナセット タイプまたはスナップショット タイプの **Recordset** の末尾までデータを格納して、 **Recordset** に含まれるカレント レコード数を示すことができます。 ただし、このような目的で **MoveLast** を使用すると、アプリケーションのパフォーマンスが低下する場合があります。 **MoveLast** を使用してレコード数を取得するのは、新しく開かれた **Recordset** の正確なレコード数をどうしても取得する必要がある場合だけにしてください。 
>
> **MoveLast** で **dbRunAsync** 定数を使用すると、メソッドの呼び出しが非同期で実行されます。 **Recordset** の末尾までデータが格納されたことを確認するには **StillExecuting** プロパティを使用し、**MoveLast** メソッドに対する非同期呼び出しの実行を終了するには **Cancel** メソッドを使用します。


            **MoveFirst**、**MoveLast**、および **MovePrevious** の各メソッドは、前方スクロール タイプの **Recordset** オブジェクトでは使用できません。


            **Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、**Move** メソッドを使用します。

