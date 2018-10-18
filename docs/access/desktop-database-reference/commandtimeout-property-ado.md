---
<<<<<<< ヘッド タイトル: CommandTimeout プロパティ (ADO) TOCTitle: CommandTimeout プロパティ (ADO) === タイトル: CommandTimeout プロパティ (ADO) TOCTitle: CommandTimeout プロパティ (ADO)
>>>>>>> マスターの ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15) ms:contentKeyID: 48546714 ms.date: 2015/09/18 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231124 f1_categories。
- Office.Version=v15
---

<<<<<<< ヘッド
# <a name="commandtimeout-property-ado"></a>CommandTimeout プロパティ (ADO)
=======
# <a name="commandtimeout-property-ado"></a>CommandTimeout プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

実行しようとしたコマンドを中止して、エラーを生成するまでの待機時間を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

コマンドが実行されるまでの待機時間を秒単位で示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 30 です。

## <a name="remarks"></a>解説

<<<<<<< ヘッドは、ネットワーク トラフィックやサーバーの使用からの遅延のため、 [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))メソッドを呼び出すのキャンセルを許可する[接続](connection-object-ado.md)オブジェクトまたは[Command](command-object-ado.md)オブジェクトの**CommandTimeout**プロパティを使用します。 コマンドの実行が完了する前に **CommandTimeout** プロパティで設定された時間が経過すると、エラーが発生してコマンドが取り消されます。 プロパティを 0 に設定すると、コマンド実行が完了するまで無限に待機します。 コードを書き込むプロバイダーとデータ ソースが **CommandTimeout** 機能をサポートしていることを確認してください。
=== ネットワーク トラフィックやサーバーの使用からの遅延のため、 [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)メソッドを呼び出すのキャンセルを許可するのに[接続](connection-object-ado.md)オブジェクトまたは[Command](command-object-ado.md)オブジェクトの**CommandTimeout**プロパティを使用します。 コマンドの実行が完了する前に **CommandTimeout** プロパティで設定された時間が経過すると、エラーが発生してコマンドが取り消されます。 プロパティを 0 に設定すると、コマンド実行が完了するまで無限に待機します。 コードを書き込むプロバイダーとデータ ソースが **CommandTimeout** 機能をサポートしていることを確認してください。
>>>>>>> master

**Connection** オブジェクトの **CommandTimeout** 設定は、同じ **Connection** 上の **Command** オブジェクトの **CommandTimeout** 設定に影響しません。つまり、 **Command** オブジェクトの **CommandTimeout** プロパティは、 **Connection** オブジェクトの **CommandTimeout** の値を継承しません。

**Connection** オブジェクトでは、 **CommandTimeout** プロパティは **Connection** が開かれた後も、読み取り/書き込みが可能です。

