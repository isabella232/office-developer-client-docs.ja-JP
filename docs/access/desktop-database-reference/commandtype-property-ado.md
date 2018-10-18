---
<<<<<<< ヘッド タイトル: CommandType プロパティ (ADO) TOCTitle: CommandType プロパティ (ADO) === タイトル: CommandType プロパティ (ADO) TOCTitle: CommandType プロパティ (ADO)
>>>>>>> マスターの ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15) ms:contentKeyID: 48547663 ms.date: 2015/09/18 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231125 f1_categories。
- Office.Version=v15
---

<<<<<<< ヘッド
# <a name="commandtype-property-ado"></a>CommandType プロパティ (ADO)
=======
# <a name="commandtype-property-ado"></a>CommandType プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Command](command-object-ado.md) オブジェクトの型を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

1 つまたは複数の [CommandTypeEnum](commandtypeenum.md) 値を設定または取得します。


> [!NOTE]
> <P>[!メモ] <STRONG>CommandType</STRONG> では、 <STRONG>adCmdFile</STRONG> または <STRONG>adCmdTableDirect</STRONG> の <STRONG>CommandTypeEnum</STRONG> 値を使用しないでください。これらの値は、 <A href="open-method-ado-recordset.md">Recordset</A> の <A href="requery-method-ado.md">Open</A> メソッドと <A href="recordset-object-ado.md">Requery</A> メソッドのオプションとしてのみ使用することができます。</P>



## <a name="remarks"></a>解説

**CommandType** プロパティは、 [CommandText](commandtext-property-ado.md) プロパティの評価を最適化するために使用します。

<<<<<<< ヘッド場合は、 **CommandType**プロパティの値が**adCmdUnknown** (既定値) に等しい、ADO は、プロバイダーにするかどうかの呼び出しを行う必要があるためパフォーマンスが低下が発生する可能性があります**CommandText**プロパティでは、SQL ステートメント、ストアド プロシージャ、またはテーブル名です。 **CommandType**プロパティを設定を使用するコマンドの種類がわかっている場合は、関連するコードに直接移動するのには ADO に指示します。 **CommandType**プロパティが**CommandText**プロパティのコマンドの種類に一致しない場合は、 [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))メソッドを呼び出すときにエラーが発生しました。
=== ADO は、 **CommandText**プロパティが SQL ステートメントでは、かどうかを判断するのには、プロバイダーへの呼び出しを行う必要があるためパフォーマンスが低下が発生する可能性があります場合は、 **CommandType**プロパティの値が**adCmdUnknown** (既定値) をストアド プロシージャ、またはテーブル名です。 **CommandType**プロパティを設定を使用するコマンドの種類がわかっている場合は、関連するコードに直接移動するのには ADO に指示します。 **CommandType**プロパティが**CommandText**プロパティのコマンドの種類に一致しない場合は、 [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)メソッドを呼び出すときにエラーが発生しました。
>>>>>>> master

