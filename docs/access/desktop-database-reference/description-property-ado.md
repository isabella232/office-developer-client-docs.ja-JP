---
<<<<<<< ヘッド タイトル: 説明プロパティ (ADO) TOCTitle: 説明プロパティ (ADO) === タイトル: Description プロパティ (ADO) TOCTitle: Description プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: 48544064 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="description-property-ado"></a>Description プロパティ (ADO)
=======
# <a name="description-property-ado"></a>Description プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Error](error-object-ado.md) オブジェクトを記述します。

<<<<<<< ヘッド
## <a name="return-value"></a>戻り値
=======
## <a name="return-value"></a>戻り値
>>>>>>> master

エラーの内容を表す文字列型 ( **String** ) の値を返します。

## <a name="remarks"></a>解説

**Description** プロパティは、エラーの簡単な説明を取得するために使います。プログラムで対処できないエラー、または処理することが望ましくないエラーは、このプロパティの内容を表示してユーザーに警告します。文字列は、ADO またはプロバイダーから渡されます。

プロバイダーは、特定のエラー テキストを ADO に渡します。ADO は、受け取ったプロバイダー エラーまたは警告ごとに [Error](error-object-ado.md) オブジェクトを **Errors** コレクションに追加します。プロバイダーが渡すエラーをトレースするには、 **Errors** コレクションを列挙します。

