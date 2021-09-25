---
title: Open メソッド (ADO Recordset)
TOCTitle: Open method (ADO Recordset)
ms:assetid: 87ef19a4-28e1-dec7-ed33-4ae500b9c460
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249591(v=office.15)
ms:contentKeyID: 48546119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ffe4c6de4bf89a49df3daabca0a5a99b21210814
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589317"
---
# <a name="open-method-ado-recordset"></a>Open メソッド (ADO Recordset)

**適用先**: Access 2013、Office 2013

カーソルを開きます。

## <a name="syntax"></a>構文

*recordset*.オープン *ソース*、 *ActiveConnection*、 *CursorType*、 *LockType*、 *Options*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |省略可能です。有効な **Command** オブジェクト、SQL ステートメント、テーブル名、ストアド プロシージャの呼び出し、URL、または永続的に保存された [Recordset](command-object-ado.md) を格納しているファイル名や [Stream](stream-object-ado.md) オブジェクト名に評価されるバリアント型 ( [Variant](recordset-object-ado.md) ) の値を指定します。|
|*ActiveConnection* |省略可能です。有効な **Connection** オブジェクトのオブジェクト変数名に評価されるバリアント型 ( [Variant](connection-object-ado.md) ) の値、または **ConnectionString** パラメーターを含む文字列型 ( [String](connectionstring-property-ado.md) ) の値を指定します。|
|*CursorType* |省略可能です。プロバイダーが [Recordset](cursortypeenum.md) を開くときに使用するカーソルの種類を決める **CursorTypeEnum** 値を指定します。既定値は **adOpenForwardOnly** です。|
|*LockType* |省略可能です。プロバイダーが [Recordset](locktypeenum.md) を開くときに使用するロック (同時作用) の種類を決めるための **LockTypeEnum** 値を指定します。既定値は **adLockReadOnly** です。|
|*Options* |省略可能です。*Source* 引数が **Command** オブジェクト以外のソースを表す場合にプロバイダーがこの引数を評価する方法、または以前に保存されていたファイルから **Recordset** を復元する必要があることを示す長整数型 (**Long**) の値を指定します。1 つまたは複数の [CommandTypeEnum](commandtypeenum.md) 値または [ExecuteOptionEnum](executeoptionenum.md) 値を指定できます。これらの値は、ビット単位の AND 演算子で組み合わせて使用することができます。|

> [!NOTE]
> 永続化された **Recordset** を含む **Stream** から **Recordset** を開く場合、**ExecuteOptionEnum** 値の **adAsyncFetchNonBlocking** を使用しても無効です。この場合、フェッチは同期であり、ブロッキングが行われます。

**Open** メソッドを使用する場合は、**ExecuteOpenEnum** に **adExecuteNoRecords** または **adExecuteStream** を指定しないでください。

## <a name="remarks"></a>注釈

ADO の **Recordset** の既定のカーソルは、サーバー側にある読み取り専用の前方スクロール カーソルです。

**Recordset** オブジェクトで **Open** メソッドを使用すると、ベース テーブルからのレコード、クエリの結果、または以前に保存された **Recordset** を表すカーソルを開くことができます。

オプションの *Source* 引数を使用して **、Command** オブジェクト変数、SQL ステートメント、ストアド プロシージャ、テーブル名、URL、または完全なファイル パス名のいずれかを使用してデータ ソースを指定します。 Source *が* ファイル パス名の場合は、完全パス ("c: \\ dir \\ file.rst")、相対パス (".) を指定できます。 \\file.rst")、または URL (" https://files/file.rst ")。

**Open** メソッドの *Source* 引数を使用して、レコードを返さないアクション クエリを実行するのは、お勧めできません。これは、呼び出しが成功したかどうかを容易に判断できないためです。このようなクエリによって返された **Recordset** は閉じられます。SQL INSERT ステートメントのように、レコードを返さないクエリを実行する場合は、代わりに **Command** オブジェクトの [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) メソッドまたは **Connection** オブジェクトの [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) メソッドを呼び出してください。

*ActiveConnection* 引数は [ActiveConnection](activeconnection-property-ado.md) プロパティに対応し、**Recordset** オブジェクトを開く接続を指定します。 この引数に接続の定義を指定すると、ADO により、指定されたパラメーターを使用して新しい接続が開かれます。 クライアント側カーソル **(CursorLocation**   =  **adUseClient)** を使用して Recordset を開いてから、このプロパティの値を変更して、更新プログラムを別のプロバイダーに送信できます。 また、このプロパティを **Nothing** (Microsoft Visual Basic の場合) または NULL に設定すると、その **Recordset** を任意のプロバイダーから切断することができます。 ただし、サーバー側カーソルの **ActiveConnection** を変更すると、エラーが発生します。

**Recordset** オブジェクトのプロパティに直接対応するその他の引数 (*Source*、*CursorType*、および *LockType*) と、プロパティの関係は次のとおりです。

- **Recordset** オブジェクトを開く前のプロパティは、読み取り/書き込み可能です。

- **Open** メソッドの実行時に、対応する引数を指定しないと、プロパティの設定値が使用されます。引数を指定した場合は、対応するプロパティの設定値が上書きされて引数の値に更新されます。

- **Recordset** オブジェクトを開いた後、プロパティは読み取り専用になります。

> [!NOTE]
> **Recordset** オブジェクトの [Source](source-property-ado-recordset.md) プロパティに有効な **Command** オブジェクトが設定されている場合、その **Recordset** オブジェクトが開いていなくても、**ActiveConnection** プロパティは読み取り専用になります。

*Source* 引数に **Command** オブジェクトを指定する場合、同時に *ActiveConnection* 引数を指定すると、エラーが発生します。**Command** オブジェクトの **ActiveConnection** プロパティは、あらかじめ有効な **Connection** オブジェクトまたは接続文字列に設定しておく必要があります。

*Source* 引数に **Command** オブジェクト以外のソースを指定する場合は、*Options* 引数を使用して *Source* 引数の評価を最適化することができます。*Options* 引数が定義されていない場合は、パフォーマンスが低下する可能性があります。これは、引数が SQL ステートメント、ストアド プロシージャ、URL、テーブル名のいずれであるかを判断するために、プロバイダーを呼び出す必要があるためです。使用する *Source* の種類がわかっている場合は、*Options* 引数を設定することにより、該当するコードに直接ジャンプすることができます。*Options* 引数が *Source* の種類と一致しない場合は、エラーが発生します。

*Source* 引数に **Stream** オブジェクトを指定する場合は、他の引数は指定しないでください。そのようにすると、エラーが発生します。**Stream** から **Recordset** を開く場合は、**ActiveConnection** の情報は保持されません。

**Recordset** に接続が関連付けられていない場合、*Options* 引数の既定値は **adCmdFile** です。代表的な例では、永続的に保存された **Recordset** オブジェクトの場合がこれに該当します。

データ ソースがレコードを返さない場合、プロバイダーは [BOF](bof-eof-properties-ado.md) プロパティと [EOF](bof-eof-properties-ado.md) プロパティを **True** に設定し、カレント レコードの位置が未定義になります。カーソルの種類によっては、この空の **Recordset** オブジェクトに新しいデータを追加することができます。

開いている **Recordset** に対する操作が完了したら、[Close](close-method-ado.md) メソッドを使用して、関連するシステム リソースをすべて解放します。オブジェクトを閉じてもメモリからは削除されないので、そのオブジェクトのプロパティを変更したり、**Open** メソッドを使用してもう一度開いたりすることができます。オブジェクトをメモリから完全に削除するには、オブジェクト変数に *Nothing* を設定します。

**ActiveConnection プロパティを設定** する前に、オペランドを指定しない **Open** を呼び出して **、Recordset Fields** コレクションにフィールドを追加して作成した Recordset のインスタンス **を**[作成](fields-collection-ado.md)します。

[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定している場合は、非同期に行を取得できる方法が 2 つあります。 推奨される方法は、*Options* を **adAsyncFetch** に設定することです。 もう 1 つの方法として、 [Properties](properties-collection-ado.md) コレクションで "非同期行セット処理" ダイナミック プロパティを使用することもできますが、 **Options** パラメーターを **adAsyncFetch** に設定していない場合は、関連して取得されたイベントが失われる可能性があります。

> [!NOTE]
> MS Remote プロバイダーのバックグラウンド フェッチは、**Open** メソッドの *Options* パラメーターを通してのみサポートされます。

> [!NOTE]
> [!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、「絶対 URL と [相対 URL」を参照してください](absolute-and-relative-urls.md)。


