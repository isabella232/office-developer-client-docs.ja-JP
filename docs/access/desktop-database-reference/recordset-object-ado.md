---
title: Recordset オブジェクト (ADO)
TOCTitle: Recordset object (ADO)
ms:assetid: 0f963bf8-f066-dc8a-b754-f427de712df1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248865(v=office.15)
ms:contentKeyID: 48543267
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a99b3f792518e65900841bab90977e2edda6e804
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927040"
---
# <a name="recordset-object-ado"></a>Recordset オブジェクト (ADO)

**適用されます**Access 2013、Office 2013。

基になるテーブルのレコードセット全体、またはコマンドの実行によって返された結果を表します。 **Recordset** オブジェクトでは、常にレコードセット内の 1 つのレコードのみをカレント レコードとして参照します。

## <a name="remarks"></a>備考

プロバイダーのデータを操作するには、 **Recordset** オブジェクトを使用します。ADO を使用する場合は、 **Recordset** オブジェクトを使用してほぼすべてのデータを操作します。すべての **Recordset** オブジェクトは、レコード (行) とフィールド (列) から構成されています。プロバイダーがサポートする機能によっては、一部の **Recordset** のメソッドまたはプロパティを使用できない場合があります。

ADODB.Recordset は、 **Recordset** オブジェクトの作成時に使用する ProgID です。古くなった ADOR.Recordset ProgID を参照する既存のアプリケーションは、再コンパイルせずそのまま使用できますが、新たに開発するアプリケーションは、ADODB.Recordset を参照する必要があります。

ADO では、次の 4 種類のカーソルが定義されています。

  - **動的カーソル**: 他のユーザーによる追加、変更、および削除を表示でき、ブックマークに依存しない **Recordset** 内でのすべての種類の移動が可能で、プロバイダーがブックマークをサポートしている場合にブックマークを許可します。

  - **キーセット カーソル**: 他のユーザーが追加したレコードを表示できない点と、他のユーザーが削除したレコードにアクセスできない点を除けば、動的カーソルと同様に動作します。他のユーザーが変更したデータは表示できます。常にブックマークをサポートするため、 **Recordset** 内でのすべての種類の移動が可能です。

  - **静的カーソル**: データの検索やレポートの生成に使用できるレコードのセットの静的コピーを提供します。常にブックマークを許可するため、 **Recordset** 内でのすべての種類の移動が可能です。他のユーザーによる追加、変更、または削除は表示されません。これは、クライアント側 **Recordset** オブジェクトを開いたときに許可されるただ 1 種類のカーソルです。

  - **前方スクロール カーソル**: **Recordset** 内で前方向のスクロールのみ許可します。他のユーザーによる追加、変更、または削除は表示されません。 **Recordset** のスクロールが 1 回だけで十分な場合は、これによってパフォーマンスを向上できます。

カーソルの種類を選択する**レコード セット**を開く前に[CursorType](cursortype-property-ado.md)プロパティを設定するか、 [Open](open-method-ado-recordset.md)メソッドを使用して*CursorType*引数を渡します。 プロバイダーによっては、カーソルのすべての種類をサポートしていないものもあります。 プロバイダーのマニュアルを確認してください。 カーソルの種類を指定しない場合、ADO では既定で前方スクロール カーソルが開かれます。

[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定して **Recordset** を開く場合、 **Field** オブジェクトの [UnderlyingValue](field-object-ado.md) プロパティは、返された **Recordset** オブジェクトでは使用できません。一部のプロバイダーと共に使用すると (たとえば、Microsoft ODBC Provider for OLE DB を Microsoft SQL Server と組み合わせて)、 **Open** メソッドで接続文字列を渡すことによって、 [Recordset](connection-object-ado.md) オブジェクトを前に定義した **Connection** オブジェクトと無関係に作成できます。ADO は、この場合も [Connection](connection-object-ado.md) オブジェクトを作成しますが、このオブジェクトをオブジェクト変数に割り当てることはありません。ただし、同じ接続上で複数の **Recordset** オブジェクトを開く場合、明示的に **Connection** オブジェクトを作成して開く必要があります。こうすることで、 **Connection** オブジェクトがオブジェクト変数に割り当てられます。 **Recordset** オブジェクトを開くときにこのオブジェクト変数を使用しなかった場合、同じ接続文字列を渡しても、ADO によって新しい各 **Recordset** に新しい **Connection** オブジェクトが作成されます。

**Recordset** オブジェクトは必要な数だけ作成できます。

**Recordset** を開くと、カレント レコードは最初のレコード (ある場合) の位置に置かれ、 [BOF](bof-eof-properties-ado.md) プロパティと [EOF](bof-eof-properties-ado.md) プロパティは **False** に設定されます。レコードがない場合、 **BOF** プロパティと **EOF** プロパティの設定値は **True** になります。

[MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)、**MoveLast**、**MoveNext** と **MovePrevious** の各メソッド、[Move](move-method-ado.md) メソッド、および [AbsolutePosition](absoluteposition-property-ado.md)、[AbsolutePage](absolutepage-property-ado.md) と [Filter](filter-property-ado.md) の各プロパティを使用すると、プロバイダーが関連する機能をサポートしているものとして、カレント レコードの位置を変更できます。前方スクロール タイプの **Recordset** オブジェクトは、[MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) メソッドのみをサポートします。**Move** メソッドを使用して各レコードに移動 (または **Recordset** を列挙) する場合、**BOF** プロパティと **EOF** プロパティを使用すると、**Recordset** の範囲を超えたかどうかを確認できます。

**Recordset** オブジェクトは、イミディエイト更新とバッチ更新の 2 種類の更新をサポートできます。イミディエイト更新では、 [Update](update-method-ado.md) メソッドを呼び出すと、データに対するすべての変更が直ちに基になるデータ ソースに書き込まれます。また、 [AddNew](addnew-method-ado.md) メソッドと **Update** メソッドを使用して、値の配列をパラメーターとして渡し、レコード内の複数のフィールドを同時に更新することもできます。

プロバイダーがバッチ更新をサポートしている場合は、プロバイダーによって複数のレコードに対する変更をキャッシュしてから、[UpdateBatch](updatebatch-method-ado.md) メソッドを使用して、データベースを一度呼び出すだけで変更内容をまとめて転送できます。この操作は、 **AddNew** 、 **Update** 、および [Delete](delete-method-ado-recordset.md) の各メソッドを使用して変更を行った場合に適用されます。 **UpdateBatch** メソッドの呼び出し後、 [Status](status-property-ado-recordset.md) プロパティを使用すると、データの競合があるかどうかを確認して解決できます。

> [!NOTE]
> [!メモ] [Command](command-object-ado.md) オブジェクトを使用せずにクエリを実行するには、クエリ文字列を **Recordset** オブジェクトの **Open** メソッドに渡します。ただし、コマンド テキストを永続化して再実行するか、クエリ パラメーターを使用する場合は、 **Command** オブジェクトが必要となります。

[Mode](mode-property-ado.md) プロパティは、アクセス権限を制御します。

**Fields** コレクションは **Recordset** オブジェクトの既定のメンバーです。結果として、次の 2 つのコード ステートメントは同じになります。

```vb
    Debug.Print objRs.Fields.Item(0)  ' Both statements print 
    Debug.Print objRs(0)              '  the Value of Item(0).
```
