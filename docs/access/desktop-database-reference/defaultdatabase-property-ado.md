---
<<<<<<< ヘッド タイトル: DefaultDatabase プロパティ (ADO) TOCTitle: DefaultDatabase プロパティ (ADO) === タイトル: DefaultDatabase プロパティ (ADO) TOCTitle: DefaultDatabase プロパティ (ADO)
>>>>>>> マスターの ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15) ms:contentKeyID: 48546784 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="defaultdatabase-property-ado"></a>DefaultDatabase プロパティ (ADO)
=======
# <a name="defaultdatabase-property-ado"></a>DefaultDatabase プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Connection](connection-object-ado.md) オブジェクトの既定のデータベースを示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

プロバイダーで使用可能なデータベースの名前に評価される文字列型 ( **String** ) の値を設定または取得します。

## <a name="remarks"></a>解説

**DefaultDatabase** プロパティは、特定の **Connection** オブジェクトの既定のデータベースの名前を設定または取得するために使います。

既定のデータベースがある場合、そのデータベースのオブジェクトにアクセスする SQL 文の構文が不適切な場合があります。 **DefaultDatabase** プロパティで指定されたデータベース以外のデータベースのオブジェクトにアクセスするには、オブジェクト名を目的のデータベース名で修飾する必要があります。接続時に、プロバイダーは **DefaultDatabase** プロパティに既定のデータベース情報を書き込みます。プロバイダーの中には 1 つの接続に 1 つのデータベースしか許可しないものがあり、その場合は **DefaultDatabase** プロパティを変更できません。

データ ソースとプロバイダーによっては、この機能をサポートせず、エラーまたは空の文字列を返す場合があります。

**リモート データ サービスの使用法**このプロパティはクライアント側の**接続**オブジェクトで使用できます。

