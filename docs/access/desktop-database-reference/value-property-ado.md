---
<<<<<<< ヘッド タイトル: 値のプロパティ (ADO) TOCTitle: 値のプロパティ (ADO) === タイトル: Value プロパティ (ADO) TOCTitle: Value プロパティ (ADO)
>>>>>>> マスターの ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15) ms:contentKeyID: 48548958 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="value-property-ado"></a>Value プロパティ (ADO)
=======
# <a name="value-property-ado"></a>Value プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Field](field-object-ado.md) オブジェクト、 [Parameter](parameter-object-ado.md) オブジェクト、または [Property](property-object-ado.md) オブジェクトに割り当てられた値を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

オブジェクトの値を示すバリアント型 ( **Variant** ) の値を設定または取得します。既定値は [Type](type-property-ado.md) プロパティによって異なります。

## <a name="remarks"></a>解説

**Field** オブジェクトのデータを設定または取得するとき、 **Parameter** オブジェクトでパラメーター値を設定または取得するとき、または **Property** オブジェクトでプロパティを設定または取得するときには、 **Value** プロパティを使用します。 **Value** プロパティは、さまざまな要因によって、値の取得と設定が可能な場合と、値の取得のみが可能な場合があります。詳細については、各オブジェクトのトピックを参照してください。

ADO では、 **Value** プロパティを使用してロング バイナリ データを設定および取得できます。


> [!NOTE]
> <P>[!メモ] <STRONG>Parameter</STRONG> オブジェクトの場合、ADO はプロバイダーから一度だけ <STRONG>Value</STRONG> プロパティを取得します。コマンドに含まれる <STRONG>Parameter</STRONG> の <STRONG>Value</STRONG> プロパティが空で、このコマンドから <A href="recordset-object-ado.md">Recordset</A> を作成する場合は、 <STRONG>Value</STRONG> プロパティを取得する前に、 <STRONG>Recordset</STRONG> を閉じる必要があります。このようにしないと、プロバイダーによっては、 <STRONG>Value</STRONG> プロパティが空になり、正しい値が格納されない場合があります。</P>



**Record** オブジェクトの [Fields](fields-collection-ado.md) コレクションに新しい [Field](record-object-ado.md) オブジェクトを追加した場合は、 **Value** プロパティを最初に設定してから、他の **Field** プロパティを指定する必要があります。まず、 **Value** プロパティに特定の値を割り当て、 [Fields](update-method-ado.md) コレクションで **Update** を呼び出します。その後は、 [Type](type-property-ado.md) や [Attributes](attributes-property-ado.md) などの他のプロパティにアクセスできます。

