---
title: メッセージの添付ファイルの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2bdba3574c962c825f45cd098efa1cba6e21a4ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332943"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="bcb6c-103">メッセージの添付ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="bcb6c-103">Creating a message attachment</span></span>
  
<span data-ttu-id="bcb6c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcb6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcb6c-105">メッセージの添付ファイルは、メッセージと共に送信または保存できる、ファイル、別のメッセージ、または OLE オブジェクトなどの追加データです。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="bcb6c-106">各添付ファイルには、それを識別し、その種類とその表示方法を説明するプロパティのコレクションがあります。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="bcb6c-107">受信者と同様に、メッセージの添付ファイルには、属しているメッセージを介してのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="bcb6c-108">そのため、添付ファイルを使用できるようにするには、メッセージを開いておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="bcb6c-109">メッセージの添付ファイルを作成する</span><span class="sxs-lookup"><span data-stu-id="bcb6c-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="bcb6c-110">メッセージの[IMessage:: createattach](imessage-createattach.md)メソッドを呼び出し、インターフェイス識別子として NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="bcb6c-111">**createattach**は、メッセージ内の新しい添付ファイルを一意に識別する番号を返します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="bcb6c-112">添付ファイルの番号は、 **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティに格納され、添付ファイルを含むメッセージが開いている間のみ有効です。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="bcb6c-113">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) を呼び出して、添付ファイルへのアクセス方法を示すように、 [imapiprop:: setprops](imapiprop-setprops.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="bcb6c-114">**PR_ATTACH_METHOD**が必要です。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="bcb6c-115">次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-115">Set it to:</span></span> 
    
   - <span data-ttu-id="bcb6c-116">添付ファイルがバイナリデータの場合は ATTACH_BY_VALUE。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="bcb6c-117">添付ファイルがファイルの場合は、ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、または ATTACH_BY_REF_ONLY。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="bcb6c-118">添付ファイルがメッセージの場合は ATTACH_EMBEDDED_MSG。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="bcb6c-119">添付ファイルが OLE オブジェクトの場合は ATTACH_OLE。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="bcb6c-120">適切な添付ファイルデータのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="bcb6c-121">**PR_ATTACH_DATA_BIN**([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) バイナリデータおよび OLE 1 オブジェクトを対象としています。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="bcb6c-122">**PR_ATTACH_PATHNAME**([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="bcb6c-123">**PR_ATTACH_DATA_OBJ**([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) メッセージおよび OLE 2 オブジェクトの場合。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="bcb6c-124">**PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) を設定して、ファイルまたはバイナリの添付ファイルのグラフィック表現を保持します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="bcb6c-125">OLE オブジェクトには、レンダリング情報を内部的に保存するか、添付されたメッセージを格納するように設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="bcb6c-126">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) を設定して、添付ファイルを表示する場所を示します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="bcb6c-127">**PR_RENDERING_POSITION**は、 **PR_BODY**プロパティを設定するクライアントにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="bcb6c-128">**PR_RTF_COMPRESSED**のみをサポートしている場合は、次のプレースホルダー情報を圧縮ストリームに配置します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="bcb6c-129">**PR_RENDERING_POSITION**を設定するには、序数オフセットを文字で表す数値を指定します。 **PR_BODY**の最初の文字は0に、添付ファイルがレンダリングされるメッセージ内の場所を知る必要がある場合は、0xffffffff、または0xffffffff**PR_BODY**内で添付ファイルをレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="bcb6c-130">**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) を設定して、ファイル添付ファイルのファイルの短い形式の名前と**\_PR ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) を指定し、ファイル名を指定します。ロングファイル形式を処理するプラットフォーム上。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="bcb6c-131">両方のプロパティは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-131">Both properties are optional.</span></span> <span data-ttu-id="bcb6c-132">ただし、 **PR_ATTACH_LONG_FILENAME**を設定する場合は、 **PR_ATTACH_FILENAME**も設定します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="bcb6c-133">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を設定して、ダイアログボックスに表示できる添付ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="bcb6c-134">PR_DISPLAY_NAME は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-prattachdatabin"></a><span data-ttu-id="bcb6c-135">PR_ATTACH_DATA_BIN の設定</span><span class="sxs-lookup"><span data-stu-id="bcb6c-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="bcb6c-136">**IStream**インターフェイスを使用してプロパティを開くには、 [imapiprop:: openproperty](imapiprop-openproperty.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="bcb6c-137">ファイルにデータが含まれていて、開かれている場合、またはバッファーサイズを明示的に制御する必要がある場合は、 **IStream:: Write** in ループを使用してデータをストリームに格納します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="bcb6c-138">別の方法として、 **openstreamonfile**を呼び出してデータファイルにアクセスするストリームを作成し、このストリームの**IStream:: CopyTo**メソッドを呼び出して、 **openproperty**によって返されるストリームにデータをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="bcb6c-139">新しいストリームの**IStream:: Commit**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-prattachdataobj"></a><span data-ttu-id="bcb6c-140">PR_ATTACH_DATA_OBJ の設定</span><span class="sxs-lookup"><span data-stu-id="bcb6c-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="bcb6c-141">**IStreamDocfile**インターフェイスを使用してプロパティを開き、構造化ストレージと連携するストリームを作成するには、 **imapiprop:: openproperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="bcb6c-142">**IStreamDocfile**は、構造化ストレージを格納して取得するためのパフォーマンスの高い方法をクライアントに提供するために、メッセージストアプロバイダーによって実装されています。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="bcb6c-143">**IStreamDocfile**インターフェイスは**IStream**と同じですが、ストリームの内容は構造化ストレージとして書式設定されることが保証されています。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="bcb6c-144">この呼び出しが正常に終了した場合は、 **PR_ATTACH_DATA_BIN**の設定についての説明と同じ手順でストリームを作成します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="bcb6c-145">**openproperty**が失敗した場合:</span><span class="sxs-lookup"><span data-stu-id="bcb6c-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="bcb6c-146">**IStorage**を再度呼び出すには、 **openproperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="bcb6c-147">**StgOpenStorage**を呼び出して、OLE オブジェクトを開き、ストレージオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="bcb6c-148">返されたストレージオブジェクトの**IStorage:: CopyTo**メソッドを呼び出して、 **openproperty**から返されたストレージオブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="bcb6c-149">新しいストレージオブジェクトの**IStorage:: Commit**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-prattachpathname"></a><span data-ttu-id="bcb6c-150">PR_ATTACH_PATHNAME の設定</span><span class="sxs-lookup"><span data-stu-id="bcb6c-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="bcb6c-151">[spropvalue](spropvalue.md)構造体を割り当て、 **ulPropTag**メンバーを**PR_ATTACH_PATHNAME**に設定し、 **LPSZ**メンバーをファイル名を表す文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="bcb6c-152">添付ファイルの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="bcb6c-153">プラットフォームが長いファイル名をサポートしている場合は、 **PR_ATTACH_PATHNAME**と**PR_ATTACH_LONG_PATHNAME**の両方を設定します。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="bcb6c-154">短いファイル名を取得するには、オペレーティングシステムの呼び出しを行う必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="bcb6c-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bcb6c-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="bcb6c-155">See also</span></span>

- [<span data-ttu-id="bcb6c-156">MAPI 添付ファイル</span><span class="sxs-lookup"><span data-stu-id="bcb6c-156">MAPI Attachments</span></span>](mapi-attachments.md)

