---
title: Open メソッド (ADO Recordset)
TOCTitle: Open Method (ADO Recordset)
ms:assetid: 87ef19a4-28e1-dec7-ed33-4ae500b9c460
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249591(v=office.15)
ms:contentKeyID: 48546119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd5a956d5a978a374e10c85e7803715f81d48f2a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603078"
---
# <a name="open-method-ado-recordset"></a>Open メソッド (ADO Recordset)


**適用されます**Access 2013 |。Office 2013


カーソルを開きます。

## <a name="syntax"></a>構文

*レコード セット*です。*ソース*、 *ActiveConnection*、 *CursorType*、 *LockType*、*オプション*を開く

## <a name="parameters"></a>パラメーター

  - *Source*

  - 省略可能です。有効な **Command** オブジェクト、SQL ステートメント、テーブル名、ストアド プロシージャの呼び出し、URL、または永続的に保存された [Recordset](command-object-ado.md) を格納しているファイル名や [Stream](stream-object-ado.md) オブジェクト名に評価されるバリアント型 ( [Variant](recordset-object-ado.md) ) の値を指定します。

  - *ActiveConnection*

  - 省略可能です。有効な **Connection** オブジェクトのオブジェクト変数名に評価されるバリアント型 ( [Variant](connection-object-ado.md) ) の値、または **ConnectionString** パラメーターを含む文字列型 ( [String](connectionstring-property-ado.md) ) の値を指定します。

  - *カーソル。*

  - 省略可能です。プロバイダーが [Recordset](cursortypeenum.md) を開くときに使用するカーソルの種類を決める **CursorTypeEnum** 値を指定します。既定値は **adOpenForwardOnly** です。

  - *ロック。*

  - 省略可能です。プロバイダーが [Recordset](locktypeenum.md) を開くときに使用するロック (同時作用) の種類を決めるための **LockTypeEnum** 値を指定します。既定値は **adLockReadOnly** です。

  - *Options*

  - 省略可能です。 プロバイダーする必要があります評価方法*元*の引数以外の**コマンド**オブジェクトを表す、または**レコード セット**は、それ以前に保存したファイルから復元するかを示す**Long**値。 1 つまたは複数[CommandTypeEnum](commandtypeenum.md)または[ExecuteOptionEnum](executeoptionenum.md)の値をビットごとの AND 演算子で組み合わせることができます。


> [!NOTE]
> <P>[!メモ] 永続化された <STRONG>Recordset</STRONG> を含む <STRONG>Stream</STRONG> から <STRONG>Recordset</STRONG> を開く場合、 <STRONG>ExecuteOptionEnum</STRONG> 値の <STRONG>adAsyncFetchNonBlocking</STRONG> を使用しても無効です。この場合、フェッチは同期であり、ブロッキングが行われます。</P>



**Open** メソッドを使用する場合は、 **ExecuteOpenEnum** に **adExecuteNoRecords** または **adExecuteStream** を指定しないでください。

## <a name="remarks"></a>解説

ADO の **Recordset** の既定のカーソルは、サーバー側にある読み取り専用の前方スクロール カーソルです。

**Recordset** オブジェクトで **Open** メソッドを使用すると、ベース テーブルからのレコード、クエリの結果、または以前に保存された **Recordset** を表すカーソルを開くことができます。

オプションの*Source*引数を使用して、次のいずれかを使用してデータ ソースを指定する:**コマンド**オブジェクト変数、SQL ステートメント、ストアド プロシージャ、テーブル名、URL やファイルの完全なパス名です。 *ソース*がファイルのパス名の場合は、ことができます、完全なパス ("c:\\dir\\file.rst")、相対パス ("..\\file.rst")、または URL ("https://files/file.rst")。

<<<<<<< ヘッドは、呼び出しが成功したかどうかを判断する簡単な方法がないため、レコードを返さないアクション クエリを実行するのには**Open**メソッドの*Source*引数を使用することをお勧めします。 このようなクエリによって返される**レコード セット**は閉じられます。 SQL INSERT ステートメントなど、レコードを返さないクエリを実行するのには、 **Command**オブジェクトの[Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))メソッドまたは**Connection**オブジェクトの[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\))メソッドを代わりに呼び出します。
=== には、呼び出しが成功したかどうかを判断する簡単な方法がないため、レコードを返さないアクション クエリを実行するのには**Open**メソッドの*Source*引数を使用することをお勧めします。 このようなクエリによって返される**レコード セット**は閉じられます。 SQL INSERT ステートメントなど、レコードを返さないクエリを実行するのには、 **Command**オブジェクトの[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)メソッドまたは**Connection**オブジェクトの[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\))メソッドを代わりに呼び出します。
>>>>>>> master

*暗黙的*では、 [ActiveConnection](activeconnection-property-ado.md)プロパティに対応し、接続を開くには、**レコード セット**オブジェクトを指定します。 この引数に接続の定義を指定すると、ADO により、指定されたパラメーターを使用して新しい接続が開かれます。 クライアント側カーソルで**レコード セット**を開いた後 (**CursorLocation** = **adUseClient**)、別のプロバイダーに更新を送信するには、このプロパティの値を変更することができます。 また、このプロパティを **Nothing** (Microsoft Visual Basic の場合) または NULL に設定すると、その **Recordset** を任意のプロバイダーから切断することができます。 ただし、サーバー側カーソルの **ActiveConnection** を変更すると、エラーが発生します。

**Recordset** オブジェクトのプロパティに直接対応するその他の引数 (*Source*、*CursorType*、および *LockType*) と、プロパティの関係は次のとおりです。

  - **Recordset** オブジェクトを開く前のプロパティは、読み取り/書き込み可能です。

  - **Open** メソッドの実行時に、対応する引数を指定しないと、プロパティの設定値が使用されます。引数を指定した場合は、対応するプロパティの設定値が上書きされて引数の値に更新されます。

  - **Recordset** オブジェクトを開いた後、プロパティは読み取り専用になります。


> [!NOTE]
> <P>[!メモ] <STRONG>Recordset</STRONG> オブジェクトの <STRONG>Source</STRONG> プロパティに有効な <A href="source-property-ado-recordset.md">Command</A> オブジェクトが設定されている場合、その <STRONG>Recordset</STRONG> オブジェクトが開いていなくても、 <STRONG>ActiveConnection</STRONG> プロパティは読み取り専用になります。</P>



*変換元*の引数で、**コマンド**オブジェクトを渡すし *、暗黙的*にも合格すると、エラーが発生します。 **Command** オブジェクトの **ActiveConnection** プロパティは、あらかじめ有効な **Connection** オブジェクトまたは接続文字列に設定しておく必要があります。

*Source*引数に**Command**オブジェクト以外の値を渡すと場合、は、*変換元*の引数の評価を最適化するために*オプション*の引数を使用できます。 *Options*引数が定義されていない場合は、ADO プロバイダーの呼び出しかどうか、引数は、SQL ステートメント、ストアド プロシージャ、URL、またはテーブル名を決定する必要があるためパフォーマンスが低下が発生する可能性があります。 どのような*ソース*の種類がわかっている場合を使用している、関連するコードに直接ジャンプするのには ADO を指示する*オプション*引数を設定します。 *オプション*の引数では、*変換元*の型は一致しない、エラーが発生します。

場合は*変換元*の引数に**Stream**オブジェクトを渡すと、他の引数に情報を渡さないでください。 そのようにすると、エラーが発生します。 **Stream** から **Recordset** を開く場合は、 **ActiveConnection** の情報は保持されません。

*オプション*引数の既定値は**adCmdFile** **レコード セット**に関連付けられている接続が存在しない場合です。 代表的な例では、永続的に保存された **Recordset** オブジェクトの場合がこれに該当します。

データ ソースがレコードを返さない場合、プロバイダーは [BOF](bof-eof-properties-ado.md) プロパティと [EOF](bof-eof-properties-ado.md) プロパティを **True** に設定し、カレント レコードの位置が未定義になります。カーソルの種類によっては、この空の **Recordset** オブジェクトに新しいデータを追加することができます。

開いている **Recordset** に対する操作が完了したら、[Close](close-method-ado.md) メソッドを使用して、関連するシステム リソースをすべて解放します。オブジェクトを閉じてもメモリからは削除されないので、そのオブジェクトのプロパティを変更したり、**Open** メソッドを使用してもう一度開いたりすることができます。オブジェクトをメモリから完全に削除するには、オブジェクト変数に *Nothing* を設定します。

**ActiveConnection**プロパティを設定すると、前に**Open**を呼び出す**レコード セット**の[Fields](fields-collection-ado.md)コレクションにフィールドを追加することによって作成した**レコード セット**のインスタンスを作成するのにはオペランドが無い。

[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定している場合は、非同期に行を取得できる方法が 2 つあります。 **AdAsyncFetch***オプション*を設定することをお勧めします。 もう 1 つの方法として、 [Properties](properties-collection-ado.md) コレクションで "非同期行セット処理" ダイナミック プロパティを使用することもできますが、 **Options** パラメーターを **adAsyncFetch** に設定していない場合は、関連して取得されたイベントが失われる可能性があります。


> [!NOTE]
> <P>MS Remote プロバイダーでバック グラウンドのフェッチは、 <STRONG>Open</STRONG>メソッドの<EM>Options</EM>パラメーターでのみサポートされます。</P>


<<<<<<< ヘッド


> [!NOTE]
> <P>[!メモ] http 体系を使用している URL は、<A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A> を自動的に呼び出します。詳細については、「 <A href="absolute-and-relative-urls.md">絶対 URL と相対 URL</A>」を参照してください。</P>
=======
> [!NOTE]
> [!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。
>>>>>>> master


