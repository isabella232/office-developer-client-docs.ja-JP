---
title: メッセージの添付ファイルを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: eef42a8c7d19af313316bea68624ac67fb1ab4e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799866"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="02a27-103">メッセージの添付ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="02a27-103">Creating a message attachment</span></span>
  
<span data-ttu-id="02a27-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="02a27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="02a27-105">メッセージの添付ファイルは、ファイル、別のメッセージを送信したり、メッセージと共に保存される、OLE オブジェクトなど、いくつかの追加データです。</span><span class="sxs-lookup"><span data-stu-id="02a27-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="02a27-106">各添付ファイルには、それを識別し、その型とそれを表示する方法について説明するプロパティのコレクションがあります。</span><span class="sxs-lookup"><span data-stu-id="02a27-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="02a27-107">受信者と同じようにメッセージの添付ファイルのみアクセスできますに所属しているメッセージです。</span><span class="sxs-lookup"><span data-stu-id="02a27-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="02a27-108">したがっての使用可能な添付ファイルは、そのメッセージを開いていなければなりません。</span><span class="sxs-lookup"><span data-stu-id="02a27-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="02a27-109">メッセージの添付ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="02a27-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="02a27-110">メッセージの[IMessage::CreateAttach](imessage-createattach.md)メソッドを呼び出すし、インターフェイス識別子として NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="02a27-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="02a27-111">**CreateAttach**では、メッセージ内の新しい添付ファイルを一意に識別する番号を返します。</span><span class="sxs-lookup"><span data-stu-id="02a27-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="02a27-112">添付ファイル数は、 **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティに格納され、添付ファイルを含むメッセージが開いている間のみ有効では。</span><span class="sxs-lookup"><span data-stu-id="02a27-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="02a27-113">**PR_ATTACH_METHOD**添付ファイルにアクセスする方法を示すために ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) を設定するのには[IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02a27-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="02a27-114">**PR_ATTACH_METHOD**は、必要があります。</span><span class="sxs-lookup"><span data-stu-id="02a27-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="02a27-115">に設定します。</span><span class="sxs-lookup"><span data-stu-id="02a27-115">Set it to:</span></span> 
    
   - <span data-ttu-id="02a27-116">添付ファイルがバイナリ データである場合は ATTACH_BY_VALUE です。</span><span class="sxs-lookup"><span data-stu-id="02a27-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="02a27-117">ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、または ATTACH_BY_REF_ONLY の添付ファイルがファイルである場合。</span><span class="sxs-lookup"><span data-stu-id="02a27-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="02a27-118">添付ファイルがメッセージの場合は ATTACH_EMBEDDED_MSG です。</span><span class="sxs-lookup"><span data-stu-id="02a27-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="02a27-119">添付ファイルが OLE オブジェクトである場合は ATTACH_OLE です。</span><span class="sxs-lookup"><span data-stu-id="02a27-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="02a27-120">適切な添付ファイルのデータのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="02a27-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="02a27-121">**PR_ATTACH_DATA_BIN**([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) のバイナリ データとオブジェクトを OLE 1 にします。</span><span class="sxs-lookup"><span data-stu-id="02a27-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="02a27-122">**PR_ATTACH_PATHNAME**([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ファイルです。</span><span class="sxs-lookup"><span data-stu-id="02a27-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="02a27-123">**PR_ATTACH_DATA_OBJ**([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) メッセージおよび OLE 2 のオブジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="02a27-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="02a27-124">**PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) ファイルの添付ファイルまたはバイナリ添付ファイルのグラフィック表現を保持するために設定します。</span><span class="sxs-lookup"><span data-stu-id="02a27-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="02a27-125">レンダリング情報を内部的に格納するには、OLE オブジェクトまたは添付されたメッセージの設定の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="02a27-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="02a27-126">**PR_RENDERING_POSITION**添付ファイルを表示するかを示すために ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) を設定します。</span><span class="sxs-lookup"><span data-stu-id="02a27-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="02a27-127">**PR_RENDERING_POSITION**は、 **PR_BODY**プロパティを設定するクライアントにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="02a27-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="02a27-128">**PR_RTF_COMPRESSED**をのみサポートする場合は、圧縮ストリームの次のプレース ホルダー情報を配置します。</span><span class="sxs-lookup"><span data-stu-id="02a27-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="02a27-129">**PR_RENDERING_POSITION**を設定するにしない場合は、序数に基づく文字単位のオフセット、 **PR_BODY**添付ファイルが表示されると、メッセージの場所を把握する必要がある場合に 0 をしているの最初の文字または 0 xffffffff を表す数値を割り当てる**PR_BODY**内の添付ファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="02a27-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="02a27-130">**PR_ATTACH_FILENAME**添付ファイルのファイルの短い名前を指定する ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) を設定し、 **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) がサポートされているファイルの名前を示すためにプラットフォームでは、長いファイル名形式を処理します。</span><span class="sxs-lookup"><span data-stu-id="02a27-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="02a27-131">両方のプロパティはオプションです。</span><span class="sxs-lookup"><span data-stu-id="02a27-131">Both properties are optional.</span></span> <span data-ttu-id="02a27-132">ただし、 **PR_ATTACH_LONG_FILENAME**を設定する場合はまた、 **PR_ATTACH_FILENAME**を設定します。</span><span class="sxs-lookup"><span data-stu-id="02a27-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="02a27-133">**PR_DISPLAY_NAME**ダイアログ ボックスに表示可能な添付ファイルの名前を示す ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を設定します。</span><span class="sxs-lookup"><span data-stu-id="02a27-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="02a27-134">PR_DISPLAY_NAME は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="02a27-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-prattachdatabin"></a><span data-ttu-id="02a27-135">PR_ATTACH_DATA_BIN を設定します。</span><span class="sxs-lookup"><span data-stu-id="02a27-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="02a27-136">**IStream**インターフェイスを使用してプロパティを開くには、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02a27-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="02a27-137">ファイルにデータが含まれているし、開いている場合、またはバッファーのサイズを明示的に制御する必要がある場合は、ストリームにデータを配置するループ内で**IStream::Write**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02a27-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="02a27-138">別のオプションは、データ ファイルにアクセスし、 **OpenProperty**によって返されるストリームにデータをコピーするのには、このストリームの**IStream::CopyTo**メソッドを呼び出すのためのストリームを作成する**OpenStreamOnFile**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="02a27-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="02a27-139">新しいストリームの**IStream::Commit**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02a27-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-prattachdataobj"></a><span data-ttu-id="02a27-140">PR_ATTACH_DATA_OBJ を設定します。</span><span class="sxs-lookup"><span data-stu-id="02a27-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="02a27-141">構造化ストレージと連携するストリームを作成するのには**IStreamDocfile**インターフェイスを使用してプロパティを開くには、 **IMAPIProp::OpenProperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02a27-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="02a27-142">**IStreamDocfile**は、クライアントに格納し、構造化ストレージを取得するパフォーマンスの高い方法を提供するのには、メッセージ ストア プロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="02a27-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="02a27-143">**IStreamDocfile**インターフェイスは**IStream**、ですが、ストリームの内容を保証して、構造化ストレージとして書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="02a27-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="02a27-144">この呼び出しが成功した場合は、 **PR_ATTACH_DATA_BIN**を設定するための同じ手順でストリームを作成します。</span><span class="sxs-lookup"><span data-stu-id="02a27-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="02a27-145">**OpenProperty**が失敗した場合。</span><span class="sxs-lookup"><span data-stu-id="02a27-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="02a27-146">**IStorage**を待ってもう一度**OpenProperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02a27-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="02a27-147">OLE オブジェクトを開き、ストレージ ・ オブジェクトを返すに**StgOpenStorage**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02a27-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="02a27-148">**OpenProperty**から返された記憶域オブジェクトにコピーするのには、返された記憶域オブジェクトの**IStorage::CopyTo**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02a27-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="02a27-149">新しい記憶域オブジェクトの**IStorage::Commit**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02a27-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-prattachpathname"></a><span data-ttu-id="02a27-150">PR_ATTACH_PATHNAME を設定します。</span><span class="sxs-lookup"><span data-stu-id="02a27-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="02a27-151">[SPropValue](spropvalue.md)構造体を割り当て、ファイル名を表す**PR_ATTACH_PATHNAME**と、 **Value.LPSZ**メンバーを文字の文字列を**ulPropTag**のメンバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="02a27-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="02a27-152">添付ファイルの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02a27-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="02a27-153">お使いのプラットフォームでは、長いファイル名をサポートする場合は、 **PR_ATTACH_PATHNAME**と**PR_ATTACH_LONG_PATHNAME**の両方を設定します。</span><span class="sxs-lookup"><span data-stu-id="02a27-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="02a27-154">短いファイル名を取得するために呼び出す、オペレーティング ・ システムが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="02a27-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02a27-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="02a27-155">See also</span></span>

- [<span data-ttu-id="02a27-156">MAPI �̓Y�t�t�@�C��</span><span class="sxs-lookup"><span data-stu-id="02a27-156">MAPI Attachments</span></span>](mapi-attachments.md)

