---
title: Stream オブジェクト (ADO)
TOCTitle: Stream Object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d689e853f1104305a08c1193b098d99935035092
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478531"
---
# <a name="stream-object-ado"></a><span data-ttu-id="c4364-102">Stream オブジェクト (ADO)</span><span class="sxs-lookup"><span data-stu-id="c4364-102">Stream Object (ADO)</span></span>


<span data-ttu-id="c4364-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4364-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c4364-104">バイナリ データまたはテキストのストリームを表します。</span><span class="sxs-lookup"><span data-stu-id="c4364-104">Represents a stream of binary data or text.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4364-105">備考</span><span class="sxs-lookup"><span data-stu-id="c4364-105">Remarks</span></span>

<span data-ttu-id="c4364-p101">ファイル システムまたは電子メール システムなどの階層化されたツリー構造では、ファイルや電子メールの内容を格納した既定のバイナリ ビット ストリームを [Record](record-object-ado.md) オブジェクトに関連付けることができます。これらのデータ ストリームを格納したフィールドまたはレコードは、 **Stream** オブジェクトを使用して操作できます。 **Stream** オブジェクトは次の方法で取得できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-p101">In tree-structured hierarchies such as a file system or an e-mail system, a [Record](record-object-ado.md) may have a default binary stream of bits associated with it that contains the contents of the file or the e-mail. A **Stream** object can be used to manipulate fields or records containing these streams of data. A **Stream** object can be obtained in these ways:</span></span>

  - <span data-ttu-id="c4364-p102">バイナリ データまたはテキスト データを格納したオブジェクト (通常はファイル) を指定する URL で取得します。このようなオブジェクトには、単純なドキュメント、構造ドキュメントを表す **Record** オブジェクト、またはフォルダーがあります。</span><span class="sxs-lookup"><span data-stu-id="c4364-p102">From a URL pointing to an object (typically a file) containing binary or text data. This object can be a simple document, a **Record** object representing a structured document, or a folder.</span></span>

  - <span data-ttu-id="c4364-p103">**Record** オブジェクトに関連付けられた既定の **Stream** オブジェクトを開いて取得します。 **Record** オブジェクトが開いているときにその **Record** オブジェクトに関連付けられた既定のストリームを取得すると、ストリームを開くときに起こるラウンドトリップを避けることができます。</span><span class="sxs-lookup"><span data-stu-id="c4364-p103">By opening the default **Stream** object associated with a **Record** object. You can obtain the default stream associated with a **Record** object when the **Record** is opened, to eliminate a round-trip just to open the stream.</span></span>

  - <span data-ttu-id="c4364-p104">**Stream** オブジェクトをインスタンス作成して取得します。このような **Stream** オブジェクトは、アプリケーション用のデータの保存に利用できます。URL に関連付けられた **Stream** オブジェクト、または **Record** オブジェクトの既定の **Stream** オブジェクトとは異なり、インスタンス作成した **Stream** オブジェクトは、既定では基になるソースに関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="c4364-p104">By instantiating a **Stream** object. These **Stream** objects can be used to store data for the purposes of your application. Unlike a **Stream** associated with a URL, or the default **Stream** of a **Record**, an instantiated **Stream** has no association with an underlying source by default.</span></span>

<span data-ttu-id="c4364-116">**Stream** オブジェクトのメソッドとプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-116">With the methods and properties of a **Stream** object, you can do the following:</span></span>

  - <span data-ttu-id="c4364-117">**Open** メソッドを使用して、 **Record** または URL から [Stream](open-method-ado-stream.md) オブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="c4364-117">Open a **Stream** object from a **Record** or URL with the [Open](open-method-ado-stream.md) method.</span></span>

  - <span data-ttu-id="c4364-118">**Close** メソッドを使用して、 [Stream](close-method-ado.md) を閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="c4364-118">Close a **Stream** with the [Close](close-method-ado.md) method.</span></span>

  - <span data-ttu-id="c4364-119">**Write** メソッドまたは [WriteText](write-method-ado.md) メソッドを使用して、バイトまたはテキストを [Stream](writetext-method-ado.md) に入力できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-119">Input bytes or text to a **Stream** with the [Write](write-method-ado.md) and [WriteText](writetext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="c4364-120">**Read** メソッドまたは [ReadText](read-method-ado.md) メソッドを使用して、 [Stream](readtext-method-ado.md) からバイトを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="c4364-120">Read bytes from the **Stream** with the [Read](read-method-ado.md) and [ReadText](readtext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="c4364-121">**Flush** メソッドを使用して、ADO バッファーにある [Stream](flush-method-ado.md) データを基になるオブジェクトに書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="c4364-121">Write any **Stream** data still in the ADO buffer to the underlying object with the [Flush](flush-method-ado.md) method.</span></span>

  - <span data-ttu-id="c4364-122">**CopyTo** メソッドを使用して、 **Stream** の内容を別の [Stream](copyto-method-ado.md) にコピーできます。</span><span class="sxs-lookup"><span data-stu-id="c4364-122">Copy the contents of a **Stream** to another **Stream** with the [CopyTo](copyto-method-ado.md) method.</span></span>

  - <span data-ttu-id="c4364-123">[SkipLine](skipline-method-ado.md) メソッドおよび [LineSeparator](lineseparator-property-ado.md) プロパティを使用して、ソース ファイルから行を読み取る方法を制御できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-123">Control how lines are read from the source file with the [SkipLine](skipline-method-ado.md) method and the [LineSeparator](lineseparator-property-ado.md) property.</span></span>

  - <span data-ttu-id="c4364-124">[EOS](eos-property-ado.md) プロパティおよび [SetEOS](seteos-method-ado.md) メソッドを使用して、ストリーム位置の末尾を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-124">Determine the end of stream position with the [EOS](eos-property-ado.md) property and [SetEOS](seteos-method-ado.md) method.</span></span>

  - <span data-ttu-id="c4364-125">[SaveToFile](savetofile-method-ado.md) メソッドおよび [LoadFromFile](loadfromfile-method-ado.md) メソッドを使用して、ファイル内のデータを保存および復元できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-125">Save and restore data in files with the [SaveToFile](savetofile-method-ado.md) and [LoadFromFile](loadfromfile-method-ado.md) methods.</span></span>

  - <span data-ttu-id="c4364-126">**Charset** プロパティを使用して、 [Stream](charset-property-ado.md) の保存に使用する文字セットを指定できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-126">Specify the character set used for storing the **Stream** with the [Charset](charset-property-ado.md) property.</span></span>

  - <span data-ttu-id="c4364-127">**Cancel** メソッドを使用して、非同期 [Stream](cancel-method-ado.md) 操作を停止できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-127">Halt an asynchronous **Stream** operation with the [Cancel](cancel-method-ado.md) method.</span></span>

  - <span data-ttu-id="c4364-128">**Size** プロパティを使用して、 [Stream](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) 内のバイト数を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-128">Determine the number of bytes in a **Stream** with the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) property.</span></span>

  - <span data-ttu-id="c4364-129">**Position** プロパティを使用して、 [Stream](position-property-ado.md) 内の現在の位置を制御できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-129">Control the current position within a **Stream** with the [Position](position-property-ado.md) property.</span></span>

  - <span data-ttu-id="c4364-130">**Type** プロパティを使用して、 [Stream](type-property-ado-stream.md) 内のデータ型を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-130">Determine the type of data in a **Stream** with the [Type](type-property-ado-stream.md) property.</span></span>

  - <span data-ttu-id="c4364-131">**State** プロパティを使用して、 [Stream](state-property-ado.md) の現在の状態 (開いている、閉じている、または実行中) を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-131">Determine the current state of the **Stream** (closed, open, or executing) with the [State](state-property-ado.md) property.</span></span>

  - <span data-ttu-id="c4364-132">**Mode** プロパティを使用して、 [Stream](mode-property-ado.md) のアクセス モードを指定できます。</span><span class="sxs-lookup"><span data-stu-id="c4364-132">Specify the access mode for the **Stream** with the [Mode](mode-property-ado.md) property.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c4364-p105">[!メモ] http スキームを使用している URL は、<A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A> を自動的に呼び出します。詳細については、「 <A href="absolute-and-relative-urls.md">絶対 URL と相対 URL</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4364-p105">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


