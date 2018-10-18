---
<<<<<<< ヘッド タイトル: 以下のプロパティ (ADO) TOCTitle: 以下のプロパティ (ADO) === タイトル: 以下のプロパティ (ADO) TOCTitle: 以下のプロパティ (ADO)
>>>>>>> マスターの ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15) ms:contentKeyID: 48546685 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="nativeerror-property-ado"></a>NativeError プロパティ (ADO)
=======
# <a name="nativeerror-property-ado"></a>以下のプロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

指定された [Error](error-object-ado.md) オブジェクトでプロバイダー固有のエラー コードを示します。

<<<<<<< ヘッド
## <a name="return-value"></a>戻り値
=======
## <a name="return-value"></a>戻り値
>>>>>>> master

エラー コードを示す長整数型 ( **Long** ) の値を返します。

## <a name="remarks"></a>解説

**NativeError** プロパティは、特定の **Error** オブジェクトの、データベース固有のエラー情報を取得するために使用します。たとえば、Microsoft ODBC Provider for OLE DB と Microsoft SQL Server データベースを使う場合、SQL Server から送信されたネイティブ エラー コードは、ODBC と ODBC Provider を経由して ADO の **NativeError** プロパティに渡されます。

