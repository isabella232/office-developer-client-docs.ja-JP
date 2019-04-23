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
# <a name="absolute-and-relative-urls"></a><span data-ttu-id="61f11-102">絶対 URL と相対 URL</span><span class="sxs-lookup"><span data-stu-id="61f11-102">Absolute and relative URLs</span></span>

<span data-ttu-id="61f11-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="61f11-103">**Applies to**: Access 2013, Office 2013</span></span>    

<span data-ttu-id="61f11-104">URL で、ファイル、ディレクトリ、HTML ページ、画像、プログラムなどの保存先、つまりローカルまたはネットワーク コンピューターでの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="61f11-104">A URL specifies the location of a target stored on a local or networked computer, such as a file, directory, HTML page, image, program, and so on.</span></span> <span data-ttu-id="61f11-105">ここでは、"絶対 URL" は次の形式とします。</span><span class="sxs-lookup"><span data-stu-id="61f11-105">In this discussion, an *absolute URL* is of the form:</span></span>

<span data-ttu-id="61f11-106">*scheme://server/path/resource*</span><span class="sxs-lookup"><span data-stu-id="61f11-106">*scheme://server/path/resource*</span></span>

<span data-ttu-id="61f11-107">各項目の意味は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="61f11-107">where:</span></span>

|<span data-ttu-id="61f11-108">名前</span><span class="sxs-lookup"><span data-stu-id="61f11-108">Name</span></span> |<span data-ttu-id="61f11-109">説明</span><span class="sxs-lookup"><span data-stu-id="61f11-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="61f11-110">*scheme*</span><span class="sxs-lookup"><span data-stu-id="61f11-110">*scheme*</span></span>|<span data-ttu-id="61f11-111">*resource* がどのようにアクセスされるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="61f11-111">Specifies how the *resource* is to be accessed.</span></span>|
|<span data-ttu-id="61f11-112">*server*</span><span class="sxs-lookup"><span data-stu-id="61f11-112">*server*</span></span>|<span data-ttu-id="61f11-113">*resource* が存在するコンピューターの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="61f11-113">Specifies the name of the computer where the *resource* is located.</span></span>|
|<span data-ttu-id="61f11-114">*path*</span><span class="sxs-lookup"><span data-stu-id="61f11-114">*path*</span></span>|<span data-ttu-id="61f11-115">ターゲットに導くディレクトリの順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="61f11-115">Specifies the sequence of directories leading to the target.</span></span> <span data-ttu-id="61f11-116">*resource* が省略されると、ターゲットは *path* 内の最後のディレクトリと見なされます。</span><span class="sxs-lookup"><span data-stu-id="61f11-116">If *resource* is omitted, the target is the last directory in *path*.</span></span>|
|<span data-ttu-id="61f11-117">*resource*</span><span class="sxs-lookup"><span data-stu-id="61f11-117">*resource*</span></span>|<span data-ttu-id="61f11-118">指定されている場合、 *resource*はターゲットで、通常はファイルの名前です。</span><span class="sxs-lookup"><span data-stu-id="61f11-118">If included, *resource* is the target, and is typically the name of a file.</span></span> <span data-ttu-id="61f11-119">単一のバイナリストリームを含む*単純なファイル*、または1つまたは複数のストレージファイルとバイナリストリームを含む、構造化された*ドキュメント*があります。</span><span class="sxs-lookup"><span data-stu-id="61f11-119">It may be a *simple file*, containing a single binary stream of bytes, or a *structured document*, containing one or more storages and binary streams of bytes.</span></span>|

<span data-ttu-id="61f11-120">"絶対 URL" には、リソースを検索するために必要なすべての情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="61f11-120">An *absolute URL* contains all the information necessary to locate a resource.</span></span>

<span data-ttu-id="61f11-121">*相対 url*は、開始点として絶対 url を使用してリソースを検索します。</span><span class="sxs-lookup"><span data-stu-id="61f11-121">A *relative URL* locates a resource using an absolute URL as a starting point.</span></span> <span data-ttu-id="61f11-122">In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs.</span><span class="sxs-lookup"><span data-stu-id="61f11-122">In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs.</span></span> <span data-ttu-id="61f11-123">通常、相対 URL は*パス*のみで構成され、必要に応じて*リソース*を構成しますが、*スキーム*や*サーバー*は含まれません。</span><span class="sxs-lookup"><span data-stu-id="61f11-123">A relative URL typically consists only of the *path*, and optionally, the *resource*, but no *scheme* or *server*.</span></span>

## <a name="url-scheme-registration"></a><span data-ttu-id="61f11-124">URL スキーマの登録</span><span class="sxs-lookup"><span data-stu-id="61f11-124">URL scheme registration</span></span>

<span data-ttu-id="61f11-125">プロバイダーが URL をサポートしている場合、1 つまたは複数の URL スキーマに登録します。</span><span class="sxs-lookup"><span data-stu-id="61f11-125">If a provider supports URLs, it will register for one or more URL schemes.</span></span> <span data-ttu-id="61f11-126">つまり、このスキーマを使用する URL は、登録されたプロバイダーを自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="61f11-126">This means that any URLs using this scheme will automatically invoke the registered provider.</span></span> <span data-ttu-id="61f11-127">たとえば、*http* スキーマは、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) に登録されます。</span><span class="sxs-lookup"><span data-stu-id="61f11-127">For example, the *http* scheme is registered to the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="61f11-128">ADO では、プレフィックス "http" が付いているすべての url は、インターネット発行プロバイダーで使用する web フォルダーまたはファイルを表しています。</span><span class="sxs-lookup"><span data-stu-id="61f11-128">ADO assumes all URLs prefixed with "http" represent web folders or files to be used with the Internet Publishing Provider.</span></span> <span data-ttu-id="61f11-129">プロバイダーにより登録されるスキーマの詳細については、使用しているプロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="61f11-129">For information about the schemes registered by your provider, see your provider documentation.</span></span>

## <a name="defining-context-with-a-url"></a><span data-ttu-id="61f11-130">URL を使用してコンテキストを定義する</span><span class="sxs-lookup"><span data-stu-id="61f11-130">Defining context with a URL</span></span>

<span data-ttu-id="61f11-p106">[Connection](connection-object-ado.md) オブジェクトで表される開かれた接続の機能の 1 つは、その接続で表されるデータ ソースへの後続の操作を制限することです。つまり、接続によって後続の操作のコンテキストが定義されます。</span><span class="sxs-lookup"><span data-stu-id="61f11-p106">One function of an open connection, represented by a [Connection](connection-object-ado.md) object, is to restrict subsequent operations to the data source represented by that connection. That is, the connection defines the context for subsequent operations.</span></span>

<span data-ttu-id="61f11-p107">ADO 2.5 では、絶対 URL でコンテキストを定義することもできます。たとえば、[Record](record-object-ado.md) オブジェクトが絶対 URL で開かれたとき、URL に指定されたリソースを表すために、 **Connection** オブジェクトが暗黙的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="61f11-p107">With ADO 2.5, an absolute URL may also define a context. For example, when a [Record](record-object-ado.md) object is opened with an absolute URL, a **Connection** object is implicitly created to represent the resource specified by the URL.</span></span>

<span data-ttu-id="61f11-135">コンテキストを定義する絶対 URL は、**Record** オブジェクト [Open](open-method-ado-record.md) メソッドの *ActiveConnection* パラメーターに指定することができます。</span><span class="sxs-lookup"><span data-stu-id="61f11-135">An absolute URL that defines a context may be specified in the *ActiveConnection* parameter of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="61f11-136">また、絶対`URL=` URL は、 **Connection**オブジェクトの[open](open-method-ado-connection.md)メソッドの*ConnectionString*パラメーターで new キーワードの値として指定され、 [Recordset](recordset-object-ado.md)オブジェクトの[open](open-method-ado-recordset.md)メソッドは*ActiveConnection*になります。parameter.</span><span class="sxs-lookup"><span data-stu-id="61f11-136">An absolute URL may also be specified as the value of the new `URL=` keyword in the **Connection** object [Open](open-method-ado-connection.md) method *ConnectionString* parameter, and the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method *ActiveConnection* parameter.</span></span>

<span data-ttu-id="61f11-137">Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.</span><span class="sxs-lookup"><span data-stu-id="61f11-137">Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.</span></span>

## <a name="scoped-operations"></a><span data-ttu-id="61f11-138">スコープ指定された操作</span><span class="sxs-lookup"><span data-stu-id="61f11-138">Scoped operations</span></span>

<span data-ttu-id="61f11-139">コンテキストは、*スコープ*(つまり、以降の操作に参加する可能性があるディレクトリとそのサブディレクトリ) を同時に定義します。</span><span class="sxs-lookup"><span data-stu-id="61f11-139">The context simultaneously defines a *scope*—that is, the directory and its subdirectories that may participate in subsequent operations.</span></span> <span data-ttu-id="61f11-140">The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](deleterecord-method-ado.md), that operate on a directory and all its subdirectories.</span><span class="sxs-lookup"><span data-stu-id="61f11-140">The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](deleterecord-method-ado.md), that operate on a directory and all its subdirectories.</span></span>

## <a name="relative-urls-as-command-text"></a><span data-ttu-id="61f11-141">コマンドテキストとしての相対 url</span><span class="sxs-lookup"><span data-stu-id="61f11-141">Relative URLs as command text</span></span>

<span data-ttu-id="61f11-142">データ ソースで実行されるコマンドを指定する文字列は、**Connection** オブジェクト **Execute** メソッドの *CommandText* パラメーター、および **Recordset** オブジェクト **Open** メソッドの *Source* パラメーター内で指定することができます。</span><span class="sxs-lookup"><span data-stu-id="61f11-142">A string specifying a command to be executed on the data source may be specified in the **Connection** object **Execute** method *CommandText* parameter, and the **Recordset** object **Open** method *Source* parameter.</span></span>

<span data-ttu-id="61f11-p110">相対 URL は、*CommandText* パラメーターまたは *Source* パラメーター内に指定できます。相対 URL は実際には SQL コマンドなどのコマンドを指定するわけではなく、単にこれらのパラメーター内に指定されるだけです。また、アクティブな接続のコンテキストは絶対 URL である必要があり、*Option* パラメーターは **adCmdTableDirect** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61f11-p110">A relative URL may be specified in the *CommandText* or *Source* parameter. The relative URL does not actually specify a command (such as an SQL command); it is merely specified in those parameters. In addition, the context of the active connection must be an absolute URL, and the *Option* parameter must be set to **adCmdTableDirect**.</span></span>

<span data-ttu-id="61f11-146">たとえば、次のようにして、Winnt/system32 ディレクトリの Readme25.txt ファイルで **Recordset** を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="61f11-146">For example, a **Recordset** could be opened on the Readme25.txt file of the Winnt/system32 directory like this:</span></span>

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<span data-ttu-id="61f11-147">接続文字列内の絶対 URL は、サーバー (サーバー名) とパス (Winnt) を指定します。</span><span class="sxs-lookup"><span data-stu-id="61f11-147">The absolute URL in the connection string specifies the server (YourServer) and the path (Winnt).</span></span> <span data-ttu-id="61f11-148">この URL は、コンテキストも定義しています。</span><span class="sxs-lookup"><span data-stu-id="61f11-148">This URL also defines the context.</span></span>

<span data-ttu-id="61f11-149">コマンドテキストの相対 url は、絶対 url を開始点として使用し、パスの残りの部分 (system32) と開くファイル (readme25.txt) を指定します。</span><span class="sxs-lookup"><span data-stu-id="61f11-149">The relative URL in the command text uses the absolute URL as a starting point and specifies the remainder of the path (system32) and the file to open (Readme25.txt).</span></span>

<span data-ttu-id="61f11-150">[オプション] フィールドは、コマンドの種類が相対 URL であることを示します。</span><span class="sxs-lookup"><span data-stu-id="61f11-150">The options field indicates that the command type is a relative URL.</span></span>

<span data-ttu-id="61f11-151">もう1つの例として、次のコードでは、ディレクトリの内容に関する**Recordset**を開きます。</span><span class="sxs-lookup"><span data-stu-id="61f11-151">As another example, the following code will open a **Recordset** on the contents of the directory:</span></span>

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a><span data-ttu-id="61f11-152">OLE DB プロバイダー提供の URL スキーマ</span><span class="sxs-lookup"><span data-stu-id="61f11-152">OLE DB provider-supplied URL schemes</span></span>

<span data-ttu-id="61f11-p112">完全修飾 URL の先頭部分は、URL の残りの部分で識別されるリソースへのアクセスに使用される "スキーマ" です。ここに示す例は、HTTP (ハイパーテキスト転送プロトコル) と FTP (ファイル転送プロトコル) です。</span><span class="sxs-lookup"><span data-stu-id="61f11-p112">The leading part of a fully-qualified URL is the *scheme* used to access the resource identified by the remainder of the URL. Examples are HTTP (HyperText Transfer Protocol) and FTP (File Transfer Protocol).</span></span>

<span data-ttu-id="61f11-155">ADO supports OLE DB providers that recognize their own URL schemes.</span><span class="sxs-lookup"><span data-stu-id="61f11-155">ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="61f11-156">たとえば、 [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)は、"公開された" Windows 2000 ファイルにアクセスして、既存の HTTP スキームを認識します。</span><span class="sxs-lookup"><span data-stu-id="61f11-156">For example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), which accesses "published" Windows 2000 files, recognizes the existing HTTP scheme.</span></span>

