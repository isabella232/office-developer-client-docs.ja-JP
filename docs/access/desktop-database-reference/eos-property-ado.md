---
タイトル: EOS プロパティ (ADO のデスクトップのデータベース参照のアクセス)) <<<<<<< ヘッド TOCTitle: EOS プロパティ (ADO) === TOCTitle: EOS プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15) ms:contentKeyID: 48546474 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="eos-property-ado"></a>EOS プロパティ (ADO)
=======
# <a name="eos-property-ado"></a>EOS プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

現在の位置がストリームの末尾にあるかどうかを示します。

<<<<<<< ヘッド
## <a name="return-values"></a>戻り値
=======
## <a name="return-values"></a>戻り値
>>>>>>> master

現在の位置がストリームの末尾かどうかを示すブール型 ( **Boolean** ) の値を返します。ストリームにバイトがなくなると **EOS** は **True** を返し、現在の位置の後にもバイトがあると **False** を返します。

ストリームの末尾の位置を設定するには、[SetEOS](seteos-method-ado.md) メソッドを使用します。現在の位置を確認するには、 [Position](position-property-ado.md) プロパティを使用します。

