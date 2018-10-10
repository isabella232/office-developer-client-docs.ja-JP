---
title: パラメーター化コマンドの操作
TOCTitle: Operation of Parameterized Commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42f0e8ffc7472dbf8a8c03fa320d3ae2b4a2e21b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479500"
---
# <a name="operation-of-parameterized-commands"></a>パラメーター化コマンドの操作


**適用されます**Access 2013 |。Office 2013

大きな子 **Recordset** を処理するとき、特に親 **Recordset** のサイズと比べて大きいにもかかわらず、わずかな子チャプターにアクセスするだけの場合は、パラメーター化コマンドを使用する方が効率的です。

*非パラメーター化コマンド*は、全体の親と子の両方**のレコード セット**を取得、チャプター列を親に追加し、親の各行に対して関連する子チャプターへの参照を割り当てます。

*パラメーター化されたコマンド*は、全体の親**レコード セット**を取得しますが、チャプター列にアクセスするときは、該当する章だけ**のレコード セット**を取得します。 この取得方法の違いは、重大なパフォーマンス上のメリットを得します。

たとえば、次のように指定することができます。

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

親と子テーブルがある列の名前、共通の顧客に\_*.* の id *子コマンド*には"?"プレース ホルダー、RELATE 句の参照先 (つまり、".パラメーター 0") です。


> [!NOTE]
> <P>[!メモ] PARAMETER 句は、Shape コマンドの構文にのみ影響します。ADO の <A href="parameter-object-ado.md">Parameter</A> オブジェクトまたは <A href="parameters-collection-ado.md">Parameters</A> コレクションとは関係ありません。</P>



パラメーター化された Shape コマンドが実行されると、次のようになります。

1.  *親コマンド*が実行され、Customers テーブルから親**レコード セット**を返します。

2.  チャプター列が親 **Recordset** に追加されます。

3.  Customer.cust の値を使用して、*子コマンド*を実行する親の行のチャプター列にアクセス、\_、パラメーターの値としての id です。

4.  手順 3 で作成したデータ プロバイダーの行セット内のすべての行を使用して、子**レコード セット**を作成します。 [受注] テーブルのすべての行は、この例では、顧客\_id customer.cust の値に等しい\_id です。 既定では、子**recordset**は、クライアント上でキャッシュ親**レコード セット**に対するすべての参照が解放されるまで。 この動作を変更するのには**false を指定**する**レコード セット**の[動的プロパティ](ado-dynamic-property-index.md)**キャッシュの子の行**を設定します。

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

パラメーター化されたコマンドを使用すると、等結合タイプの階層のパフォーマンスを向上できるだけでなく、より複雑な親子関係をサポートできます。 例えば、2 つのテーブルを持つ少年野球リーグ データベース: チームで構成される 1 つ (チーム\_id、チーム\_名) およびその他のゲームの (日付、ホーム\_チーム、訪問\_チーム)。

非パラメーター化階層を使用する場合、各チームの子 **Recordset** にその完全な日程が含まれるように、チーム テーブルと試合テーブルを関連付けることはできません。 ホームの日程または遠征の日程のいずれかを含むチャプターを作成することはできますが、両方を含むチャプターは作成できません。 これは、RELATE 句では、親子関係が (pc1=cc1) AND (pc2=pc2) 形式に制限されるためです。 コマンドが含まれている場合、"関連チーム\_id にホーム\_チーム、チーム\_訪問する id\_チーム"、ゲームのみの取得は、チームが再生された自体です。 必要な」(チーム\_id ホーム =\_チーム) または (チーム\_id = 訪問\_チーム)」、Shape プロバイダーは、OR 句をサポートしていませんが。

必要な結果を取得するには、パラメーター化されたコマンドを使用します。次に例を示します。

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

この例では、必要な結果を取得するため、より柔軟に SQL WHERE 句を利用しています。

