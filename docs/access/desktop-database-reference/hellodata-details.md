---
title: HelloData の詳細 (デスクトップ データベース参照のアクセス)
TOCTitle: HelloData Details
ms:assetid: db51e15c-1b5b-c64a-2f84-34dd0e78c6cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250105(v=office.15)
ms:contentKeyID: 48548103
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6de174362e014af3e90686e53a563a10e04ec665
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477628"
---
# <a name="hellodata-details"></a>HelloData の詳細


**適用されます**Access 2013 |。Office 2013

HelloData アプリケーションは、一般的な ADO アプリケーションの基本操作手順: 取得、検査、編集、およびデータを更新します。 アプリケーションを起動するときは、最初のボタンでは、**データの取り込み**をクリックします。 GetData() サブルーチンが実行されます。

## <a name="getdata"></a>GetData

GetData は、モジュール レベル変数に有効な接続文字列を配置*m\_sConnStr*。 接続文字列の詳細については、「 [接続文字列を作成する](creating-the-connection-string.md)」を参照してください。

Visual Basic の**OnError**ステートメントを使用してエラー ハンドラーを割り当てます。 ADO のエラー処理の詳細についてを参照してください[第 6 章: エラー処理](chapter-6-error-handling.md)。 新しい**接続**オブジェクトを作成すると、および HelloData の例は、*切断されたレコード セット*を作成するために、 **CursorLocation**プロパティが**adUseClient**に設定されています。 つまり、データがデータ ソースからフェッチされる、データ ソースとの物理的な接続が切断された場合が、まだ使用できます、キャッシュされたデータをローカルで、 **Recordset**オブジェクトにします。

接続後、SQL 文字列を変数 (sSQL) に割り当てます。 新規の**Recordset**オブジェクトのインスタンスを作成し、m\_oRecordset1。 コードの次の行では、既存の**接続**に渡すことで**レコード セット**を開きます。 コードの次の行には、既存の**接続**、**レコード セット**のソースとして sSQL に渡すことで**レコード セット**を開きます。 ADO は**レコード セット**のソースとして渡された SQL 文字列では、コマンドのテキストの定義を**レコード セット**を**開く**方法を最後の引数で**adCmdText**を渡すことによって決定を行うために役立ちます。 この行は、 **LockType**も設定し、 **CursorType**は、**レコード セット**に関連付けられています。

次の行のコードでは、 **MarshalOptions** プロパティを **adMarshalModifiedOnly** に設定します。 **MarshalOptions** は、中間層 (または Web サーバー) にマーシャリングされるレコードを示します。 マーシャリングの詳細については、COM のマニュアルを参照してください。 **AdMarshalModifiedOnly**を使用してクライアント側カーソルがある場合 ([CursorLocation](cursorlocation-property-ado.md) = **adUseClient**)、クライアント上で変更されたレコードのみを中間層に書き戻す。 **MarshalOptions** を **adMarshalModifiedOnly** に設定すると、マーシャリングされる行が少なくなり、パフォーマンスが向上する場合があります。

次に、 **ActiveConnection** プロパティを **Nothing** に設定して **Recordset** を切断します。詳細については、「5 章: データを更新し、保存する」の「 [レコードセットを切断し、再接続する](disconnecting-and-reconnecting-the-recordset.md)」を参照してください。

データ ソースへの接続を閉じ、既存の **Connection** オブジェクトを破棄して、使用していたリソースを解放します。

最後に、フォーム上で Microsoft DataBound Grid Control の **DataSource** として **Recordset** を設定し、 **Recordset** のデータをフォームに簡単に表示できるようにします。

**データを調べて**、2 番目のボタンをクリックします。 ExamineData サブルーチンが実行されます。

## <a name="examinedata"></a>ExamineData

ExamineData では、**Recordset** オブジェクトのさまざまなメソッドやプロパティを使用して、**Recordset** のデータに関する情報を表示します。**RecordCount** プロパティを使用してレコード数を表示します。**Recordset** をループ処理し、フォームの表示テキスト ボックスに **AbsolutePosition** プロパティの値を表示します。また、ループ処理中に、3 番目のレコードの **Bookmark** プロパティの値が、後で使用するために、バリアント型の変数 *vBookmark* に配置されます。

ルーチンの処理は、前に格納されたブックマーク変数を使用して、直接 3 番目のレコードに戻ります。WalkFields サブルーチンを呼び出して、 **Recordset** の **Fields** コレクションをループ処理し、コレクション内の各 **Field** の詳細を表示します。

最後に、ExamineData は **Recordset** の **Filter** プロパティを使用して、CategoryId が 2 のレコードのみを表示します。このフィルターを適用した結果は、フォームの表示グリッドですぐに確認できます。

ExamineData サブルーチンで使用されている機能の詳細については、「[3 章: データを調べる](chapter-3-examining-data.md)」を参照してください。

次に、3 番目のボタンでは、**データの編集**] をクリックします。 EditData サブルーチンが実行されます。

## <a name="editdata"></a>EditData

EditData サブルーチンが実行されるときも、 **Recordset** には CategoryId が 2 というフィルターが適用されたままなので、フィルター条件を満たす項目だけが表示されます。まず、 **Recordset** をループ処理し、 **Recordset** の表示項目の価格を 10% ずつ増やします。 **Price** フィールドの値を変更するには、そのフィールドの **Value** プロパティを新しい有効な金額に設定します。

**Recordset** はデータ ソースからは切断されています。EditData による変更は、ローカルにキャッシュされたデータのコピーにのみ適用されます。詳細については、「 [4 章: データを編集する](chapter-4-editing-data.md)」を参照してください。

変更できません。 データ ソースに**データの更新**、4 番目のボタンをクリックするまでです。 UpdateData サブルーチンが実行されます。

## <a name="updatedata"></a>UpdateData

UpdateData は、まず **Recordset** に適用されたフィルターを削除します。 コードは、削除し、フィルター処理されていない**レコード セット**がグリッドに表示されるように、**データ ソース**として、Microsoft バインド データ グリッドのフォームにリセットします。

次に、 **adMovePrevious** 引数を持つ **Supports** メソッドを使用して、 **Recordset** 内で後方へ移動できるかどうかを確認します。

ルーチンは **MoveFirst** メソッドを使用して最初のレコードに移動し、 **Field** オブジェクトの **OriginalValue** プロパティと **Value** プロパティを使用して、フィールドの元の値と現在の値を表示します。これらのプロパティと **UnderlyingValue** プロパティ (ここでは使用しません) については、「 [5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。

次に、新しい **Connection** オブジェクトが作成され、このオブジェクトを使用してデータ ソースへの接続が再確立されます。 **Recordset** をデータ ソースに再接続するには、新しい **Connection** を **Recordset** の **ActiveConnection** として設定します。更新内容をサーバーに送信するために、 **Recordset** の **UpdateBatch** を呼び出します。

場合、バッチ更新が成功すると、モジュール レベルのフラグ変数、True に設定します。 これは、データベースに対して行ったすべての変更を後で取り消すための目印になります。

最後に、 **Recordset** 内の最初のレコードに戻り、元の値と現在の値を表示します。値は、 **UpdateBatch** を呼び出した後と同じです。

**Recordset** の切断中にサーバーのデータが変更された場合の対処など、データの更新の詳細については、「 [5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。

## <a name="formunload"></a>フォーム\_アンロード

フォーム\_アンロード サブルーチンが、重要ないくつかの理由です。 最初、これは、サンプル アプリケーション、フォーム、\_アンロードは、アプリケーションが終了する前にデータベースに加えられた変更をクリーンアップします。 次に、開いている **Connection** オブジェクトから **Execute** メソッドを使用してコマンドを直接実行する方法を示していることです。 最後に、データ ソースに対して以外の行を返さないクエリ (UPDATE クエリ) を実行する例を示します。

