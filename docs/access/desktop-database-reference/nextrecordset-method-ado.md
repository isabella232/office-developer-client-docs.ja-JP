---
title: NextRecordset メソッド (ADO)
TOCTitle: NextRecordset method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b572f4ebe55da1add781ecd86df97937cfeae126
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717161"
---
# <a name="nextrecordset-method-ado"></a>NextRecordset メソッド (ADO)

**適用されます**Access 2013、Office 2013。
 
現在の [Recordset](recordset-object-ado.md) オブジェクトをクリアし、一連のコマンド操作を実行して次の **Recordset** を返します。

## <a name="syntax"></a>構文

*Recordset2*の設定 = *recordset1*。NextRecordset (*RecordsAffected* )

## <a name="return-value"></a>戻り値

**Recordset** オブジェクトを返します。構文モデルの *recordset1* と *recordset2* には、同じ **Recordset** オブジェクト、または別のオブジェクトを指定できます。別の **Recordset** オブジェクトを使用する場合、**NextRecordset** の呼び出しの後に元の **Recordset** (*recordset1*) の **ActiveConnection** プロパティを再設定すると、エラーが発生します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*RecordsAffected* |省略可能です。長整数型 ( **Long** ) の変数を指定します。プロバイダーは、操作の影響を受けたレコード数をここに返します。|

> [!NOTE]
> [!メモ] このパラメーターは、操作の影響を受けたレコード数のみを返します。 **Recordset** を作成するために使用された Select ステートメントからのレコード数を返すことはありません。

## <a name="remarks"></a>解説

**NextRecordset** メソッドでは、複合コマンド ステートメントの次のコマンドの結果、または複数の結果を返すストアド プロシージャの結果を返します。 複合コマンド ステートメントに基づく**レコード セット**オブジェクトを開くかどうか (たとえば、"を選択して\*table1; から\* Table2 から」) [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)メソッドを使用して、[コマンド](command-object-ado.md)または**レコード セット**で[Open](open-method-ado-recordset.md)メソッドで、ADO は最初のコマンドのみを実行し、*レコード セット*に結果を返します。 ステートメントの次のコマンドの結果にアクセスするには、 **NextRecordset** メソッドを呼び出します。

追加の結果は、複合ステートメントを含む**レコード セット**が切断またはプロセスの境界を越えてマーシャ リングされない限り、 **NextRecordset**メソッドは引き続き**レコード セット**オブジェクトを返します。 行を返すコマンドが正常に実行されるレコードが返されない場合は、返された**Recordset**オブジェクトが開いている空れます。 このケースをテストするには、 [bof プロパティ](bof-eof-properties-ado.md)と[EOF](bof-eof-properties-ado.md)プロパティが両方の**場合は True**であることの確認します。 行を返さないコマンドが正常に実行された場合、返される**レコード セット**オブジェクトは閉じて**レコード セット**で、 [State](state-property-ado.md)プロパティをテストすることによって確認することができます。 以上結果が存在する場合、*レコード セット*を*Nothing*に設定されます。

切断された **Recordset** オブジェクトでは、 **ActiveConnection** が [Nothing](activeconnection-property-ado.md) (Microsoft Visual Basic) または NULL (その他の言語) に設定されているため、 **NextRecordset** メソッドは使用できません。

即時更新モードで編集を行っているときに **NextRecordset** メソッドを呼び出すと、エラーが発生します。 [Update](update-method-ado.md) メソッドまたは [CancelUpdate](cancelupdate-method-ado.md) メソッドを先に呼び出す必要があります。

複合ステートメントの複数のコマンドにパラメーターを渡すには、[Parameters](parameters-collection-ado.md) コレクションを使用するか、または元の **Open** メソッドまたは **Execute** メソッドの呼び出しで配列を渡します。この場合、コレクションまたは配列のパラメーターの並び順は、一連のコマンドの並び順と同じである必要があります。出力パラメーターの値を読み込むには、すべての結果の読み込みが終了している必要があります。

複合ステートメント内の各コマンドをいつ実行するかは、OLE DB プロバイダーが決定します。たとえば、[Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) は、複合ステートメントを受け取ったときにすべてのコマンドをバッチで実行します。結果の **Recordsets** は、 **NextRecordset** を呼び出したときに返されます。

ただし、それ以外のプロバイダーでは、ステートメント内の次のコマンドが NextRecordset の呼び出しの後にしか実行されないこともあります。そのようなプロバイダーの場合、ステートメントのすべてのコマンドを実行する前に **Recordset** オブジェクトを明示的に閉じると、残りのコマンドは実行されません。

