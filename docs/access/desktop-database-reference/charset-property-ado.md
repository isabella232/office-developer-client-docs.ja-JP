---
<<<<<<< ヘッド タイトル: Charset プロパティ (ADO) TOCTitle: Charset プロパティ (ADO) === タイトル: Charset プロパティ (ADO) TOCTitle: Charset プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15) ms:contentKeyID: 48544551 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="charset-property-ado"></a>Charset プロパティ (ADO)
=======
# <a name="charset-property-ado"></a>Charset プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

テキスト [Stream](stream-object-ado.md) の内容を変換して Stream オブジェクト内部バッファーに格納するための文字セットを示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

**Stream** の内容の変換に使用される文字セットを指定する文字列型 ( **String** ) の値を設定または取得します。 既定値は "Unicode" です。 指定可能な値は、インターフェイスを介してインターネット文字セット文字列として渡すことのできる通常の文字列 ("iso-8859-1"、"Windows-1252" など) です。 システムで認識されている文字セットの文字列のリスト、HKEY のサブキーを参照してください\_クラス\_ルート\\MIME\\データベース\\Windows レジストリ内の文字セットです。

## <a name="remarks"></a>解説

テキスト **Stream** オブジェクトでは、 **Charset** プロパティで指定された文字セットでテキスト データが格納されます。既定値は Unicode です。 **Charset** プロパティは、 **Stream** に送るデータの変換、または **Stream** から受け取るデータの変換に使用されます。たとえば、 **Stream** に ISO-8859-1 データが格納されており、そのデータが BSTR にコピーされる場合、 **Stream** オブジェクトはデータを Unicode に変換します。逆の変換も同じように行われます。

開いている **Stream** の場合、 [Charset](position-property-ado.md) を設定するには、現在の **Position** が **Stream** の先頭 (0) になっている必要があります。

**Charset** は、テキスト **Stream** オブジェクト ([Type](type-property-ado-stream.md) が **adTypeText**) でのみ使用されます。**Type** が **adTypeBinary** の場合、このプロパティは無視されます。

