---
title: 添付ファイルを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3875e51868e882ca454c06949347327a21a93eb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801678"
---
# <a name="opening-an-attachment"></a><span data-ttu-id="9ef06-103">添付ファイルを開く</span><span class="sxs-lookup"><span data-stu-id="9ef06-103">Opening an attachment</span></span>

<span data-ttu-id="9ef06-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ef06-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ef06-105">添付ファイルを開くには、そのデータを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ef06-105">Opening an attachment involves displaying its data.</span></span> <span data-ttu-id="9ef06-106">たとえば、添付ファイルを開くと、ファイルの内容が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ef06-106">For example, when a file attachment is opened, the contents of the file are displayed.</span></span> <span data-ttu-id="9ef06-107">その添付ファイルの番号を使用して添付ファイルを開くが、メッセージとフォルダーを開くと、エントリの識別子を使用して、- **PR_ATTACH_NUM**のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="9ef06-107">Whereas messages and folders are opened using their entry identifiers, attachments are opened using their attachment numbers — **PR_ATTACH_NUM** properties.</span></span> <span data-ttu-id="9ef06-108">詳細については、 **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ef06-108">For more information, see **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span></span> <span data-ttu-id="9ef06-109">添付ファイル番号は、メッセージの添付ファイル テーブルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9ef06-109">Attachment numbers are available through a message's attachment table.</span></span>
  
### <a name="to-open-all-attachments-in-a-message"></a><span data-ttu-id="9ef06-110">メッセージですべての添付ファイルを開く</span><span class="sxs-lookup"><span data-stu-id="9ef06-110">To open all attachments in a message</span></span>
  
1. <span data-ttu-id="9ef06-111">その添付ファイル テーブルにアクセスするためのメッセージの[IMessage::GetAttachmentTable](imessage-getattachmenttable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9ef06-111">Call the message's [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method to access its attachment table.</span></span> 
    
2. <span data-ttu-id="9ef06-112">テーブル内のすべての行を取得するために[HrQueryAllRows](hrqueryallrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9ef06-112">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all the rows in the table.</span></span> 
    
3. <span data-ttu-id="9ef06-113">行ごと。</span><span class="sxs-lookup"><span data-stu-id="9ef06-113">For each row:</span></span> 
    
    1. <span data-ttu-id="9ef06-114">メッセージの**IMessage::OpenAttach**メソッドの呼び出しで [ **PR_ATTACH_NUM** ] 列で表される添付ファイルの数を渡すことによって、添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="9ef06-114">Open the attachment by passing the attachment number represented in the **PR_ATTACH_NUM** column in a call to the message's **IMessage::OpenAttach** method.</span></span> <span data-ttu-id="9ef06-115">詳細については、 [IMessage::OpenAttach](imessage-openattach.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ef06-115">For more information, see [IMessage::OpenAttach](imessage-openattach.md).</span></span> <span data-ttu-id="9ef06-116">**OpenAttach**は、添付ファイルのプロパティへのアクセスを提供する**IAttach**の実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9ef06-116">**OpenAttach** returns a pointer to an **IAttach** implementation that provides access to attachment properties.</span></span> 
        
    2. <span data-ttu-id="9ef06-117">その**PR_ATTACH_METHOD**プロパティを取得するために、添付ファイルの**IMAPIProp::GetProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9ef06-117">Call the attachment's **IMAPIProp::GetProps** method to retrieve its **PR_ATTACH_METHOD** property.</span></span> <span data-ttu-id="9ef06-118">詳細については、 [IMAPIProp::GetProps](imapiprop-getprops.md)と**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ef06-118">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span></span>
        
    3. <span data-ttu-id="9ef06-119">**PR_ATTACH_METHOD**は、ATTACH_BY_REF_ONLY に設定されている場合は、 **PR_ATTACH_PATHNAME**プロパティを取得するために**IMAPIProp::GetProps**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9ef06-119">If **PR_ATTACH_METHOD** is set to ATTACH_BY_REF_ONLY, call **IMAPIProp::GetProps** to retrieve the **PR_ATTACH_PATHNAME** property.</span></span> <span data-ttu-id="9ef06-120">詳細については、 **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ef06-120">For more information, see **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span></span>
        
    4. <span data-ttu-id="9ef06-121">場合**PR\_ATTACH_METHOD**アタッチに設定されて\_BY_VALUE を開くには**IMAPIProp::OpenProperty**を呼び出し、 **PR\_ATTACH_DATA_BIN** **IStream**インターフェイスを使用してプロパティです。</span><span class="sxs-lookup"><span data-stu-id="9ef06-121">If **PR\_ATTACH_METHOD** is set to ATTACH\_BY_VALUE, call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_BIN** property with the **IStream** interface.</span></span> <span data-ttu-id="9ef06-122">この手順を次のサンプル コードを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ef06-122">See the sample code following this procedure.</span></span> <span data-ttu-id="9ef06-123">詳細については、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)と**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ef06-123">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span>
        
    5. <span data-ttu-id="9ef06-124">**PR_ATTACH_METHOD**は、ATTACH_OLE と、添付ファイルに設定されている場合は、OLE 2 オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="9ef06-124">If **PR_ATTACH_METHOD** is set to ATTACH_OLE and the attachment is an OLE 2 object:</span></span> 
        
        1. <span data-ttu-id="9ef06-125">開くには**IMAPIProp::OpenProperty**を呼び出し、 **PR\_ATTACH_DATA_OBJ** **IStreamDocfile**インタ フェースを持つプロパティです。</span><span class="sxs-lookup"><span data-stu-id="9ef06-125">Call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_OBJ** property with the **IStreamDocfile** interface.</span></span> <span data-ttu-id="9ef06-126">**IStream**を最小限のオーバーヘッドでの構造化ストレージの実装であるために、このインターフェイスを使用しようとしてください。</span><span class="sxs-lookup"><span data-stu-id="9ef06-126">Attempt to use this interface because it is an implementation of **IStream** guaranteed to work with structured storage with the least amount of overhead.</span></span> <span data-ttu-id="9ef06-127">詳細については、 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ef06-127">For more information, see **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span></span>
            
        2. <span data-ttu-id="9ef06-128">**OpenProperty**呼び出しが失敗した場合は、 **IStreamDocfile**インタ フェースを持つ**PR_ATTACH_DATA_BIN**プロパティを取得するには、もう一度を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9ef06-128">If the **OpenProperty** call fails, call it again to retrieve the **PR_ATTACH_DATA_BIN** property with the **IStreamDocfile** interface.</span></span> 
            
        3. <span data-ttu-id="9ef06-129">この 2 番目の**OpenProperty**呼び出しが失敗した場合、もう一度**PR_ATTACH_DATA_OBJ**を取得するために**OpenProperty**をコールします。</span><span class="sxs-lookup"><span data-stu-id="9ef06-129">If this second **OpenProperty** call fails, try again to call **OpenProperty** to retrieve **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="9ef06-130">ただし、 **IStreamDocfile**を指定するのではなく、 **IStorage**インターフェイスを指定します。</span><span class="sxs-lookup"><span data-stu-id="9ef06-130">However, rather than specifying **IStreamDocfile**, specify the **IStorage** interface.</span></span> 
    
4. <span data-ttu-id="9ef06-131">**PR_ATTACH_METHOD**は、ATTACH_EMBEDDED_MSG に設定されている場合は、エラーを格納する**PR_ATTACH_DATA_OBJ**の値の異常なことはできません。</span><span class="sxs-lookup"><span data-stu-id="9ef06-131">If **PR_ATTACH_METHOD** is set to ATTACH_EMBEDDED_MSG, it is not unusual for the value of **PR_ATTACH_DATA_OBJ** to contain an error.</span></span> <span data-ttu-id="9ef06-132">テーブルの作成者とすることはありませんを返すオブジェクトの型が一致するためです。</span><span class="sxs-lookup"><span data-stu-id="9ef06-132">This is because you and the table implementer have no way to agree on the type of object to return.</span></span> <span data-ttu-id="9ef06-133">添付されたメッセージへのポインターを取得するには、 **IMessage::OpenAttach**を使用して添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="9ef06-133">To retrieve a pointer to the attached message, open the attachment using **IMessage::OpenAttach**.</span></span> <span data-ttu-id="9ef06-134">その**IMAPIProp::OpenProperty**メソッドを呼び出すことによって添付ファイルのデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="9ef06-134">Then access the attachment data by calling its **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="9ef06-135">詳細については、 [IMessage::OpenAttach](imessage-openattach.md)および[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ef06-135">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="9ef06-136">添付ファイルが読み取り/書き込みまたは読み取り専用モードで開かれているを要求することができます。</span><span class="sxs-lookup"><span data-stu-id="9ef06-136">You can request that an attachment is opened in read/write or read-only mode.</span></span> <span data-ttu-id="9ef06-137">読み取り専用では、既定のモード、およびメッセージ ストア プロバイダーの多くは、クライアントの要求に関係なく、このモードですべての添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="9ef06-137">Read-only is the default mode, and many message store providers open all attachments in this mode regardless of what clients request.</span></span> <span data-ttu-id="9ef06-138">メッセージ ストア プロバイダーが最高レベルのアクセスが与えられているアクセス権のレベルを決定するのには、開いている添付ファイルの**PR_ACCESS_LEVEL**プロパティを取得し、そのことができますを与えることを要求するのには MAPI_BEST_ACCESS フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="9ef06-138">Pass the MAPI_BEST_ACCESS flag to request that the message store provider grant the highest level of access it can and then retrieve the open attachment's **PR_ACCESS_LEVEL** property to determine the level of access that was actually granted.</span></span> <span data-ttu-id="9ef06-139">詳細については、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ef06-139">For more information, see **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span></span>
  
<span data-ttu-id="9ef06-140">次の例では、添付ファイルのデータを開く方法を示しています**PR\_ATTACH_DATA_BIN**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="9ef06-140">The following example shows how to open the data in an attachment's **PR\_ATTACH_DATA_BIN** property.</span></span> <span data-ttu-id="9ef06-141">2 つのストリームへのポインターが割り当てられます。 ファイルと添付ファイルのいずれかのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="9ef06-141">It allocates pointers to two streams: one for the file and one for the attachment.</span></span> <span data-ttu-id="9ef06-142">**OpenStreamOnFile**関数では、ファイル ストリームが読み取り専用モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="9ef06-142">The **OpenStreamOnFile** function opens the file stream in read-only mode.</span></span> <span data-ttu-id="9ef06-143">添付ファイルの**IMAPIProp::OpenProperty**メソッドを呼び出すには、読み取り/書き込みモードで添付ファイルのストリームを開きます。</span><span class="sxs-lookup"><span data-stu-id="9ef06-143">The call to the attachment's **IMAPIProp::OpenProperty** method opens the attachment stream in read/write mode.</span></span> <span data-ttu-id="9ef06-144">詳細については、 **PR_ATTACH_DATA_BIN**、 [OpenStreamOnFile](openstreamonfile.md)、および[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ef06-144">For more information, see **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md), and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="9ef06-145">コードは、ファイル ストリームから添付ファイルのストリームにコピーし、両方のストリームを解放します。</span><span class="sxs-lookup"><span data-stu-id="9ef06-145">The code then copies from the file stream to the attachment stream and releases both streams.</span></span>
  
```cpp
LPSTREAM pStreamFile, pStreamAtt;
HRESULT hr;
hr = OpenStreamOnFile (MAPIAllocateBuffer, MAPIFreeBuffer,
                       STGM_READ, "myfile.doc", NULL, &pStreamFile);
if (HR_SUCCEEDED(hr))
{
    // Open the destination stream in the attachment object
    hr = pAttach->OpenProperty (PR_ATTACH_DATA_BIN,
                                &IID_IStream,
                                0,
                                MAPI_MODIFY | MAPI_CREATE,
                                (LPUNKNOWN *)&pStreamAtt);
    if (HR_SUCCEEDED(hr))
    {
        STATSTG StatInfo;
        pStreamFile->Stat (&StatInfo, STATFLAG_NONAME);
        hResult = pStreamFile->CopyTo (pStreamAtt, StatInfo.cbSize,
                                       NULL, NULL);
        pStreamAtt->Release();
    }
    pStreamFile->Release();
}
```


