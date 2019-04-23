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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288618"
---
# <a name="nextrecordset-method-ado"></a>NextRecordset メソッド (ADO)

**適用先:** Access 2013、Office 2013
 
現在の [Recordset](recordset-object-ado.md) オブジェクトをクリアし、一連のコマンド操作を実行して次の **Recordset** を返します。

## <a name="syntax"></a>構文

*recordset2* = *recordset1*を設定します。NextRecordset (*RecordsAffected* )

## <a name="return-value"></a>戻り値

**Recordset** オブジェクトを返します。構文モデルの *recordset1* と *recordset2* には、同じ **Recordset** オブジェクト、または別のオブジェクトを指定できます。別の **Recordset** オブジェクトを使用する場合、**NextRecordset** の呼び出しの後に元の **Recordset** (*recordset1*) の **ActiveConnection** プロパティを再設定すると、エラーが発生します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*RecordsAffected* |省略可能です。長整数型 ( **Long** ) の変数を指定します。プロバイダーは、操作の影響を受けたレコード数をここに返します。|

> [!NOTE]
> このパラメーターは、操作の影響を受けたレコード数のみを返します。**Recordset** を作成するために使用された Select ステートメントからのレコード数を返すことはありません。

## <a name="remarks"></a>注釈

**NextRecordset** メソッドでは、複合コマンド ステートメントの次のコマンドの結果、または複数の結果を返すストアド プロシージャの結果を返します。 複合コマンドステートメントに基づいて**Recordset**オブジェクトを開いた場合 (たとえば、"table1 から\*選択してください。[ \* table2 からの選択][コマンド](command-object-ado.md)に対して[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)メソッドまたは**recordset**の[Open](open-method-ado-recordset.md)メソッドを使用すると、最初のコマンドのみが実行され、結果が*recordset*に返されます。 ステートメントの次のコマンドの結果にアクセスするには、 **NextRecordset** メソッドを呼び出します。

その他の結果があり、複合ステートメントを含む**Recordset**がプロセス境界を越えて切断またはマーシャリングされていない限り、 **NextRecordset**メソッドは引き続き**recordset**オブジェクトを返します。 行を返すコマンドが正常に実行されてもレコードが返されない場合は、返された**Recordset**オブジェクトが空になります。 この場合は、 [BOF](bof-eof-properties-ado.md)プロパティと[EOF](bof-eof-properties-ado.md)プロパティが両方とも**True**であることを確認してテストします。 行を返さないコマンドが正常に実行された場合は、返された**recordset**オブジェクトが閉じられ、 **recordset**の[State](state-property-ado.md)プロパティをテストすることによって確認できます。 結果がなければ、 *recordset*は*Nothing*に設定されます。

切断された **Recordset** オブジェクトでは、 **ActiveConnection** が [Nothing](activeconnection-property-ado.md) (Microsoft Visual Basic) または NULL (その他の言語) に設定されているため、 **NextRecordset** メソッドは使用できません。

即時更新モードで編集を行っているときに **NextRecordset** メソッドを呼び出すと、エラーが発生します。 [Update](update-method-ado.md) メソッドまたは [CancelUpdate](cancelupdate-method-ado.md) メソッドを先に呼び出す必要があります。

複合ステートメントの複数のコマンドにパラメーターを渡すには、[Parameters](parameters-collection-ado.md) コレクションを使用するか、または元の **Open** メソッドまたは **Execute** メソッドの呼び出しで配列を渡します。この場合、コレクションまたは配列のパラメーターの並び順は、一連のコマンドの並び順と同じである必要があります。出力パラメーターの値を読み込むには、すべての結果の読み込みが終了している必要があります。

複合ステートメント内の各コマンドをいつ実行するかは、OLE DB プロバイダーが決定します。たとえば、[Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) は、複合ステートメントを受け取ったときにすべてのコマンドをバッチで実行します。結果の **Recordsets** は、 **NextRecordset** を呼び出したときに返されます。

ただし、それ以外のプロバイダーでは、ステートメント内の次のコマンドが NextRecordset の呼び出しの後にしか実行されないこともあります。そのようなプロバイダーの場合、ステートメントのすべてのコマンドを実行する前に **Recordset** オブジェクトを明示的に閉じると、残りのコマンドは実行されません。

