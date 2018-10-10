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
# <a name="absolute-and-relative-urls"></a><span data-ttu-id="f4390-102">絶対 URL と相対 URL</span><span class="sxs-lookup"><span data-stu-id="f4390-102">Absolute and Relative URLs</span></span>

<span data-ttu-id="f4390-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4390-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="f4390-104">URL など、ファイル、ディレクトリ、HTML ページ、画像、プログラム、*.* 、ローカルまたはネットワーク コンピューター上の保存先の場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4390-104">A URL specifies the location of a target stored on a local or networked computer, such as a file, directory, HTML page, image, program, and so on *.*</span></span> <span data-ttu-id="f4390-105">ここでは、*絶対 URL*は、フォームのです。</span><span class="sxs-lookup"><span data-stu-id="f4390-105">In this discussion, an *absolute URL* is of the form:</span></span>

<span data-ttu-id="f4390-106">*scheme://server/path/resource*</span><span class="sxs-lookup"><span data-stu-id="f4390-106">*scheme://server/path/resource*</span></span>

<span data-ttu-id="f4390-107">各項目の意味は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f4390-107">where:</span></span>

  - <span data-ttu-id="f4390-108">*scheme*</span><span class="sxs-lookup"><span data-stu-id="f4390-108">*scheme*</span></span>

  - <span data-ttu-id="f4390-109">*リソース*のアクセス方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4390-109">Specifies how the *resource* is to be accessed.</span></span>

  - <span data-ttu-id="f4390-110">*server*</span><span class="sxs-lookup"><span data-stu-id="f4390-110">*server*</span></span>

  - <span data-ttu-id="f4390-111">*リソース*が配置されているコンピューターの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4390-111">Specifies the name of the computer where the *resource* is located.</span></span>

  - <span data-ttu-id="f4390-112">*path*</span><span class="sxs-lookup"><span data-stu-id="f4390-112">*path*</span></span>

  - <span data-ttu-id="f4390-p102">ターゲットに導くディレクトリの順序を指定します。*resource* が省略されると、ターゲットは *path* 内の最後のディレクトリと見なされます。</span><span class="sxs-lookup"><span data-stu-id="f4390-p102">Specifies the sequence of directories leading to the target. If *resource* is omitted, the target is the last directory in *path*.</span></span>

  - <span data-ttu-id="f4390-115">*resource*</span><span class="sxs-lookup"><span data-stu-id="f4390-115">*resource*</span></span>

  - <span data-ttu-id="f4390-116">含まれる場合、*リソース*は、ターゲットであるし、ファイルの名前は、通常です。</span><span class="sxs-lookup"><span data-stu-id="f4390-116">If included, *resource* is the target, and is typically the name of a file.</span></span> <span data-ttu-id="f4390-117">バイト数、または 1 つ以上の記憶域とバイトのバイナリ ストリームを含む*構造化されたドキュメントは、* 単一のバイナリ ストリームを格納している*単純なファイル*がある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f4390-117">It may be a *simple file,* containing a single binary stream of bytes, or a *structured document,* containing one or more storages and binary streams of bytes.</span></span>

<span data-ttu-id="f4390-118">*絶対 URL*には、リソースを特定するために必要なすべての情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f4390-118">An *absolute URL* contains all the information necessary to locate a resource.</span></span>

<span data-ttu-id="f4390-119">*相対 URL*では、開始点として絶対 URL を使用してリソースを検索します。</span><span class="sxs-lookup"><span data-stu-id="f4390-119">A *relative URL* locates a resource using an absolute URL as a starting point.</span></span> <span data-ttu-id="f4390-120">実際には、ターゲットの「完全 URL」は、絶対 url と相対 Url を連結することによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="f4390-120">In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs.</span></span> <span data-ttu-id="f4390-121">相対 URL 通常は、のみ*のパス*、および必要に応じて、*リソース*がない*スキーム*または*サーバー*。</span><span class="sxs-lookup"><span data-stu-id="f4390-121">A relative URL typically consists only of the *path*, and optionally, the *resource*, but no *scheme* or *server*.</span></span>

## <a name="url-scheme-registration"></a><span data-ttu-id="f4390-122">URL スキーマ登録</span><span class="sxs-lookup"><span data-stu-id="f4390-122">URL Scheme Registration</span></span>

<span data-ttu-id="f4390-123">プロバイダーが URL をサポートしている場合、1 つまたは複数の URL スキーマに登録します。</span><span class="sxs-lookup"><span data-stu-id="f4390-123">If a provider supports URLs, it will register for one or more URL schemes.</span></span> <span data-ttu-id="f4390-124">つまり、このスキーマを使用する URL は、登録されたプロバイダーを自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f4390-124">This means that any URLs using this scheme will automatically invoke the registered provider.</span></span> <span data-ttu-id="f4390-125">たとえば、 [Microsoft OLE DB プロバイダー インターネット パブリッシング用](microsoft-ole-db-provider-for-internet-publishing.md)に*http*スキームが登録されています。</span><span class="sxs-lookup"><span data-stu-id="f4390-125">For example, the *http* scheme is registered to the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="f4390-126">ADO では、先頭に "http" の付く URL はすべて、Internet Publishing Provider で使用される Web フォルダーまたはファイルを示すことを前提としています。</span><span class="sxs-lookup"><span data-stu-id="f4390-126">ADO assumes all URLs prefixed with "http" represent Web folders or files to be used with the Internet Publishing Provider.</span></span> <span data-ttu-id="f4390-127">プロバイダーにより登録されるスキーマの詳細については、使用しているプロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4390-127">For information about the schemes registered by your provider, see your provider documentation.</span></span>

## <a name="defining-context-with-a-url"></a><span data-ttu-id="f4390-128">URL を使用したコンテキストの定義</span><span class="sxs-lookup"><span data-stu-id="f4390-128">Defining Context with a URL</span></span>

<span data-ttu-id="f4390-p106">[Connection](connection-object-ado.md) オブジェクトで表される開かれた接続の機能の 1 つは、その接続で表されるデータ ソースへの後続の操作を制限することです。つまり、接続によって後続の操作のコンテキストが定義されます。</span><span class="sxs-lookup"><span data-stu-id="f4390-p106">One function of an open connection, represented by a [Connection](connection-object-ado.md) object, is to restrict subsequent operations to the data source represented by that connection. That is, the connection defines the context for subsequent operations.</span></span>

<span data-ttu-id="f4390-p107">ADO 2.5 では、絶対 URL でコンテキストを定義することもできます。たとえば、[Record](record-object-ado.md) オブジェクトが絶対 URL で開かれたとき、URL に指定されたリソースを表すために、 **Connection** オブジェクトが暗黙的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="f4390-p107">With ADO 2.5, an absolute URL may also define a context. For example, when a [Record](record-object-ado.md) object is opened with an absolute URL, a **Connection** object is implicitly created to represent the resource specified by the URL.</span></span>

<span data-ttu-id="f4390-133">コンテキストを定義する絶対 URL は、 **Record**オブジェクトの[Open](open-method-ado-record.md)メソッドの*ActiveConnection*パラメーターで指定できます。</span><span class="sxs-lookup"><span data-stu-id="f4390-133">An absolute URL that defines a context may be specified in the *ActiveConnection* parameter of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="f4390-134">絶対 URL を指定すると、新規の値として"URL**=**"**接続**オブジェクト[Open](open-method-ado-connection.md)メソッド*接続文字列*パラメーター、および[レコード セット](recordset-object-ado.md)オブジェクトの[Open](open-method-ado-recordset.md)メソッドの ActiveConnection を*のキーワード*パラメーター。</span><span class="sxs-lookup"><span data-stu-id="f4390-134">An absolute URL may also be specified as the value of the new "URL**=**" keyword in the **Connection** object [Open](open-method-ado-connection.md) method *ConnectionString* parameter, and the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method *ActiveConnection* parameter.</span></span>

<span data-ttu-id="f4390-135">ディレクトリを表す、開かれた Record オブジェクトや Recordset オブジェクトは既にコンテキストを指定する Connection オブジェクトを明示的または暗黙的に宣言しているので、これらの Record オブジェクトや Recordset オブジェクトを使用してコンテキストを定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="f4390-135">Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.</span></span>

## <a name="scoped-operations"></a><span data-ttu-id="f4390-136">適用範囲についての操作</span><span class="sxs-lookup"><span data-stu-id="f4390-136">Scoped Operations</span></span>

<span data-ttu-id="f4390-137">コンテキストの*スコープ*を同時に定義する-は、ディレクトリとそのサブディレクトリ以降の操作に参加します。</span><span class="sxs-lookup"><span data-stu-id="f4390-137">The context simultaneously defines a *scope* — that is, the directory and its subdirectories that may participate in subsequent operations.</span></span> <span data-ttu-id="f4390-138">**レコード**オブジェクトには、スコープ指定など複数の方法、[つまり](copyrecord-method-ado.md)、[関係](moverecord-method-ado.md)、および[関係する](https://msdn.microsoft.com/library/jj249832\(v=office.15\))ディレクトリとそのすべてのサブディレクトリに対して動作するがあります。</span><span class="sxs-lookup"><span data-stu-id="f4390-138">The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), that operate on a directory and all its subdirectories.</span></span>

## <a name="relative-urls-as-command-text"></a><span data-ttu-id="f4390-139">コマンド コンテキストとしての相対 URL</span><span class="sxs-lookup"><span data-stu-id="f4390-139">Relative URLs as Command Text</span></span>

<span data-ttu-id="f4390-140">オブジェクトの**Execute**メソッドを**接続**する*CommandText*パラメーター、および**Recordset**オブジェクト**Open**メソッドの*ソース*パラメーターでは、データ ソース上で実行するコマンドを指定する文字列を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f4390-140">A string specifying a command to be executed on the data source may be specified in the **Connection** object **Execute** method *CommandText* parameter, and the **Recordset** object **Open** method *Source* parameter.</span></span>

<span data-ttu-id="f4390-141">*CommandText*または*ソース*のパラメーターでは、相対 URL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f4390-141">A relative URL may be specified in the *CommandText* or *Source* parameter.</span></span> <span data-ttu-id="f4390-142">相対 URL は実際には SQL コマンドなどのコマンドを指定するわけではなく、単にこれらのパラメーター内に指定されるだけです。</span><span class="sxs-lookup"><span data-stu-id="f4390-142">The relative URL does not actually specify a command (such as an SQL command); it is merely specified in those parameters.</span></span> <span data-ttu-id="f4390-143">さらに、アクティブな接続のコンテキストは絶対 URL である必要があり、 **adCmdTableDirect**に*オプション*のパラメーターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4390-143">In addition, the context of the active connection must be an absolute URL, and the *Option* parameter must be set to **adCmdTableDirect**.</span></span>

<span data-ttu-id="f4390-144">たとえば、次のようにして、Winnt/system32 ディレクトリの Readme25.txt ファイルで **Recordset** を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="f4390-144">For example, a **Recordset** could be opened on the Readme25.txt file of the Winnt/system32 directory like this:</span></span>

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<span data-ttu-id="f4390-145">接続文字列に絶対 URL は、サーバー (通常) とパス () とパス (Winnt) を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4390-145">The absolute URL in the connection string specifies the server (YourServer ) and the path () and the path (Winnt ).</span></span> <span data-ttu-id="f4390-146">この URL は、コンテキストも定義しています。</span><span class="sxs-lookup"><span data-stu-id="f4390-146">This URL also defines the context.</span></span>

<span data-ttu-id="f4390-147">コマンド テキスト内の相対 URL では、開始点として絶対 URL を使用し、(system32) のパスとファイルを開くには () と、ファイルを開く (Readme25.txt) の残りの部分を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4390-147">The relative URL in the command text uses the absolute URL as a starting point and specifies the remainder of the path (system32 ) and the file to open () and the file to open (Readme25.txt ).</span></span>

<span data-ttu-id="f4390-148">オプションのフィールド () は、コマンドの種類が相対 URL であることを示します。</span><span class="sxs-lookup"><span data-stu-id="f4390-148">The options field () indicates that the command type is a relative URL.</span></span>

<span data-ttu-id="f4390-149">別の例として次のコードは、ディレクトリの内容には、**レコード セット**を開きます。</span><span class="sxs-lookup"><span data-stu-id="f4390-149">As another example, the following code will open a **Recordset** on the contents of the directory:</span></span>

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a><span data-ttu-id="f4390-150">OLE DB プロバイダー供給の URL スキーマ</span><span class="sxs-lookup"><span data-stu-id="f4390-150">OLE DB Provider-Supplied URL Schemes</span></span>

<span data-ttu-id="f4390-151">完全修飾 URL の先頭部分は、URL の残りの部分で識別されるリソースへのアクセスに使用する*スキーム*です。</span><span class="sxs-lookup"><span data-stu-id="f4390-151">The leading part of a fully-qualified URL is the *scheme* used to access the resource identified by the remainder of the URL.</span></span> <span data-ttu-id="f4390-152">例としては、HTTP (ハイパー テキスト転送プロトコル) および FTP (ファイル転送プロトコル) です。</span><span class="sxs-lookup"><span data-stu-id="f4390-152">Examples are HTTP (HyperText Transfer Protocol) and FTP (File Transfer Protocol).</span></span>

<span data-ttu-id="f4390-153">ADO には、独自の URL スキームを認識する OLE DB プロバイダーがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f4390-153">ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="f4390-154">たとえば、 [Microsoft OLE DB プロバイダー](microsoft-ole-db-provider-for-internet-publishing.md)*,* するアクセスは、Windows 2000 のファイルを「公開」は、既存の HTTP スキームを認識します。</span><span class="sxs-lookup"><span data-stu-id="f4390-154">For example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses "published" Windows 2000 files, recognizes the existing HTTP scheme.</span></span>

