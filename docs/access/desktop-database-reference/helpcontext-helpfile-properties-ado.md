---
<<<<<<< ヘッド タイトル: HelpContext、HelpFile プロパティ (ADO) TOCTitle: HelpContext、HelpFile プロパティ (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 09/18/2015 mtps_version: v=office.15
---

# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext プロパティと HelpFile プロパティ (ADO)

=== タイトル: HelpContext、HelpFile プロパティ (ADO) TOCTitle: HelpContext、HelpFile プロパティ (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 2018/10/17 mtps_version: v=office.15
---

# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext、HelpFile プロパティ (ADO)
>>>>>>> master

**適用されます**Access 2013 |。Office 2013

[Error](error-object-ado.md) オブジェクトに関連するヘルプ ファイルおよびヘルプ トピックを示します。

<<<<<<< ヘッド
## <a name="return-values"></a>戻り値

  - **HelpContextID**: ヘルプ ファイルのトピックのコンテキスト ID を長整数型 ( **Long** ) の値で返します。

  - **HelpFile**: ヘルプ ファイルへの完全なパスに評価される文字列型 ( **String** ) の値を返します。
=======
## <a name="return-values"></a>戻り値

- **HelpContextID**: ヘルプ ファイルのトピックのコンテキスト ID を長整数型 ( **Long** ) の値で返します。

- **HelpFile**: ヘルプ ファイルへの完全なパスに評価される文字列型 ( **String** ) の値を返します。
>>>>>>> master

## <a name="remarks"></a>解説

**HelpFile** プロパティでヘルプ ファイルが指定されている場合、 **HelpContext** プロパティを使って特定のヘルプ トピックを自動的に表示できます。該当するヘルプ トピックがない場合、 **HelpContext** プロパティは 0 を返し、 **HelpFile** プロパティは長さ 0 の文字列 ("") を返します。

