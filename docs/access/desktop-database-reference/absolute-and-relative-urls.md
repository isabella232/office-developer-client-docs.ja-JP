---
title: 絶対 URL と相対 URL
TOCTitle: Absolute and relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6195467d6ca41c5f1f26084975f2f00fc8dd9b83
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586440"
---
# <a name="absolute-and-relative-urls"></a>絶対 URL と相対 URL

**適用先**: Access 2013、Office 2013    

URL で、ファイル、ディレクトリ、HTML ページ、画像、プログラムなどの保存先、つまりローカルまたはネットワーク コンピューターでの場所を指定します。 ここでは、"絶対 URL" は次の形式とします。

*scheme://server/path/resource*

各項目の意味は次のとおりです。

|名前 |説明|
|:----|:----------|
|*scheme*|*resource* がどのようにアクセスされるかを指定します。|
|*server*|*resource* が存在するコンピューターの名前を指定します。|
|*path*|ターゲットに導くディレクトリの順序を指定します。*resource* が省略されると、ターゲットは *path* 内の最後のディレクトリと見なされます。|
|*resource*|含まれている場合 *、リソース* はターゲットであり、通常はファイルの名前です。 1 つのバイナリ ストリームのバイトを含む単純なファイル、または1 つ以上の記憶域とバイナリ ストリームのバイトを含む構造化ドキュメントを指定できます。|

"絶対 URL" には、リソースを検索するために必要なすべての情報が含まれています。

相対 *URL は* 、開始点として絶対 URL を使用してリソースを検索します。 In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs. 相対 URL は、通常、パス、およびオプションでリソースで構成されますが、スキーム *やサーバーは* 含 *されません*。

## <a name="url-scheme-registration"></a>URL スキームの登録

プロバイダーが URL をサポートしている場合、1 つまたは複数の URL スキーマに登録します。 つまり、このスキーマを使用する URL は、登録されたプロバイダーを自動的に呼び出します。 たとえば、*http* スキーマは、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) に登録されます。 ADO では、"http" というプレフィックスが付くすべての URL は、インターネット発行プロバイダーで使用する Web フォルダーまたはファイルを表します。 プロバイダーにより登録されるスキーマの詳細については、使用しているプロバイダーのマニュアルを参照してください。

## <a name="defining-context-with-a-url"></a>URL を使用したコンテキストの定義

[Connection](connection-object-ado.md) オブジェクトで表される開かれた接続の機能の 1 つは、その接続で表されるデータ ソースへの後続の操作を制限することです。つまり、接続によって後続の操作のコンテキストが定義されます。

ADO 2.5 では、絶対 URL でコンテキストを定義することもできます。たとえば、[Record](record-object-ado.md) オブジェクトが絶対 URL で開かれたとき、URL に指定されたリソースを表すために、 **Connection** オブジェクトが暗黙的に作成されます。

コンテキストを定義する絶対 URL は、**Record** オブジェクト [Open](open-method-ado-record.md) メソッドの *ActiveConnection* パラメーターに指定することができます。 絶対 URL は、Connection オブジェクトの Open メソッド ConnectionString パラメーターと Recordset オブジェクト Open メソッド `URL=` [](recordset-object-ado.md)[](open-method-ado-connection.md)*ActiveConnection* パラメーターの新しいキーワードの値として指定することもできます。 [](open-method-ado-recordset.md)

Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.

## <a name="scoped-operations"></a>スコープ操作

コンテキストは同時にスコープ *、つまり*、後続の操作に参加する可能性があるディレクトリとそのサブディレクトリを定義します。 The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](deleterecord-method-ado.md), that operate on a directory and all its subdirectories.

## <a name="relative-urls-as-command-text"></a>コマンド テキストとしての相対 URL

データ ソースで実行されるコマンドを指定する文字列は、**Connection** オブジェクト **Execute** メソッドの *CommandText* パラメーター、および **Recordset** オブジェクト **Open** メソッドの *Source* パラメーター内で指定することができます。

相対 URL は、*CommandText* パラメーターまたは *Source* パラメーター内に指定できます。相対 URL は実際には SQL コマンドなどのコマンドを指定するわけではなく、単にこれらのパラメーター内に指定されるだけです。また、アクティブな接続のコンテキストは絶対 URL である必要があり、*Option* パラメーターは **adCmdTableDirect** に設定する必要があります。

たとえば、次のようにして、Winnt/system32 ディレクトリの Readme25.txt ファイルで **Recordset** を開くことができます。

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

接続文字列の絶対 URL は、サーバー (YourServer) とパス (Winnt) を指定します。 この URL は、コンテキストも定義しています。

コマンド テキストの相対 URL は、絶対 URL を開始点として使用し、パスの残りの部分 (system32) と開くファイル (Readme25.txt) を指定します。

オプション フィールドは、コマンドの種類が相対 URL を示します。

別の例として、次のコードはディレクトリの内容 **に対** して Recordset を開きます。

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a>OLE DB プロバイダー提供の URL スキーム

完全修飾 URL の先頭部分は、URL の残りの部分で識別されるリソースへのアクセスに使用される "スキーマ" です。ここに示す例は、HTTP (ハイパーテキスト転送プロトコル) と FTP (ファイル転送プロトコル) です。

ADO supports OLE DB providers that recognize their own URL schemes. たとえば[、Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)(2000 ファイルの "発行済み" Windowsアクセス) は、既存の HTTP スキームを認識します。

