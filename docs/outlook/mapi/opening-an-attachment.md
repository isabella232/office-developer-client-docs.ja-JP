---
title: 添付ファイルを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 39da1e02622d81cd12a2d4673b827d49bf418128
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326174"
---
# <a name="opening-an-attachment"></a><span data-ttu-id="fde6a-103">添付ファイルを開く</span><span class="sxs-lookup"><span data-stu-id="fde6a-103">Opening an attachment</span></span>

<span data-ttu-id="fde6a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fde6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fde6a-105">添付ファイルを開くには、そのデータを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde6a-105">Opening an attachment involves displaying its data.</span></span> <span data-ttu-id="fde6a-106">たとえば、添付ファイルが開かれると、ファイルの内容が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fde6a-106">For example, when a file attachment is opened, the contents of the file are displayed.</span></span> <span data-ttu-id="fde6a-107">メッセージとフォルダーはエントリ識別子を使用して開かれますが、添付ファイルは、添付ファイルの番号 ( **PR_ATTACH_NUM**プロパティ) を使用して開かれます。</span><span class="sxs-lookup"><span data-stu-id="fde6a-107">Whereas messages and folders are opened using their entry identifiers, attachments are opened using their attachment numbers — **PR_ATTACH_NUM** properties.</span></span> <span data-ttu-id="fde6a-108">詳細については、「 **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-108">For more information, see **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span></span> <span data-ttu-id="fde6a-109">添付ファイルの番号は、メッセージの添付ファイルテーブルを通じて使用できます。</span><span class="sxs-lookup"><span data-stu-id="fde6a-109">Attachment numbers are available through a message's attachment table.</span></span>
  
### <a name="to-open-all-attachments-in-a-message"></a><span data-ttu-id="fde6a-110">メッセージ内のすべての添付ファイルを開くには</span><span class="sxs-lookup"><span data-stu-id="fde6a-110">To open all attachments in a message</span></span>
  
1. <span data-ttu-id="fde6a-111">メッセージの[IMessage:: getattachmenttable](imessage-getattachmenttable.md)メソッドを呼び出して、その添付ファイルテーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="fde6a-111">Call the message's [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method to access its attachment table.</span></span> 
    
2. <span data-ttu-id="fde6a-112">[hrqueryallrows](hrqueryallrows.md)を呼び出して、テーブル内のすべての行を取得します。</span><span class="sxs-lookup"><span data-stu-id="fde6a-112">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all the rows in the table.</span></span> 
    
3. <span data-ttu-id="fde6a-113">各行の場合:</span><span class="sxs-lookup"><span data-stu-id="fde6a-113">For each row:</span></span> 
    
    1. <span data-ttu-id="fde6a-114">添付ファイルを開くには、 **PR_ATTACH_NUM**列で表された添付ファイルの番号を、メッセージの**IMessage:: openattach**メソッドへの呼び出しで渡します。</span><span class="sxs-lookup"><span data-stu-id="fde6a-114">Open the attachment by passing the attachment number represented in the **PR_ATTACH_NUM** column in a call to the message's **IMessage::OpenAttach** method.</span></span> <span data-ttu-id="fde6a-115">詳細については、「 [IMessage:: openattach](imessage-openattach.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-115">For more information, see [IMessage::OpenAttach](imessage-openattach.md).</span></span> <span data-ttu-id="fde6a-116">**openattach**は、添付ファイルのプロパティへのアクセスを提供する**iattach**実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="fde6a-116">**OpenAttach** returns a pointer to an **IAttach** implementation that provides access to attachment properties.</span></span> 
        
    2. <span data-ttu-id="fde6a-117">添付ファイルの**imapiprop:: GetProps**メソッドを呼び出して、その**PR_ATTACH_METHOD**プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="fde6a-117">Call the attachment's **IMAPIProp::GetProps** method to retrieve its **PR_ATTACH_METHOD** property.</span></span> <span data-ttu-id="fde6a-118">詳細については、「 [imapiprop:: GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-118">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span></span>
        
    3. <span data-ttu-id="fde6a-119">**PR_ATTACH_METHOD**が ATTACH_BY_REF_ONLY に設定されている場合は、 **PR_ATTACH_PATHNAME**プロパティを取得するために**imapiprop:: GetProps**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fde6a-119">If **PR_ATTACH_METHOD** is set to ATTACH_BY_REF_ONLY, call **IMAPIProp::GetProps** to retrieve the **PR_ATTACH_PATHNAME** property.</span></span> <span data-ttu-id="fde6a-120">詳細については、「 **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-120">For more information, see **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span></span>
        
    4. <span data-ttu-id="fde6a-121">**pr\_ATTACH_METHOD**が BY_VALUE を接続\_するように設定されている場合は、 **imapiprop:: openproperty**を呼び出して、 **IStream**インターフェイスで**PR\_ATTACH_DATA_BIN**プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="fde6a-121">If **PR\_ATTACH_METHOD** is set to ATTACH\_BY_VALUE, call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_BIN** property with the **IStream** interface.</span></span> <span data-ttu-id="fde6a-122">この手順の次のサンプルコードを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-122">See the sample code following this procedure.</span></span> <span data-ttu-id="fde6a-123">詳細については、「 [imapiprop:: openproperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-123">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span>
        
    5. <span data-ttu-id="fde6a-124">**PR_ATTACH_METHOD**が ATTACH_OLE に設定されていて、添付ファイルが OLE 2 オブジェクトの場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="fde6a-124">If **PR_ATTACH_METHOD** is set to ATTACH_OLE and the attachment is an OLE 2 object:</span></span> 
        
        1. <span data-ttu-id="fde6a-125">**IStreamDocfile**インターフェイスを使用して**PR\_ATTACH_DATA_OBJ**プロパティを開くには、 **imapiprop:: openproperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fde6a-125">Call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_OBJ** property with the **IStreamDocfile** interface.</span></span> <span data-ttu-id="fde6a-126">このインターフェイスは、少なくともオーバーヘッドが少ない構造化ストレージで機能することが保証される**IStream**の実装であるため、使用してみてください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-126">Attempt to use this interface because it is an implementation of **IStream** guaranteed to work with structured storage with the least amount of overhead.</span></span> <span data-ttu-id="fde6a-127">詳細については、「 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-127">For more information, see **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span></span>
            
        2. <span data-ttu-id="fde6a-128">**openproperty**呼び出しが失敗した場合は、 **IStreamDocfile**インターフェイスを使用して**PR_ATTACH_DATA_BIN**プロパティを取得するために、もう一度呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fde6a-128">If the **OpenProperty** call fails, call it again to retrieve the **PR_ATTACH_DATA_BIN** property with the **IStreamDocfile** interface.</span></span> 
            
        3. <span data-ttu-id="fde6a-129">この2番目の**openproperty**呼び出しが失敗した場合は、 **openproperty**を呼び出して**PR_ATTACH_DATA_OBJ**を取得してください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-129">If this second **OpenProperty** call fails, try again to call **OpenProperty** to retrieve **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="fde6a-130">ただし、 **IStreamDocfile**を指定するのではなく、 **IStorage**インターフェイスを指定します。</span><span class="sxs-lookup"><span data-stu-id="fde6a-130">However, rather than specifying **IStreamDocfile**, specify the **IStorage** interface.</span></span> 
    
4. <span data-ttu-id="fde6a-131">**PR_ATTACH_METHOD**が ATTACH_EMBEDDED_MSG に設定されている場合は、 **PR_ATTACH_DATA_OBJ**の値がエラーを含むことが珍しくありません。</span><span class="sxs-lookup"><span data-stu-id="fde6a-131">If **PR_ATTACH_METHOD** is set to ATTACH_EMBEDDED_MSG, it is not unusual for the value of **PR_ATTACH_DATA_OBJ** to contain an error.</span></span> <span data-ttu-id="fde6a-132">これは、ユーザーとテーブルの実装者が、返すオブジェクトの種類について合意することができないためです。</span><span class="sxs-lookup"><span data-stu-id="fde6a-132">This is because you and the table implementer have no way to agree on the type of object to return.</span></span> <span data-ttu-id="fde6a-133">添付されたメッセージへのポインターを取得するには、 **IMessage:: openattach**を使用して添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="fde6a-133">To retrieve a pointer to the attached message, open the attachment using **IMessage::OpenAttach**.</span></span> <span data-ttu-id="fde6a-134">その後、 **imapiprop:: openproperty**メソッドを呼び出して、添付ファイルデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="fde6a-134">Then access the attachment data by calling its **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="fde6a-135">詳細については、「 [IMessage:: openattach](imessage-openattach.md) and [imapiprop:: openattach](imapiprop-openproperty.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-135">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="fde6a-136">読み取り/書き込みモードまたは読み取り専用モードで添付ファイルを開くように要求することができます。</span><span class="sxs-lookup"><span data-stu-id="fde6a-136">You can request that an attachment is opened in read/write or read-only mode.</span></span> <span data-ttu-id="fde6a-137">読み取り専用は既定のモードで、多くのメッセージストアプロバイダーは、要求されたクライアントに関係なく、すべての添付ファイルをこのモードで開きます。</span><span class="sxs-lookup"><span data-stu-id="fde6a-137">Read-only is the default mode, and many message store providers open all attachments in this mode regardless of what clients request.</span></span> <span data-ttu-id="fde6a-138">MAPI_BEST_ACCESS フラグを渡して、メッセージストアプロバイダーが最高レベルのアクセス権を付与することを要求し、開いている添付ファイルの**PR_ACCESS_LEVEL**プロパティを取得して、実際に付与されているアクセスレベルを判断します。</span><span class="sxs-lookup"><span data-stu-id="fde6a-138">Pass the MAPI_BEST_ACCESS flag to request that the message store provider grant the highest level of access it can and then retrieve the open attachment's **PR_ACCESS_LEVEL** property to determine the level of access that was actually granted.</span></span> <span data-ttu-id="fde6a-139">詳細については、「 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-139">For more information, see **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span></span>
  
<span data-ttu-id="fde6a-140">次の例は、添付ファイルの**PR\_ATTACH_DATA_BIN**プロパティでデータを開く方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fde6a-140">The following example shows how to open the data in an attachment's **PR\_ATTACH_DATA_BIN** property.</span></span> <span data-ttu-id="fde6a-141">2つのストリームにポインターを割り当てます。1つはファイル用、もう1つは添付ファイル用です。</span><span class="sxs-lookup"><span data-stu-id="fde6a-141">It allocates pointers to two streams: one for the file and one for the attachment.</span></span> <span data-ttu-id="fde6a-142">**openstreamonfile**関数は、ファイルストリームを読み取り専用モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="fde6a-142">The **OpenStreamOnFile** function opens the file stream in read-only mode.</span></span> <span data-ttu-id="fde6a-143">添付ファイルの**imapiprop:: openproperty**メソッドを呼び出すと、添付ファイルストリームが読み取り/書き込みモードで開きます。</span><span class="sxs-lookup"><span data-stu-id="fde6a-143">The call to the attachment's **IMAPIProp::OpenProperty** method opens the attachment stream in read/write mode.</span></span> <span data-ttu-id="fde6a-144">詳細については、「 **PR_ATTACH_DATA_BIN**」、「 [openstreamonfile](openstreamonfile.md)」、および「 [imapiprop:: openproperty](imapiprop-openproperty.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fde6a-144">For more information, see **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md), and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="fde6a-145">その後、コードはファイルストリームから添付ファイルストリームにコピーし、両方のストリームを解放します。</span><span class="sxs-lookup"><span data-stu-id="fde6a-145">The code then copies from the file stream to the attachment stream and releases both streams.</span></span>
  
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


