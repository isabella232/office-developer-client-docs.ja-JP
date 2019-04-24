---
title: HelloData details (Access デスクトップデータベースリファレンス)
TOCTitle: HelloData details
ms:assetid: db51e15c-1b5b-c64a-2f84-34dd0e78c6cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250105(v=office.15)
ms:contentKeyID: 48548103
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 78b04b74d4e2b8d9c215235d6e7ccebed4fa2ef2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292000"
---
# <a name="hellodata-details"></a>HelloData の詳細


**適用先:** Access 2013、Office 2013

The HelloData application steps through the basic operations of a typical ADO application: getting, examining, editing, and updating data. When you start the application, click the first button, **Get Data**. This will run the GetData() subroutine.

## <a name="getdata"></a>GetData

GetData は、有効な接続文字列をモジュールレベルの変数*m\_sconnstr*に格納します。 接続文字列の詳細については、「 [接続文字列を作成する](creating-the-connection-string.md)」を参照してください。

Assign an error handler using a Visual Basic **OnError** statement. For more information about error handling in ADO, see [Chapter 6: Error Handling](chapter-6-error-handling.md). 新しい**Connection**オブジェクトが作成され、HelloData **** の例では切断された*Recordset*が作成されるので、このプロパティは**adUseClient**に設定されています。 This means that once the data has been fetched from the data source, the physical connection with the data source is broken, but you can still work with the data that is cached locally in your **Recordset** object.

接続後、SQL 文字列を変数 (sSQL) に割り当てます。 その後、新しい**Recordset**オブジェクト m\_oRecordset1 をインスタンス化します。 次のコード行で、既存の**接続**を介して**Recordset**を開き、を渡します。 コードの次の行で、既存の**接続**を介して**recordset**を開き、 **recordset**のソースとして ssql を渡します。 You assist ADO in making the determination that the SQL string you have passed as the source for the **Recordset** is a textual definition of a command by passing **adCmdText** in the final argument to the **Recordset** **Open** method. This line also sets the **LockType** and **CursorType** associated with the **Recordset**.

次の行のコードでは、 **MarshalOptions** プロパティを **adMarshalModifiedOnly** に設定します。 **marshaloptions**は、中間層 (または web サーバー) にマーシャリングするレコードを示します。 マーシャリングの詳細については、COM のマニュアルを参照してください。 クライアント側カーソル ([cursor location](cursorlocation-property-ado.md) = **adUseClient**) で**adMarshalModifiedOnly**を使用する場合、クライアント上で変更されたレコードのみが中間層に書き戻されます。 **MarshalOptions** を **adMarshalModifiedOnly** に設定すると、マーシャリングされる行が少なくなり、パフォーマンスが向上する場合があります。

次に、 **ActiveConnection** プロパティを **Nothing** に設定して **Recordset** を切断します。詳細については、「5 章: データを更新し、保存する」の「 [レコードセットを切断し、再接続する](disconnecting-and-reconnecting-the-recordset.md)」を参照してください。

データ ソースへの接続を閉じ、既存の **Connection** オブジェクトを破棄して、使用していたリソースを解放します。

最後に、フォーム上で Microsoft DataBound Grid Control の **DataSource** として **Recordset** を設定し、 **Recordset** のデータをフォームに簡単に表示できるようにします。

Click the second button, **Examine Data**. This runs the ExamineData subroutine.

## <a name="examinedata"></a>ExamineData

ExamineData では、**Recordset** オブジェクトのさまざまなメソッドやプロパティを使用して、**Recordset** のデータに関する情報を表示します。**RecordCount** プロパティを使用してレコード数を表示します。**Recordset** をループ処理し、フォームの表示テキスト ボックスに **AbsolutePosition** プロパティの値を表示します。また、ループ処理中に、3 番目のレコードの **Bookmark** プロパティの値が、後で使用するために、バリアント型の変数 *vBookmark* に配置されます。

ルーチンの処理は、前に格納されたブックマーク変数を使用して、直接 3 番目のレコードに戻ります。WalkFields サブルーチンを呼び出して、 **Recordset** の **Fields** コレクションをループ処理し、コレクション内の各 **Field** の詳細を表示します。

最後に、ExamineData は **Recordset** の **Filter** プロパティを使用して、CategoryId が 2 のレコードのみを表示します。このフィルターを適用した結果は、フォームの表示グリッドですぐに確認できます。

ExamineData サブルーチンで使用されている機能の詳細については、「[3 章: データを調べる](chapter-3-examining-data.md)」を参照してください。

Next, click the third button, **Edit Data**. This will run the EditData subroutine.

## <a name="editdata"></a>EditData

EditData サブルーチンが実行されるときも、 **Recordset** には CategoryId が 2 というフィルターが適用されたままなので、フィルター条件を満たす項目だけが表示されます。まず、 **Recordset** をループ処理し、 **Recordset** の表示項目の価格を 10% ずつ増やします。 **Price** フィールドの値を変更するには、そのフィールドの **Value** プロパティを新しい有効な金額に設定します。

**Recordset** はデータ ソースからは切断されています。EditData による変更は、ローカルにキャッシュされたデータのコピーにのみ適用されます。詳細については、「 [4 章: データを編集する](chapter-4-editing-data.md)」を参照してください。

The changes will not be made on the data source until you click the fourth button, **Update Data**. This will run the UpdateData subroutine.

## <a name="updatedata"></a>UpdateData

UpdateData は、まず **Recordset** に適用されたフィルターを削除します。 このコードは、フィルターを使用しない**Recordset**がグリッドに表示されるように、フォーム上の Microsoft Bound DataGrid の**DataSource**として削除およびリセットします。

次に、 **adMovePrevious** 引数を持つ **Supports** メソッドを使用して、 **Recordset** 内で後方へ移動できるかどうかを確認します。

ルーチンは **MoveFirst** メソッドを使用して最初のレコードに移動し、 **Field** オブジェクトの **OriginalValue** プロパティと **Value** プロパティを使用して、フィールドの元の値と現在の値を表示します。これらのプロパティと **UnderlyingValue** プロパティ (ここでは使用しません) については、「 [5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。

次に、新しい **Connection** オブジェクトが作成され、このオブジェクトを使用してデータ ソースへの接続が再確立されます。 **Recordset** をデータ ソースに再接続するには、新しい **Connection** を **Recordset** の **ActiveConnection** として設定します。更新内容をサーバーに送信するために、 **Recordset** の **UpdateBatch** を呼び出します。

バッチ更新が正常に終了すると、モジュールレベルのフラグ変数が True に設定されます。 これは、データベースに対して行ったすべての変更を後で取り消すための目印になります。

最後に、 **Recordset** 内の最初のレコードに戻り、元の値と現在の値を表示します。値は、 **UpdateBatch** を呼び出した後と同じです。

**Recordset** の切断中にサーバーのデータが変更された場合の対処など、データの更新の詳細については、「 [5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。

## <a name="formunload"></a>フォーム\_のアンロード

Form\_Unload サブルーチンは、いくつかの理由から重要です。 最初に、これはサンプルアプリケーションなので\_、フォームのアンロードでは、アプリケーションが終了する前にデータベースに加えられた変更がクリーンアップされます。 次に、開いている **Connection** オブジェクトから **Execute** メソッドを使用してコマンドを直接実行する方法を示していることです。 最後に、データ ソースに対して行を返さないクエリ (UPDATE クエリ) を実行する例を示していることです。

