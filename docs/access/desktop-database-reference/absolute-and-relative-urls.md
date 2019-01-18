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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710329"
---
# <a name="absolute-and-relative-urls"></a><span data-ttu-id="ba0af-102">絶対 URL と相対 URL</span><span class="sxs-lookup"><span data-stu-id="ba0af-102">Absolute and relative URLs</span></span>

<span data-ttu-id="ba0af-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ba0af-103">**Applies to**: Access 2013, Office 2013</span></span>    

<span data-ttu-id="ba0af-104">URL など、ファイル、ディレクトリ、HTML ページ、画像、プログラム、およびように、ローカルまたはネットワーク コンピューターに保存されているターゲットの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-104">A URL specifies the location of a target stored on a local or networked computer, such as a file, directory, HTML page, image, program, and so on.</span></span> <span data-ttu-id="ba0af-105">ここでは、*絶対 URL*は、フォームのです。</span><span class="sxs-lookup"><span data-stu-id="ba0af-105">In this discussion, an *absolute URL* is of the form:</span></span>

<span data-ttu-id="ba0af-106">*scheme://server/path/resource*</span><span class="sxs-lookup"><span data-stu-id="ba0af-106">*scheme://server/path/resource*</span></span>

<span data-ttu-id="ba0af-107">各項目の意味は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ba0af-107">where:</span></span>

|<span data-ttu-id="ba0af-108">名前</span><span class="sxs-lookup"><span data-stu-id="ba0af-108">Name</span></span> |<span data-ttu-id="ba0af-109">説明</span><span class="sxs-lookup"><span data-stu-id="ba0af-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="ba0af-110">*scheme*</span><span class="sxs-lookup"><span data-stu-id="ba0af-110">*scheme*</span></span>|<span data-ttu-id="ba0af-111">*リソース*のアクセス方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-111">Specifies how the *resource* is to be accessed.</span></span>|
|<span data-ttu-id="ba0af-112">*server*</span><span class="sxs-lookup"><span data-stu-id="ba0af-112">*server*</span></span>|<span data-ttu-id="ba0af-113">*リソース*が配置されているコンピューターの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-113">Specifies the name of the computer where the *resource* is located.</span></span>|
|<span data-ttu-id="ba0af-114">*path*</span><span class="sxs-lookup"><span data-stu-id="ba0af-114">*path*</span></span>|<span data-ttu-id="ba0af-p102">ターゲットに導くディレクトリの順序を指定します。*resource* が省略されると、ターゲットは *path* 内の最後のディレクトリと見なされます。</span><span class="sxs-lookup"><span data-stu-id="ba0af-p102">Specifies the sequence of directories leading to the target. If *resource* is omitted, the target is the last directory in *path*.</span></span>|
|<span data-ttu-id="ba0af-117">*resource*</span><span class="sxs-lookup"><span data-stu-id="ba0af-117">*resource*</span></span>|<span data-ttu-id="ba0af-118">含まれる場合、*リソース*は、ターゲットであるし、ファイルの名前は、通常です。</span><span class="sxs-lookup"><span data-stu-id="ba0af-118">If included, *resource* is the target, and is typically the name of a file.</span></span> <span data-ttu-id="ba0af-119">*簡易ファイル*のバイト数、または*構造化ドキュメント*、1 つ以上の記憶域とバイトのバイナリ ストリームを含む単一のバイナリ ストリームを格納しているがある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ba0af-119">It may be a *simple file*, containing a single binary stream of bytes, or a *structured document*, containing one or more storages and binary streams of bytes.</span></span>|

<span data-ttu-id="ba0af-120">*絶対 URL*には、リソースを特定するために必要なすべての情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ba0af-120">An *absolute URL* contains all the information necessary to locate a resource.</span></span>

<span data-ttu-id="ba0af-121">*相対 URL*では、開始点として絶対 URL を使用してリソースを検索します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-121">A *relative URL* locates a resource using an absolute URL as a starting point.</span></span> <span data-ttu-id="ba0af-122">実際には、ターゲットの「完全 URL」は、絶対 url と相対 Url を連結することによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="ba0af-122">In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs.</span></span> <span data-ttu-id="ba0af-123">相対 URL 通常は、のみ*のパス*、および必要に応じて、*リソース*がない*スキーム*または*サーバー*。</span><span class="sxs-lookup"><span data-stu-id="ba0af-123">A relative URL typically consists only of the *path*, and optionally, the *resource*, but no *scheme* or *server*.</span></span>

## <a name="url-scheme-registration"></a><span data-ttu-id="ba0af-124">URL パターンの登録</span><span class="sxs-lookup"><span data-stu-id="ba0af-124">URL scheme registration</span></span>

<span data-ttu-id="ba0af-125">プロバイダーが URL をサポートしている場合、1 つまたは複数の URL スキーマに登録します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-125">If a provider supports URLs, it will register for one or more URL schemes.</span></span> <span data-ttu-id="ba0af-126">つまり、このスキーマを使用する URL は、登録されたプロバイダーを自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-126">This means that any URLs using this scheme will automatically invoke the registered provider.</span></span> <span data-ttu-id="ba0af-127">たとえば、 [Microsoft OLE DB プロバイダー インターネット パブリッシング用](microsoft-ole-db-provider-for-internet-publishing.md)に*http*スキームが登録されています。</span><span class="sxs-lookup"><span data-stu-id="ba0af-127">For example, the *http* scheme is registered to the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="ba0af-128">ADO では、"http"で始まるすべての Url は、web フォルダーまたはインターネット発行プロバイダーで使用するファイルを表すものとします。</span><span class="sxs-lookup"><span data-stu-id="ba0af-128">ADO assumes all URLs prefixed with "http" represent web folders or files to be used with the Internet Publishing Provider.</span></span> <span data-ttu-id="ba0af-129">プロバイダーにより登録されるスキーマの詳細については、使用しているプロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba0af-129">For information about the schemes registered by your provider, see your provider documentation.</span></span>

## <a name="defining-context-with-a-url"></a><span data-ttu-id="ba0af-130">URL を使用してコンテキストを定義します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-130">Defining context with a URL</span></span>

<span data-ttu-id="ba0af-p106">[Connection](connection-object-ado.md) オブジェクトで表される開かれた接続の機能の 1 つは、その接続で表されるデータ ソースへの後続の操作を制限することです。つまり、接続によって後続の操作のコンテキストが定義されます。</span><span class="sxs-lookup"><span data-stu-id="ba0af-p106">One function of an open connection, represented by a [Connection](connection-object-ado.md) object, is to restrict subsequent operations to the data source represented by that connection. That is, the connection defines the context for subsequent operations.</span></span>

<span data-ttu-id="ba0af-p107">ADO 2.5 では、絶対 URL でコンテキストを定義することもできます。たとえば、[Record](record-object-ado.md) オブジェクトが絶対 URL で開かれたとき、URL に指定されたリソースを表すために、 **Connection** オブジェクトが暗黙的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ba0af-p107">With ADO 2.5, an absolute URL may also define a context. For example, when a [Record](record-object-ado.md) object is opened with an absolute URL, a **Connection** object is implicitly created to represent the resource specified by the URL.</span></span>

<span data-ttu-id="ba0af-135">コンテキストを定義する絶対 URL は、 **Record**オブジェクトの[Open](open-method-ado-record.md)メソッドの*ActiveConnection*パラメーターで指定できます。</span><span class="sxs-lookup"><span data-stu-id="ba0af-135">An absolute URL that defines a context may be specified in the *ActiveConnection* parameter of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="ba0af-136">絶対 URL を指定すると、新規の値として`URL=`**接続**オブジェクト[Open](open-method-ado-connection.md)メソッド*接続文字列*パラメーター、および[レコード セット](recordset-object-ado.md)オブジェクトの[Open](open-method-ado-recordset.md)メソッドの*ActiveConnection*のキーワードパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="ba0af-136">An absolute URL may also be specified as the value of the new `URL=` keyword in the **Connection** object [Open](open-method-ado-connection.md) method *ConnectionString* parameter, and the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method *ActiveConnection* parameter.</span></span>

<span data-ttu-id="ba0af-137">ディレクトリを表す、開かれた Record オブジェクトや Recordset オブジェクトは既にコンテキストを指定する Connection オブジェクトを明示的または暗黙的に宣言しているので、これらの Record オブジェクトや Recordset オブジェクトを使用してコンテキストを定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="ba0af-137">Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.</span></span>

## <a name="scoped-operations"></a><span data-ttu-id="ba0af-138">スコープ操作</span><span class="sxs-lookup"><span data-stu-id="ba0af-138">Scoped operations</span></span>

<span data-ttu-id="ba0af-139">コンテキストの*スコープ*を同時に定義する-は、ディレクトリとそのサブディレクトリ以降の操作に参加します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-139">The context simultaneously defines a *scope*—that is, the directory and its subdirectories that may participate in subsequent operations.</span></span> <span data-ttu-id="ba0af-140">**レコード**オブジェクトには、スコープ指定など複数の方法、[つまり](copyrecord-method-ado.md)、[関係](moverecord-method-ado.md)、および[関係する](deleterecord-method-ado.md)ディレクトリとそのすべてのサブディレクトリに対して動作するがあります。</span><span class="sxs-lookup"><span data-stu-id="ba0af-140">The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](deleterecord-method-ado.md), that operate on a directory and all its subdirectories.</span></span>

## <a name="relative-urls-as-command-text"></a><span data-ttu-id="ba0af-141">コマンド テキストとの相対 Url</span><span class="sxs-lookup"><span data-stu-id="ba0af-141">Relative URLs as command text</span></span>

<span data-ttu-id="ba0af-142">オブジェクトの**Execute**メソッドを**接続**する*CommandText*パラメーター、および**Recordset**オブジェクト**Open**メソッドの*ソース*パラメーターでは、データ ソース上で実行するコマンドを指定する文字列を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ba0af-142">A string specifying a command to be executed on the data source may be specified in the **Connection** object **Execute** method *CommandText* parameter, and the **Recordset** object **Open** method *Source* parameter.</span></span>

<span data-ttu-id="ba0af-143">*CommandText*または*ソース*のパラメーターでは、相対 URL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ba0af-143">A relative URL may be specified in the *CommandText* or *Source* parameter.</span></span> <span data-ttu-id="ba0af-144">相対 URL は実際には SQL コマンドなどのコマンドを指定するわけではなく、単にこれらのパラメーター内に指定されるだけです。</span><span class="sxs-lookup"><span data-stu-id="ba0af-144">The relative URL does not actually specify a command (such as an SQL command); it is merely specified in those parameters.</span></span> <span data-ttu-id="ba0af-145">さらに、アクティブな接続のコンテキストは絶対 URL である必要があり、 **adCmdTableDirect**に*オプション*のパラメーターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba0af-145">In addition, the context of the active connection must be an absolute URL, and the *Option* parameter must be set to **adCmdTableDirect**.</span></span>

<span data-ttu-id="ba0af-146">たとえば、次のようにして、Winnt/system32 ディレクトリの Readme25.txt ファイルで **Recordset** を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="ba0af-146">For example, a **Recordset** could be opened on the Readme25.txt file of the Winnt/system32 directory like this:</span></span>

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<span data-ttu-id="ba0af-147">接続文字列に絶対 URL は、サーバー (通常) とパス (Winnt) を指定します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-147">The absolute URL in the connection string specifies the server (YourServer) and the path (Winnt).</span></span> <span data-ttu-id="ba0af-148">この URL は、コンテキストも定義しています。</span><span class="sxs-lookup"><span data-stu-id="ba0af-148">This URL also defines the context.</span></span>

<span data-ttu-id="ba0af-149">コマンド テキスト内の相対 URL では、開始点として絶対 URL を使用し、(system32) のパスとファイルを開くには (Readme25.txt) の残りの部分を指定します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-149">The relative URL in the command text uses the absolute URL as a starting point and specifies the remainder of the path (system32) and the file to open (Readme25.txt).</span></span>

<span data-ttu-id="ba0af-150">[オプション] フィールドは、コマンドの種類が相対 URL であることを示します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-150">The options field indicates that the command type is a relative URL.</span></span>

<span data-ttu-id="ba0af-151">別の例として次のコードは、ディレクトリの内容には、**レコード セット**を開きます。</span><span class="sxs-lookup"><span data-stu-id="ba0af-151">As another example, the following code will open a **Recordset** on the contents of the directory:</span></span>

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a><span data-ttu-id="ba0af-152">OLE DB プロバイダーが指定した URL のスキーム</span><span class="sxs-lookup"><span data-stu-id="ba0af-152">OLE DB provider-supplied URL schemes</span></span>

<span data-ttu-id="ba0af-153">完全修飾 URL の先頭部分は、URL の残りの部分で識別されるリソースへのアクセスに使用する*スキーム*です。</span><span class="sxs-lookup"><span data-stu-id="ba0af-153">The leading part of a fully-qualified URL is the *scheme* used to access the resource identified by the remainder of the URL.</span></span> <span data-ttu-id="ba0af-154">例としては、HTTP (ハイパー テキスト転送プロトコル) および FTP (ファイル転送プロトコル) です。</span><span class="sxs-lookup"><span data-stu-id="ba0af-154">Examples are HTTP (HyperText Transfer Protocol) and FTP (File Transfer Protocol).</span></span>

<span data-ttu-id="ba0af-155">ADO には、独自の URL スキームを認識する OLE DB プロバイダーがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ba0af-155">ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="ba0af-156">たとえば、 [Microsoft OLE DB プロバイダー](microsoft-ole-db-provider-for-internet-publishing.md)するアクセスは、Windows 2000 のファイルを「公開」は、既存の HTTP スキームを認識します。</span><span class="sxs-lookup"><span data-stu-id="ba0af-156">For example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), which accesses "published" Windows 2000 files, recognizes the existing HTTP scheme.</span></span>

