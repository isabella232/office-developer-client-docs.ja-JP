---
<<<<<<< ヘッド タイトル: LineSeparator プロパティ (ADO) TOCTitle: LineSeparator プロパティ (ADO) === タイトル: LineSeparator プロパティ (ADO) TOCTitle: LineSeparator プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID: 48546676 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="lineseparator-property-ado"></a>LineSeparator プロパティ (ADO)
=======
# <a name="lineseparator-property-ado"></a>LineSeparator プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

テキスト [Stream](stream-object-ado.md) オブジェクトの行区切り文字として使用するバイナリ文字を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

[Stream](lineseparatorsenum.md) で使う行区切り文字を示す **LineSeparatorsEnum** 値を設定または取得します。既定値は **adCRLF** です。

## <a name="remarks"></a>解説

**LineSeparator** は、テキスト **Stream** の内容を読むときに行を解釈するために使います。行は、 [SkipLine](skipline-method-ado.md) メソッドで読み飛ばすこともできます。

**LineSeparator** は、テキスト **Stream** オブジェクト ([Type](type-property-ado-stream.md) が **adTypeText**) だけに使用します。**Type** が **adTypeBinary** の場合、このプロパティは無視されます。

