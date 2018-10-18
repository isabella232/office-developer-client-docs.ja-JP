---
<<<<<<< ヘッド タイトル: TOCTitle のサイズ プロパティ (ADO): サイズ プロパティ (ADO) === タイトル: Size プロパティ (ADO) TOCTitle: Size プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15) ms:contentKeyID: 48543753 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="size-property-ado"></a>Size プロパティ (ADO)
=======
# <a name="size-property-ado"></a>Size プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Parameter](parameter-object-ado.md) オブジェクトの最大サイズをバイト数または文字数で示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

**Parameter** オブジェクトの最大サイズをバイト数または文字数で示す長整数型 ( **Long** ) の値を設定または取得します。

## <a name="remarks"></a>解説

**Parameter** オブジェクトの [Value](value-property-ado.md) プロパティで設定または取得できる値の最大サイズを調べるには、 **Size** プロパティを使用します。

**Parameter** オブジェクトとして可変長データ型 (たとえば、**adVarChar** などのすべての文字列型 (**String**)) を指定した場合、[Parameters](parameters-collection-ado.md) コレクションにそのオブジェクトを追加する前に、オブジェクトの **Size** プロパティを設定する必要があり、この設定を行わないとエラーが発生します。

**Parameter** オブジェクトが **Command** オブジェクトの [Parameters](command-object-ado.md) コレクションに既に追加されている場合に、そのデータ型を可変長データ型に変更した場合は、 **Command** オブジェクトを実行する前に **Parameter** オブジェクトの **Size** プロパティを設定する必要があり、この設定を行わないとエラーが発生します。

[Refresh](refresh-method-ado.md) メソッドを使用してプロバイダーからパラメーター情報を取得したときに、可変長データ型の **Parameter** オブジェクトが返された場合、可能な最大サイズに基づいてパラメーターにメモリが割り当てられますが、これが原因で実行時にエラーが発生することがあります。エラーを回避するには、コマンドを実行する前に、明示的にこれらのパラメーターの **Size** プロパティを設定します。

**Size** プロパティは、値の取得および設定が可能です。

