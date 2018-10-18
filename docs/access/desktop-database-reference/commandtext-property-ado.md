---
<<<<<<< ヘッド タイトル: CommandText プロパティ (ADO) TOCTitle: CommandText プロパティ (ADO) === タイトル: CommandText プロパティ (ADO) TOCTitle: CommandText プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15) ms:contentKeyID: 48543234 ms.date: 2015/09/18 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231123 f1_categories。
- Office.Version=v15
---

<<<<<<< ヘッド
# <a name="commandtext-property-ado"></a>CommandText プロパティ (ADO)
=======
# <a name="commandtext-property-ado"></a>CommandText プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

プロバイダーに対して発行するコマンド文字列を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

SQL ステートメント、テーブル名、相対 URL、またはストアド プロシージャの呼び出しなど、プロバイダーのコマンドを含む文字列型 ( **String** ) の値を設定または取得します。既定値は "" (長さ 0 の文字列) です。

## <a name="remarks"></a>解説

**Command** オブジェクトで表されるコマンド テキストを設定または取得するには、 [CommandText](command-object-ado.md) プロパティを使用します。通常は SQL ステートメントを使いますが、ストアド プロシージャの呼び出しなど、プロバイダーが認識する、他の種類のコマンド ステートメントでもかまいません。SQL ステートメントは、特定の文法またはプロバイダーのクエリ プロセッサがサポートするバージョンである必要があります。

<<<<<<< **Command**オブジェクトの[Prepared](prepared-property-ado.md)プロパティが**True**に設定されている場合はヘッド、 **CommandText**プロパティを設定するときに、接続を開く**コマンド**オブジェクトがバインドされていると、ADO クエリ (の準備プロバイダーによって格納されているクエリのコンパイルされた形式では、) [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))や**Open**メソッドを呼び出すとします。
=== ADO クエリを準備場合は、 **Command**オブジェクトの[Prepared](prepared-property-ado.md)プロパティが**True**に設定し、**コマンド**オブジェクトの**CommandText**プロパティを設定すると、開かれた接続をバインド、(コンパイル済みのフォームは、プロバイダーによって格納されているクエリ) [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)や**Open**メソッドを呼び出すとします。
>>>>>>> master

[CommandType](commandtype-property-ado.md) プロパティの設定値によっては、 **CommandText** プロパティが変更される場合があります。 **CommandText** プロパティはいつでも読み出すことができ、ADO がコマンド実行中に使う実際のコマンド テキストの参照も可能です。

ファイルやディレクトリなどのリソースを指定する相対 URL を設定したり取得したりするには、 **CommandText** プロパティを使います。リソースは、絶対 URL で明示的に指定された位置や、開かれた [Connection](connection-object-ado.md) オブジェクトで暗黙的に指定された位置に対して相対的です。


> [!NOTE]
<<<<<<< ヘッド
> <P>[!メモ] http 体系を使用している URL は、<A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A> を自動的に呼び出します。詳細については、「 <A href="absolute-and-relative-urls.md">絶対 URL と相対 URL</A>」を参照してください。</P>
=======
> [!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。
>>>>>>> master


