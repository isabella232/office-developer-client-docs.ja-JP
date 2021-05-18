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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405997"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="4245a-103">メッセージの添付ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="4245a-103">Creating a message attachment</span></span>
  
<span data-ttu-id="4245a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4245a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4245a-105">メッセージ添付ファイルは、ファイル、別のメッセージ、OLE オブジェクトなどの追加のデータで、メッセージと共に送信または保存できます。</span><span class="sxs-lookup"><span data-stu-id="4245a-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="4245a-106">各添付ファイルには、それを識別し、その種類とそのレンダリング方法を記述するプロパティのコレクションがあります。</span><span class="sxs-lookup"><span data-stu-id="4245a-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="4245a-107">受信者と同様に、メッセージの添付ファイルにアクセスできるのは、その添付ファイルが属するメッセージのみです。</span><span class="sxs-lookup"><span data-stu-id="4245a-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="4245a-108">したがって、添付ファイルを使用するには、そのメッセージを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="4245a-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="4245a-109">メッセージ添付ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="4245a-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="4245a-110">メッセージの [IMessage::CreateAttach メソッドを呼び出](imessage-createattach.md) し、インターフェイス識別子として NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="4245a-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="4245a-111">**CreateAttach** は、メッセージ内の新しい添付ファイルを一意に識別する番号を返します。</span><span class="sxs-lookup"><span data-stu-id="4245a-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="4245a-112">添付ファイル番号は PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティに格納され、添付ファイルを含むメッセージが開いている限り有効です。</span><span class="sxs-lookup"><span data-stu-id="4245a-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="4245a-113">[IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出して、PR_ATTACH_METHOD[(PidTagAttachMethod)](pidtagattachmethod-canonical-property.md)を設定して、添付ファイルにアクセスする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4245a-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="4245a-114">**PR_ATTACH_METHOD** 必要です。</span><span class="sxs-lookup"><span data-stu-id="4245a-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="4245a-115">次の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="4245a-115">Set it to:</span></span> 
    
   - <span data-ttu-id="4245a-116">ATTACH_BY_VALUEがバイナリ データの場合は、この値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4245a-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="4245a-117">ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、または添付ATTACH_BY_REF_ONLYファイルの場合は、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="4245a-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="4245a-118">ATTACH_EMBEDDED_MSGメッセージの場合は、添付ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="4245a-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="4245a-119">ATTACH_OLEが OLE オブジェクトの場合は、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="4245a-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="4245a-120">適切な添付ファイル データ プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4245a-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="4245a-121">**PR_ATTACH_DATA_BIN** データおよび OLE 1 オブジェクトの場合は、 ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) を使用します。</span><span class="sxs-lookup"><span data-stu-id="4245a-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="4245a-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) を使用します。</span><span class="sxs-lookup"><span data-stu-id="4245a-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="4245a-123">**PR_ATTACH_DATA_OBJ** と OLE 2 オブジェクトの場合は、 ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) を使用します。</span><span class="sxs-lookup"><span data-stu-id="4245a-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="4245a-124">ファイル **PR_ATTACH_RENDERING** バイナリ添付ファイルの添付ファイルのグラフィック表現を保持する場合は、[ファイル][(PidTagAttachRendering)](pidtagattachrendering-canonical-property.md)を設定します。</span><span class="sxs-lookup"><span data-stu-id="4245a-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="4245a-125">レンダリング情報を内部的に格納する OLE オブジェクト、または添付メッセージには設定しません。</span><span class="sxs-lookup"><span data-stu-id="4245a-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="4245a-126">添付 **PR_RENDERING_POSITION** を表示する場所を示すプロパティ [(PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)を設定します。</span><span class="sxs-lookup"><span data-stu-id="4245a-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="4245a-127">**PR_RENDERING_POSITION** プロパティを設定するクライアントにのみ **PR_BODY** されます。</span><span class="sxs-lookup"><span data-stu-id="4245a-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="4245a-128">データの取得のみをサポート **PR_RTF_COMPRESSED、** 次のプレースホルダー情報を圧縮ストリームに配置します。</span><span class="sxs-lookup"><span data-stu-id="4245a-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="4245a-129">PR_RENDERING_POSITIONを設定するには、メッセージ内で添付ファイルがレンダリングされる場所を知る必要がある場合は **、PR_BODY** の最初の文字を 0 に、文字で序数オフセットを表す数値を割り当てるか、PR_BODY 内で添付ファイルをレンダリングしない場合は 0xFFFFFFFF を **割** り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4245a-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="4245a-130">**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) を設定して、ファイル添付ファイルのファイルの短い名前を示し **、PR \_ ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) は、長いファイル名の形式を処理するプラットフォームでサポートされているファイルの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="4245a-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="4245a-131">どちらのプロパティもオプションです。</span><span class="sxs-lookup"><span data-stu-id="4245a-131">Both properties are optional.</span></span> <span data-ttu-id="4245a-132">ただし、このプロパティを **設定PR_ATTACH_LONG_FILENAME、\*\*\*\*設定も** PR_ATTACH_FILENAME。</span><span class="sxs-lookup"><span data-stu-id="4245a-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="4245a-133">**[PR_DISPLAY_NAME** ] ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を設定して、ダイアログ ボックスに表示できる添付ファイルの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="4245a-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="4245a-134">PR_DISPLAY_NAMEオプションです。</span><span class="sxs-lookup"><span data-stu-id="4245a-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-pr_attach_data_bin"></a><span data-ttu-id="4245a-135">設定PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="4245a-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="4245a-136">[IMAPIProp::OpenProperty を](imapiprop-openproperty.md)呼び出して **、IStream インターフェイスでプロパティを開** きます。</span><span class="sxs-lookup"><span data-stu-id="4245a-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="4245a-137">ファイルにデータが含まれており、開いている場合、またはバッファー サイズを明示的に制御する必要がある場合は、ループ内で **IStream::Write** を呼び出して、データをストリームに配置します。</span><span class="sxs-lookup"><span data-stu-id="4245a-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="4245a-138">もう 1 つのオプションは **、OpenStreamOnFile** を呼び出してデータ ファイルにアクセスするストリームを作成し、このストリームの **IStream::CopyTo** メソッドを呼び出して **、OpenProperty** によって返されるストリームにデータをコピーすることです。</span><span class="sxs-lookup"><span data-stu-id="4245a-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="4245a-139">新しいストリームの **IStream::Commit メソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="4245a-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-pr_attach_data_obj"></a><span data-ttu-id="4245a-140">設定PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="4245a-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="4245a-141">**IMAPIProp::OpenProperty** を呼び出して **、IStreamDocfile** インターフェイスを使用してプロパティを開き、構造化ストレージで動作するストリームを作成します。</span><span class="sxs-lookup"><span data-stu-id="4245a-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="4245a-142">**IStreamDocfile は** メッセージ ストア プロバイダーによって実装され、クライアントに構造化ストレージを格納および取得するためのパフォーマンスの高い方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="4245a-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="4245a-143">**IStreamDocfile** インターフェイスは **IStream** と同じですが、ストリームのコンテンツは構造化ストレージとしてフォーマットされる保証があります。</span><span class="sxs-lookup"><span data-stu-id="4245a-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="4245a-144">この呼び出しが成功した場合は、ストリームの設定と同じ手順でストリームを作成 **PR_ATTACH_DATA_BIN。**</span><span class="sxs-lookup"><span data-stu-id="4245a-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="4245a-145">**OpenProperty が失敗** した場合:</span><span class="sxs-lookup"><span data-stu-id="4245a-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="4245a-146">**OpenProperty を再度呼び** 出して **IStorage を求める**。</span><span class="sxs-lookup"><span data-stu-id="4245a-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="4245a-147">**StgOpenStorage を呼び出** して OLE オブジェクトを開き、ストレージ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="4245a-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="4245a-148">返されたストレージ オブジェクトの **IStorage::CopyTo** メソッドを呼び出して **、OpenProperty** から返されたストレージ オブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="4245a-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="4245a-149">新しいストレージ オブジェクトの **IStorage::Commit メソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="4245a-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-pr_attach_pathname"></a><span data-ttu-id="4245a-150">設定PR_ATTACH_PATHNAME</span><span class="sxs-lookup"><span data-stu-id="4245a-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="4245a-151">[SPropValue](spropvalue.md)構造体を割り当て **、ulPropTag** メンバーを PR_ATTACH_PATHNAME に **、Value.LPSZ** メンバーをファイル名を表す文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="4245a-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="4245a-152">添付ファイルの [IMAPIProp::SetProps メソッドを呼び出](imapiprop-setprops.md) します。</span><span class="sxs-lookup"><span data-stu-id="4245a-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="4245a-153">プラットフォームで長いファイル名がサポートされている場合は、ファイル名とファイル名 **PR_ATTACH_PATHNAME** 設定 **PR_ATTACH_LONG_PATHNAME。**</span><span class="sxs-lookup"><span data-stu-id="4245a-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="4245a-154">短いファイル名を取得するには、オペレーティング システムの呼び出しが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="4245a-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4245a-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="4245a-155">See also</span></span>

- [<span data-ttu-id="4245a-156">MAPI 添付ファイル</span><span class="sxs-lookup"><span data-stu-id="4245a-156">MAPI Attachments</span></span>](mapi-attachments.md)

