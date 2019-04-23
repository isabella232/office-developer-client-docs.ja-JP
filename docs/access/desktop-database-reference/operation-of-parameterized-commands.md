---
title: パラメーター化コマンドの操作
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 145a2ee6c3d3c614eb9660350a0bb8a00d44d04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288288"
---
# <a name="operation-of-parameterized-commands"></a>パラメーター化コマンドの操作

**適用先:** Access 2013、Office 2013

大きな子 **Recordset** を処理するとき、特に親 **Recordset** のサイズと比べて大きいにもかかわらず、わずかな子チャプターにアクセスするだけの場合は、パラメーター化コマンドを使用する方が効率的です。

*非パラメーター化コマンド*は、親と子の両方の**recordset**全体を取得し、チャプター列を親に追加して、親の各行に関連する子チャプターへの参照を割り当てます。

*パラメーター化*されたコマンドは親**recordset**全体を取得しますが、チャプター列にアクセスしたときにはチャプター **recordset**のみを取得します。 This difference in retrieval strategy can yield significant performance benefits.

たとえば、次のように指定することができます。

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

親と子のテーブルには、共通の cust\_id の列名があり*ます。* *child-command* には、RELATE 句の参照先 ("...PARAMETER 0") へのプレースホルダー "?" が指定されています。

> [!NOTE]
> [!メモ] PARAMETER 句は、Shape コマンドの構文にのみ影響します。ADO の [Parameter](parameter-object-ado.md) オブジェクトまたは [Parameters](parameters-collection-ado.md) コレクションとは関係ありません。

パラメーター化された Shape コマンドが実行されると、次のようになります。

1.  *parent-command* が実行され、Customers テーブルから親 **Recordset** が返されます。

2.  チャプター列が親 **Recordset** に追加されます。

3.  親の行のチャプター列にアクセスすると、customer の値を使用して*子コマンド*が実行されます\_。 cust id は、パラメーターの値として指定します。

4.  手順3で作成したデータプロバイダーの行セット内のすべての行を使用して、子**Recordset**にデータを設定します。 この例では、Orders テーブルには、cust\_id が customers\_id の値と等しい行がすべて含まれています。 既定では、親**recordset**への参照がすべて解放されるまで、子**recordset**s はクライアント上にキャッシュされます。 この動作を変更するには、 **Recordset**の[動的プロパティ](ado-dynamic-property-index.md)**キャッシュの子の行**を**False**に設定します。

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

パラメーター化されたコマンドを使用すると、等結合タイプの階層のパフォーマンスを向上できるだけでなく、より複雑な親子関係をサポートできます。 \_たとえば、teams (チーム id、チーム\_名) と、その他のゲーム (日付、自宅\_チーム、訪問\_チーム) の2つのテーブルで構成されるちょっとしたリーグデータベースを考えてみます。

非パラメーター化階層を使用する場合、各チームの子 **Recordset** にその完全な日程が含まれるように、チーム テーブルと試合テーブルを関連付けることはできません。 ホームの日程または遠征の日程のいずれかを含むチャプターを作成することはできますが、両方を含むチャプターは作成できません。 これは、RELATE 句では、親子関係が (pc1=cc1) AND (pc2=pc2) 形式に制限されるためです。 \_そのため、「team id からホーム\_チームへのチーム id への\_\_関連付け」というコマンドを使用した場合、チームが自分たちをプレイしていたゲームのみが表示されます。 必要なのは、"(\_チーム id =\_ホームチーム)" また\_は (team\_id = 訪問チーム) "ですが、Shape プロバイダーは OR 句をサポートしていません。

必要な結果を取得するには、パラメーター化されたコマンドを使用します。次に例を示します。

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

この例では、必要な結果を取得するため、より柔軟に SQL WHERE 句を利用しています。

