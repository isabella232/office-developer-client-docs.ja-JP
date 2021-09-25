---
title: NextRecordset メソッド (ADO)
TOCTitle: NextRecordset method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 282d6ff3646800ebc107a1e2a7c96f80926e463f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589380"
---
# <a name="nextrecordset-method-ado"></a>NextRecordset メソッド (ADO)

**適用先**: Access 2013、Office 2013
 
現在の [Recordset](recordset-object-ado.md) オブジェクトをクリアし、一連のコマンド操作を実行して次の **Recordset** を返します。

## <a name="syntax"></a>構文

Recordset2   =  *recordset1 を設定します*。NextRecordset(*RecordsAffected* )

## <a name="return-value"></a>戻り値

**Recordset** オブジェクトを返します。構文モデルの *recordset1* と *recordset2* には、同じ **Recordset** オブジェクト、または別のオブジェクトを指定できます。別の **Recordset** オブジェクトを使用する場合、**NextRecordset** の呼び出しの後に元の **Recordset** (*recordset1*) の **ActiveConnection** プロパティを再設定すると、エラーが発生します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*RecordsAffected* |省略可能です。長整数型 ( **Long** ) の変数を指定します。プロバイダーは、操作の影響を受けたレコード数をここに返します。|

> [!NOTE]
> このパラメーターは、操作の影響を受けたレコード数のみを返します。**Recordset** を作成するために使用された Select ステートメントからのレコード数を返すことはありません。

## <a name="remarks"></a>注釈

**NextRecordset** メソッドでは、複合コマンド ステートメントの次のコマンドの結果、または複数の結果を返すストアド プロシージャの結果を返します。 複合コマンド ステートメントに **基づいて Recordset** オブジェクトを開く場合 (たとえば、「SELECT \* FROM table1;SELECT FROM table2") を使用して、Command の Execute メソッドまたは Recordset の Open メソッドを使用すると、ADO は最初のコマンドのみを実行し、結果をレコードセット \* に返 *します*。 [](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) [](command-object-ado.md) [](open-method-ado-recordset.md)  ステートメントの次のコマンドの結果にアクセスするには、 **NextRecordset** メソッドを呼び出します。

結果が追加され、複合ステートメントを含む **Recordset** がプロセス境界を越えて切断またはマーシャリングされない限り **、NextRecordset** メソッドは **Recordset** オブジェクトを返し続ける。 行を返すコマンドが正常に実行され、レコードが返されていない場合、返される **Recordset** オブジェクトは開いているが空になります。 このケースをテストするには [、BOF](bof-eof-properties-ado.md) プロパティと [EOF](bof-eof-properties-ado.md) プロパティの両方が True である必要 **があります**。 行を返す以外のコマンドが正常に実行されると、返される **Recordset** オブジェクトが閉じられます。これは **、Recordset** の [State](state-property-ado.md)プロパティをテストして確認できます。 結果がこれ以上ない場合、 *レコードセットは Nothing* に *設定されます*。

切断された **Recordset** オブジェクトでは、 **ActiveConnection** が [Nothing](activeconnection-property-ado.md) (Microsoft Visual Basic) または NULL (その他の言語) に設定されているため、 **NextRecordset** メソッドは使用できません。

即時更新モードで編集を行っているときに **NextRecordset** メソッドを呼び出すと、エラーが発生します。 [Update](update-method-ado.md) メソッドまたは [CancelUpdate](cancelupdate-method-ado.md) メソッドを先に呼び出す必要があります。

複合ステートメントの複数のコマンドにパラメーターを渡すには、[Parameters](parameters-collection-ado.md) コレクションを使用するか、または元の **Open** メソッドまたは **Execute** メソッドの呼び出しで配列を渡します。この場合、コレクションまたは配列のパラメーターの並び順は、一連のコマンドの並び順と同じである必要があります。出力パラメーターの値を読み込むには、すべての結果の読み込みが終了している必要があります。

複合ステートメント内の各コマンドをいつ実行するかは、OLE DB プロバイダーが決定します。たとえば、[Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) は、複合ステートメントを受け取ったときにすべてのコマンドをバッチで実行します。結果の **Recordsets** は、 **NextRecordset** を呼び出したときに返されます。

ただし、それ以外のプロバイダーでは、ステートメント内の次のコマンドが NextRecordset の呼び出しの後にしか実行されないこともあります。そのようなプロバイダーの場合、ステートメントのすべてのコマンドを実行する前に **Recordset** オブジェクトを明示的に閉じると、残りのコマンドは実行されません。

