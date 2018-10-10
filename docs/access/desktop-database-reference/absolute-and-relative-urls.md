---
title: 絶対 URL と相対 URL
TOCTitle: Absolute and Relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bc0cb3086f8fdfa032c005f7e2d219dab56999b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478967"
---
# <a name="absolute-and-relative-urls"></a>絶対 URL と相対 URL

**適用されます**Access 2013 |。Office 2013 

URL など、ファイル、ディレクトリ、HTML ページ、画像、プログラム、*.* 、ローカルまたはネットワーク コンピューター上の保存先の場所を指定します。 ここでは、*絶対 URL*は、フォームのです。

*scheme://server/path/resource*

各項目の意味は次のとおりです。

  - *scheme*

  - *リソース*のアクセス方法を指定します。

  - *server*

  - *リソース*が配置されているコンピューターの名前を指定します。

  - *path*

  - ターゲットに導くディレクトリの順序を指定します。*resource* が省略されると、ターゲットは *path* 内の最後のディレクトリと見なされます。

  - *resource*

  - 含まれる場合、*リソース*は、ターゲットであるし、ファイルの名前は、通常です。 バイト数、または 1 つ以上の記憶域とバイトのバイナリ ストリームを含む*構造化されたドキュメントは、* 単一のバイナリ ストリームを格納している*単純なファイル*がある可能性があります。

*絶対 URL*には、リソースを特定するために必要なすべての情報が含まれています。

*相対 URL*では、開始点として絶対 URL を使用してリソースを検索します。 実際には、ターゲットの「完全 URL」は、絶対 url と相対 Url を連結することによって指定されます。 相対 URL 通常は、のみ*のパス*、および必要に応じて、*リソース*がない*スキーム*または*サーバー*。

## <a name="url-scheme-registration"></a>URL スキーマ登録

プロバイダーが URL をサポートしている場合、1 つまたは複数の URL スキーマに登録します。 つまり、このスキーマを使用する URL は、登録されたプロバイダーを自動的に呼び出します。 たとえば、 [Microsoft OLE DB プロバイダー インターネット パブリッシング用](microsoft-ole-db-provider-for-internet-publishing.md)に*http*スキームが登録されています。 ADO では、先頭に "http" の付く URL はすべて、Internet Publishing Provider で使用される Web フォルダーまたはファイルを示すことを前提としています。 プロバイダーにより登録されるスキーマの詳細については、使用しているプロバイダーのマニュアルを参照してください。

## <a name="defining-context-with-a-url"></a>URL を使用したコンテキストの定義

[Connection](connection-object-ado.md) オブジェクトで表される開かれた接続の機能の 1 つは、その接続で表されるデータ ソースへの後続の操作を制限することです。つまり、接続によって後続の操作のコンテキストが定義されます。

ADO 2.5 では、絶対 URL でコンテキストを定義することもできます。たとえば、[Record](record-object-ado.md) オブジェクトが絶対 URL で開かれたとき、URL に指定されたリソースを表すために、 **Connection** オブジェクトが暗黙的に作成されます。

コンテキストを定義する絶対 URL は、 **Record**オブジェクトの[Open](open-method-ado-record.md)メソッドの*ActiveConnection*パラメーターで指定できます。 絶対 URL を指定すると、新規の値として"URL**=**"**接続**オブジェクト[Open](open-method-ado-connection.md)メソッド*接続文字列*パラメーター、および[レコード セット](recordset-object-ado.md)オブジェクトの[Open](open-method-ado-recordset.md)メソッドの ActiveConnection を*のキーワード*パラメーター。

ディレクトリを表す、開かれた Record オブジェクトや Recordset オブジェクトは既にコンテキストを指定する Connection オブジェクトを明示的または暗黙的に宣言しているので、これらの Record オブジェクトや Recordset オブジェクトを使用してコンテキストを定義することもできます。

## <a name="scoped-operations"></a>適用範囲についての操作

コンテキストの*スコープ*を同時に定義する-は、ディレクトリとそのサブディレクトリ以降の操作に参加します。 **レコード**オブジェクトには、スコープ指定など複数の方法、[つまり](copyrecord-method-ado.md)、[関係](moverecord-method-ado.md)、および[関係する](https://msdn.microsoft.com/library/jj249832\(v=office.15\))ディレクトリとそのすべてのサブディレクトリに対して動作するがあります。

## <a name="relative-urls-as-command-text"></a>コマンド コンテキストとしての相対 URL

オブジェクトの**Execute**メソッドを**接続**する*CommandText*パラメーター、および**Recordset**オブジェクト**Open**メソッドの*ソース*パラメーターでは、データ ソース上で実行するコマンドを指定する文字列を指定できます。

*CommandText*または*ソース*のパラメーターでは、相対 URL を指定できます。 相対 URL は実際には SQL コマンドなどのコマンドを指定するわけではなく、単にこれらのパラメーター内に指定されるだけです。 さらに、アクティブな接続のコンテキストは絶対 URL である必要があり、 **adCmdTableDirect**に*オプション*のパラメーターを設定する必要があります。

たとえば、次のようにして、Winnt/system32 ディレクトリの Readme25.txt ファイルで **Recordset** を開くことができます。

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

接続文字列に絶対 URL は、サーバー (通常) とパス () とパス (Winnt) を指定します。 この URL は、コンテキストも定義しています。

コマンド テキスト内の相対 URL では、開始点として絶対 URL を使用し、(system32) のパスとファイルを開くには () と、ファイルを開く (Readme25.txt) の残りの部分を指定します。

オプションのフィールド () は、コマンドの種類が相対 URL であることを示します。

別の例として次のコードは、ディレクトリの内容には、**レコード セット**を開きます。

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a>OLE DB プロバイダー供給の URL スキーマ

完全修飾 URL の先頭部分は、URL の残りの部分で識別されるリソースへのアクセスに使用する*スキーム*です。 例としては、HTTP (ハイパー テキスト転送プロトコル) および FTP (ファイル転送プロトコル) です。

ADO には、独自の URL スキームを認識する OLE DB プロバイダーがサポートしています。 たとえば、 [Microsoft OLE DB プロバイダー](microsoft-ole-db-provider-for-internet-publishing.md)*,* するアクセスは、Windows 2000 のファイルを「公開」は、既存の HTTP スキームを認識します。

