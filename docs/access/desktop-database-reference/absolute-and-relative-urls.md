---
title: 絶対 URL と相対 URL
TOCTitle: Absolute and relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a488617dc7ba0d7d1f7e38391f8382fa1e7ed247
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282102"
---
# <a name="absolute-and-relative-urls"></a>絶対 URL と相対 URL

**適用先:** Access 2013、Office 2013    

URL で、ファイル、ディレクトリ、HTML ページ、画像、プログラムなどの保存先、つまりローカルまたはネットワーク コンピューターでの場所を指定します。 ここでは、"絶対 URL" は次の形式とします。

*scheme://server/path/resource*

各項目の意味は次のとおりです。

|名前 |説明|
|:----|:----------|
|*scheme*|*resource* がどのようにアクセスされるかを指定します。|
|*server*|*resource* が存在するコンピューターの名前を指定します。|
|*path*|ターゲットに導くディレクトリの順序を指定します。 *resource* が省略されると、ターゲットは *path* 内の最後のディレクトリと見なされます。|
|*resource*|指定されている場合、 *resource*はターゲットで、通常はファイルの名前です。 単一のバイナリストリームを含む*単純なファイル*、または1つまたは複数のストレージファイルとバイナリストリームを含む、構造化された*ドキュメント*があります。|

"絶対 URL" には、リソースを検索するために必要なすべての情報が含まれています。

*相対 url*は、開始点として絶対 url を使用してリソースを検索します。 In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs. 通常、相対 URL は*パス*のみで構成され、必要に応じて*リソース*を構成しますが、*スキーム*や*サーバー*は含まれません。

## <a name="url-scheme-registration"></a>URL スキーマの登録

プロバイダーが URL をサポートしている場合、1 つまたは複数の URL スキーマに登録します。 つまり、このスキーマを使用する URL は、登録されたプロバイダーを自動的に呼び出します。 たとえば、*http* スキーマは、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) に登録されます。 ADO では、プレフィックス "http" が付いているすべての url は、インターネット発行プロバイダーで使用する web フォルダーまたはファイルを表しています。 プロバイダーにより登録されるスキーマの詳細については、使用しているプロバイダーのマニュアルを参照してください。

## <a name="defining-context-with-a-url"></a>URL を使用してコンテキストを定義する

[Connection](connection-object-ado.md) オブジェクトで表される開かれた接続の機能の 1 つは、その接続で表されるデータ ソースへの後続の操作を制限することです。つまり、接続によって後続の操作のコンテキストが定義されます。

ADO 2.5 では、絶対 URL でコンテキストを定義することもできます。たとえば、[Record](record-object-ado.md) オブジェクトが絶対 URL で開かれたとき、URL に指定されたリソースを表すために、 **Connection** オブジェクトが暗黙的に作成されます。

コンテキストを定義する絶対 URL は、**Record** オブジェクト [Open](open-method-ado-record.md) メソッドの *ActiveConnection* パラメーターに指定することができます。 また、絶対`URL=` URL は、 **Connection**オブジェクトの[open](open-method-ado-connection.md)メソッドの*ConnectionString*パラメーターで new キーワードの値として指定され、 [Recordset](recordset-object-ado.md)オブジェクトの[open](open-method-ado-recordset.md)メソッドは*ActiveConnection*になります。parameter.

Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.

## <a name="scoped-operations"></a>スコープ指定された操作

コンテキストは、*スコープ*(つまり、以降の操作に参加する可能性があるディレクトリとそのサブディレクトリ) を同時に定義します。 The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](deleterecord-method-ado.md), that operate on a directory and all its subdirectories.

## <a name="relative-urls-as-command-text"></a>コマンドテキストとしての相対 url

データ ソースで実行されるコマンドを指定する文字列は、**Connection** オブジェクト **Execute** メソッドの *CommandText* パラメーター、および **Recordset** オブジェクト **Open** メソッドの *Source* パラメーター内で指定することができます。

相対 URL は、*CommandText* パラメーターまたは *Source* パラメーター内に指定できます。相対 URL は実際には SQL コマンドなどのコマンドを指定するわけではなく、単にこれらのパラメーター内に指定されるだけです。また、アクティブな接続のコンテキストは絶対 URL である必要があり、*Option* パラメーターは **adCmdTableDirect** に設定する必要があります。

たとえば、次のようにして、Winnt/system32 ディレクトリの Readme25.txt ファイルで **Recordset** を開くことができます。

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

接続文字列内の絶対 URL は、サーバー (サーバー名) とパス (Winnt) を指定します。 この URL は、コンテキストも定義しています。

コマンドテキストの相対 url は、絶対 url を開始点として使用し、パスの残りの部分 (system32) と開くファイル (readme25.txt) を指定します。

[オプション] フィールドは、コマンドの種類が相対 URL であることを示します。

もう1つの例として、次のコードでは、ディレクトリの内容に関する**Recordset**を開きます。

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a>OLE DB プロバイダー提供の URL スキーマ

完全修飾 URL の先頭部分は、URL の残りの部分で識別されるリソースへのアクセスに使用される "スキーマ" です。ここに示す例は、HTTP (ハイパーテキスト転送プロトコル) と FTP (ファイル転送プロトコル) です。

ADO supports OLE DB providers that recognize their own URL schemes. たとえば、 [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)は、"公開された" Windows 2000 ファイルにアクセスして、既存の HTTP スキームを認識します。

