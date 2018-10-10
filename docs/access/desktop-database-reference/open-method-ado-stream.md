---
title: Open メソッド (ADO Stream)
TOCTitle: Open Method (ADO Stream)
ms:assetid: fa2e6aaa-e9f5-009c-f3a0-050a00abf9b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250275(v=office.15)
ms:contentKeyID: 48548833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 025a1a5141adab07999337f9cc518edd2b669fdf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479060"
---
# <a name="open-method-ado-stream"></a><span data-ttu-id="b34d2-102">Open メソッド (ADO Stream)</span><span class="sxs-lookup"><span data-stu-id="b34d2-102">Open Method (ADO Stream)</span></span>


<span data-ttu-id="b34d2-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b34d2-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="b34d2-104">バイナリ データまたはテキスト データのストリームを操作するために [Stream](stream-object-ado.md) オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="b34d2-104">Opens a [Stream](stream-object-ado.md) object to manipulate streams of binary or text data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b34d2-105">構文</span><span class="sxs-lookup"><span data-stu-id="b34d2-105">Syntax</span></span>

<span data-ttu-id="b34d2-106">*ストリーム*。</span><span class="sxs-lookup"><span data-stu-id="b34d2-106">*Stream*.</span></span> <span data-ttu-id="b34d2-107">*ソース*、*モード*、 *OpenOptions*、*ユーザー名*、*パスワード*を開く</span><span class="sxs-lookup"><span data-stu-id="b34d2-107">Open *Source*, *Mode*, *OpenOptions*, *UserName*, *Password*</span></span>

## <a name="parameters"></a><span data-ttu-id="b34d2-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b34d2-108">Parameters</span></span>

  - <span data-ttu-id="b34d2-109">*Source*</span><span class="sxs-lookup"><span data-stu-id="b34d2-109">*Source*</span></span>

  - <span data-ttu-id="b34d2-110">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="b34d2-110">Optional.</span></span> <span data-ttu-id="b34d2-111">**ストリーム**のデータのソースを指定する**バリアント型**の値です。</span><span class="sxs-lookup"><span data-stu-id="b34d2-111">A **Variant** value that specifies the source of data for the **Stream**.</span></span> <span data-ttu-id="b34d2-112">*ソース*に、電子メールまたはファイル システムのように、既知のツリー構造内の既存のノードを指す絶対 URL 文字列が含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b34d2-112">*Source* may contain an absolute URL string that points to an existing node in a well-known tree structure, like an e-mail or file system.</span></span> <span data-ttu-id="b34d2-113">URL キーワードを使用して URL を指定する必要があります (「URL://*サーバー*の*設定*を =/*フォルダー*").</span><span class="sxs-lookup"><span data-stu-id="b34d2-113">A URL should be specified using the URL keyword ("URL=*scheme*://*server*/*folder*").</span></span> <span data-ttu-id="b34d2-114">代わりに、*ソース*には、**レコード**に関連付けられた既定ストリームを開きの既に開いている[Record](record-object-ado.md)オブジェクトへの参照が含まれて可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b34d2-114">Alternately, *Source* may contain a reference to an already open [Record](record-object-ado.md) object, which opens the default stream associated with the **Record**.</span></span> <span data-ttu-id="b34d2-115">*ソース*が指定されていない場合、**ストリーム**は、既定でない基になるソースに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="b34d2-115">If *Source* is not specified, a **Stream** is instantiated and opened, associated with no underlying source by default.</span></span> <span data-ttu-id="b34d2-116">URL スキームと、関連付けられているプロバイダーの詳細については、[絶対パスと相対 Url](absolute-and-relative-urls.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b34d2-116">For more information about URL schemes and their associated providers, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span>

  - <span data-ttu-id="b34d2-117">*Mode*</span><span class="sxs-lookup"><span data-stu-id="b34d2-117">*Mode*</span></span>

  - <span data-ttu-id="b34d2-118">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="b34d2-118">Optional.</span></span> <span data-ttu-id="b34d2-119">結果の [Stream](connectmodeenum.md) に対するアクセス モード (読み取り/書き込み、読み取り専用など) を **ConnectModeEnum** 値で指定します。</span><span class="sxs-lookup"><span data-stu-id="b34d2-119">A [ConnectModeEnum](connectmodeenum.md) value that specifies the access mode for the resultant **Stream** (for example, read/write or read-only).</span></span> <span data-ttu-id="b34d2-120">既定値は **adModeUnknown** です。</span><span class="sxs-lookup"><span data-stu-id="b34d2-120">Default value is **adModeUnknown**.</span></span> <span data-ttu-id="b34d2-121">アクセス モードの詳細については、「 [Mode プロパティ (ADO)](mode-property-ado.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b34d2-121">See the [Mode](mode-property-ado.md) property for more information about access modes.</span></span> <span data-ttu-id="b34d2-122">*モード*を指定しない場合は、ソース オブジェクトによって継承されます。</span><span class="sxs-lookup"><span data-stu-id="b34d2-122">If *Mode* is not specified, it is inherited by the source object.</span></span> <span data-ttu-id="b34d2-123">たとえば、ソース **Record** が読み取り専用モードで開かれている場合、既定では、その **Stream** も読み取り専用モードで開かれます。</span><span class="sxs-lookup"><span data-stu-id="b34d2-123">For example, if the source **Record** is opened in read-only mode, the **Stream** will also be opened in read-only mode by default.</span></span>

  - <span data-ttu-id="b34d2-124">*OpenOptions*</span><span class="sxs-lookup"><span data-stu-id="b34d2-124">*OpenOptions*</span></span>

  - <span data-ttu-id="b34d2-p104">省略可能です。[StreamOpenOptionsEnum](streamopenoptionsenum.md) 値を指定します。既定値は **adOpenStreamUnspecified** です。</span><span class="sxs-lookup"><span data-stu-id="b34d2-p104">Optional. A [StreamOpenOptionsEnum](streamopenoptionsenum.md) value. Default value is **adOpenStreamUnspecified**.</span></span>

  - <span data-ttu-id="b34d2-128">*UserName*</span><span class="sxs-lookup"><span data-stu-id="b34d2-128">*UserName*</span></span>

  - <span data-ttu-id="b34d2-p105">省略可能です。必要に応じて、 **Stream** オブジェクトにアクセスするためのユーザー ID を含む、文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b34d2-p105">Optional. A **String** value that contains the user identification that, if needed, accesses the **Stream** object.</span></span>

  - <span data-ttu-id="b34d2-131">*Password*</span><span class="sxs-lookup"><span data-stu-id="b34d2-131">*Password*</span></span>

  - <span data-ttu-id="b34d2-p106">省略可能です。必要に応じて、 **Stream** オブジェクトにアクセスするためのパスワードを含む、文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b34d2-p106">Optional. A **String** value that contains the password that, if needed, accesses the **Stream** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b34d2-134">解説</span><span class="sxs-lookup"><span data-stu-id="b34d2-134">Remarks</span></span>

<span data-ttu-id="b34d2-135">**Record**オブジェクトへのアクセスが用意されているため、ソース パラメーターは、*ユーザー Id*と*パスワード*のパラメーターとしての**Record**オブジェクトが渡されるときは使用されません。</span><span class="sxs-lookup"><span data-stu-id="b34d2-135">When a **Record** object is passed in as the source parameter, the *UserID* and *Password* parameters are not used because access to the **Record** object is already available.</span></span> <span data-ttu-id="b34d2-136">同様に、 **Record**オブジェクトの[モード](mode-property-ado.md)は、**ストリーム**オブジェクトに転送されます。*ソース*が指定されていない、開かれている**ストリーム**はデータが含まれていないと、[サイズ](https://msdn.microsoft.com/library/jj250128\(v=office.15\))はゼロ (0)。</span><span class="sxs-lookup"><span data-stu-id="b34d2-136">Similarly, the [Mode](mode-property-ado.md) of the **Record** object is transferred to the **Stream** object.When *Source* is not specified, the **Stream** opened contains no data and has a [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of zero (0).</span></span> <span data-ttu-id="b34d2-137">**ストリーム**が閉じているときに、この**ストリーム**に書き込まれるすべてのデータが失われるを避けるためには、**ストリーム**を付けて、 [CopyTo](copyto-method-ado.md)メソッドまたは[SaveToFile](savetofile-method-ado.md)メソッド、またはメモリの別の場所に保存します。</span><span class="sxs-lookup"><span data-stu-id="b34d2-137">To avoid losing any data that is written to this **Stream** when the **Stream** is closed, save the **Stream** with the [CopyTo](copyto-method-ado.md) or [SaveToFile](savetofile-method-ado.md) methods, or save it to another memory location.</span></span>

<span data-ttu-id="b34d2-138">*OpenOptions*値の**adOpenStreamFromRecord**は、 *Source*パラメーターを既に開いている**レコード**オブジェクトの内容を識別します。</span><span class="sxs-lookup"><span data-stu-id="b34d2-138">An *OpenOptions* value of **adOpenStreamFromRecord** identifies the contents of the *Source* parameter to be an already open **Record** object.</span></span> <span data-ttu-id="b34d2-139">既定の動作では、ファイルなどのツリー構造内のノードを直接指し示す URL として*Source*を扱います。</span><span class="sxs-lookup"><span data-stu-id="b34d2-139">The default behavior is to treat *Source* as a URL that points directly to a node in a tree structure, such as a file.</span></span> <span data-ttu-id="b34d2-140">そのノードに関連付けられる既定のストリームが開かれます。</span><span class="sxs-lookup"><span data-stu-id="b34d2-140">The default stream associated with that node is opened.</span></span>

<span data-ttu-id="b34d2-p109">**Stream** が開かれていないときは、 **Stream** の読み取り専用プロパティをすべて読み取ることができます。 **Stream** が非同期で開かれている場合、以降のすべての操作 ( [State](state-property-ado.md) プロパティやその他の読み取り専用プロパティの確認を除く) は、 **Open** 操作が完了するまでブロックされます。</span><span class="sxs-lookup"><span data-stu-id="b34d2-p109">While the **Stream** is not open, it is possible to read all the read-only properties of the **Stream**. If a **Stream** is opened asynchronously, all subsequent operations (other than checking the [State](state-property-ado.md) and other read-only properties) are blocked until the **Open** operation is completed.</span></span>

<span data-ttu-id="b34d2-p110">上で説明したオプションに加えて、*Source* を指定しないことにより、基になるソースに関連付けることなく、**Stream** オブジェクトのインスタンスをメモリ内に作成することができます。ストリームにデータを動的に追加するには、[Write](write-method-ado.md) または [WriteText](writetext-method-ado.md) を使用してバイナリ データまたはテキスト データを **Stream** に書き込むか、または [LoadFromFile](loadfromfile-method-ado.md) を使用してデータをファイルから読み込みます。</span><span class="sxs-lookup"><span data-stu-id="b34d2-p110">In addition to the options discussed above, by not specifying *Source*, you can simply instantiate a **Stream** object in memory without associating it with an underlying source. You can dynamically add data to the stream simply by writing binary or text data to the **Stream** with [Write](write-method-ado.md) or [WriteText](writetext-method-ado.md), or by loading data from a file with [LoadFromFile](loadfromfile-method-ado.md).</span></span>
