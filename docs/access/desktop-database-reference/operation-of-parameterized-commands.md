---
title: パラメーター化コマンドの操作
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 08c290f0eaf6c5dd6787031e688604063970b2b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577172"
---
# <a name="operation-of-parameterized-commands"></a>パラメーター化コマンドの操作

**適用先:** Access 2013、Office 2013

大きな子 **Recordset** を処理するとき、特に親 **Recordset** のサイズと比べて大きいにもかかわらず、わずかな子チャプターにアクセスするだけの場合は、パラメーター化コマンドを使用する方が効率的です。

パラメーター *化されていない* コマンドは、親レコードセットと子 **Recordsets** の両方を取得し、チャプター列を親に追加し、親行ごとに関連する子チャプターへの参照を割り当てる。

パラメーター *化されたコマンドは* 、親 **Recordset** 全体を取得しますが、チャプター列にアクセスすると **チャプター Recordset** のみを取得します。 This difference in retrieval strategy can yield significant performance benefits.

たとえば、次のように指定することができます。

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

親テーブルと子テーブルの列名は、共通の cust \_ id です *。* *child-command* には、RELATE 句の参照先 ("...PARAMETER 0") へのプレースホルダー "?" が指定されています。

> [!NOTE]
> [!メモ] PARAMETER 句は、Shape コマンドの構文にのみ影響します。ADO の [Parameter](parameter-object-ado.md) オブジェクトまたは [Parameters](parameters-collection-ado.md) コレクションとは関係ありません。

パラメーター化された Shape コマンドが実行されると、次のようになります。

1.  *parent-command* が実行され、Customers テーブルから親 **Recordset** が返されます。

2.  チャプター列が親 **Recordset** に追加されます。

3.  親行のチャプター列にアクセスすると、パラメーターの値としてcustomer.cust id の値を使用して子コマンド \_ が実行されます。

4.  手順 3 で作成したデータ プロバイダー行セット内のすべての行を使用して、子 Recordset を設定 **します**。 この例では、cust id が customer.cust id の値と等しい Orders テーブルのすべての行 \_ \_ です。 既定では、親 **Recordset** へのすべての参照が解放されるまで、子 Recordset s は **クライアントにキャッシュ** されます。 この動作を変更するには **、Recordset**[](ado-dynamic-property-index.md)動的プロパティ Cache Child Rows を **False に****設定します**。

5.  取得された子の行への参照 (つまり、子 **Recordset** のチャプター) は、親 **Recordset** のカレント行のチャプター列に配置されます。

6.  別の行のチャプター列にアクセスすると、手順 3. ～ 5. が繰り返されます。

既定では、 **Cache Child Rows** 動的プロパティは **True** に設定されています。キャッシュの動作は、クエリのパラメーター値によって異なります。単一のパラメーターが指定されたクエリの場合、指定されたパラメーター値に対応する子 **Recordset** は、その値を持つ子に対する要求があるまでキャッシュに保持されます。次のコードにこの例を示します。

```vb
... 
SCmd = "SHAPE {select * from customer} " & _ 
 "APPEND({select * from orders where cust_id = ?} " & _ 
 "RELATE cust_id TO PARAMETER 0) AS chpCustOrder" 
Rst1.Open sCmd, Cnn1 
Set RstChild = Rst1("chpCustOrder").Value 
Rst1.MoveNext ' Next cust_id passed to Param 0, & new rs fetched 
 ' into RstChild. 
Rst1.MovePrevious ' RstChild now holds cached rs, saving round trip. 
... 
```

2 つ以上のパラメーターが指定されたクエリでは、すべてのパラメーター値がキャッシュに入れられた値と等しい場合のみ、キャッシュに入れられた子が使用されます。

## <a name="parameterized-commands-and-complex-parent-child-relations"></a>パラメーター化されたコマンドと複雑な親子関係

パラメーター化されたコマンドを使用すると、等結合タイプの階層のパフォーマンスを向上できるだけでなく、より複雑な親子関係をサポートできます。 たとえば、チーム (チーム ID、チーム名) と他のゲーム (日付、ホーム チーム、訪問チーム) で構成される 2 つのテーブルを持つ Little League データベースを \_ \_ \_ 検討 \_ します。

非パラメーター化階層を使用する場合、各チームの子 **Recordset** にその完全な日程が含まれるように、チーム テーブルと試合テーブルを関連付けることはできません。 ホームの日程または遠征の日程のいずれかを含むチャプターを作成することはできますが、両方を含むチャプターは作成できません。 これは、RELATE 句では、親子関係が (pc1=cc1) AND (pc2=pc2) 形式に制限されるためです。 したがって、コマンドに "RELATE team id TO home \_ team, team id TO visiting team"が含まれている場合は、チームがプレイしているゲームのみを \_ \_ \_ 取得します。 必要なのが "(team \_ id=home \_ team) OR (team \_ id=visiting team)"ですが、Shape プロバイダーは OR 句 \_ をサポートしていない。

必要な結果を取得するには、パラメーター化されたコマンドを使用します。次に例を示します。

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

この例では、必要な結果を取得するため、より柔軟に SQL WHERE 句を利用しています。

