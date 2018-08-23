---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bf100ed916080a91366062f45b9e3349516bdb98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588518"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="ac041-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="ac041-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="ac041-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac041-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac041-105">メッセージの添付ファイル テーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="ac041-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="ac041-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="ac041-106">Parameters</span></span>

 <span data-ttu-id="ac041-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac041-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ac041-108">[in]テーブルの作成に関連するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ac041-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="ac041-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ac041-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="ac041-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ac041-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ac041-111">Unicode 形式では、文字列型の列です。</span><span class="sxs-lookup"><span data-stu-id="ac041-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="ac041-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列型の列です。</span><span class="sxs-lookup"><span data-stu-id="ac041-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="ac041-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ac041-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ac041-114">正常に戻す、可能性のあるテーブルが呼び出し側のクライアントに完全に使用する前に**GetAttachmentTable**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ac041-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="ac041-115">テーブルが使用できない場合は、それ以降の呼び出しを行うとエラーが発生することができます。</span><span class="sxs-lookup"><span data-stu-id="ac041-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="ac041-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="ac041-116">_lppTable_</span></span>
  
> <span data-ttu-id="ac041-117">[out]添付ファイル テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ac041-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac041-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ac041-118">Return value</span></span>

<span data-ttu-id="ac041-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac041-119">S_OK</span></span> 
  
> <span data-ttu-id="ac041-120">添付ファイル テーブルが正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="ac041-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac041-121">注釈</span><span class="sxs-lookup"><span data-stu-id="ac041-121">Remarks</span></span>

<span data-ttu-id="ac041-122">**IMessage::GetAttachmentTable**メソッドは、メッセージ内のすべての添付ファイルに関する情報が含まれています、メッセージの添付ファイル テーブルにポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="ac041-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="ac041-123">クライアントは、添付ファイル テーブルを介してのみ添付ファイルへのアクセスを取得できます。</span><span class="sxs-lookup"><span data-stu-id="ac041-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="ac041-124">添付ファイルの数を取得することによって**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティは、クライアントが使用できる**IMessage**の方法のいくつかの添付ファイルを操作します。</span><span class="sxs-lookup"><span data-stu-id="ac041-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="ac041-125">添付ファイルごとに 1 つの行があります。</span><span class="sxs-lookup"><span data-stu-id="ac041-125">There is one row for each attachment.</span></span> <span data-ttu-id="ac041-126">添付ファイル テーブル内の列の一覧は、[添付ファイル テーブル](attachment-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac041-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="ac041-127">添付ファイル通常はテーブルに表示されない、添付ファイル[IMAPIProp::SaveChanges](imapiprop-savechanges.md)への呼び出しで、添付ファイルとメッセージの両方が保存されるまでです。</span><span class="sxs-lookup"><span data-stu-id="ac041-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="ac041-128">添付ファイル テーブルでは、動的です。</span><span class="sxs-lookup"><span data-stu-id="ac041-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="ac041-129">クライアントは新しい添付ファイルを作成、既存の添付ファイルを削除、または 1 つまたは複数のプロパティを変更したら、 **SaveChanges**の呼び出し、メッセージの添付ファイルを場合添付ファイル テーブルが新しい情報を反映するように更新されます。</span><span class="sxs-lookup"><span data-stu-id="ac041-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="ac041-130">いくつかの添付ファイル テーブルのサポートまで、さまざまな制限です。そうでないです。</span><span class="sxs-lookup"><span data-stu-id="ac041-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="ac041-131">制限のサポートは、メッセージ ストア プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="ac041-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="ac041-132">最初に開くと、添付ファイル テーブルは必ずしも並べ替えられていない特定の順序で。</span><span class="sxs-lookup"><span data-stu-id="ac041-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="ac041-133">_UlFlags_パラメーターに MAPI_UNICODE フラグを設定すると、添付ファイル テーブルに次の呼び出しが影響します。</span><span class="sxs-lookup"><span data-stu-id="ac041-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="ac041-134">列を取得する[IMAPITable::QueryColumns](imapitable-querycolumns.md)を設定します。</span><span class="sxs-lookup"><span data-stu-id="ac041-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="ac041-135">[IMAPITable::QueryRows](imapitable-queryrows.md)の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="ac041-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="ac041-136">並べ替え順序を取得するために[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)をします。</span><span class="sxs-lookup"><span data-stu-id="ac041-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="ac041-137">これらの呼び出しから返される文字列の列の情報は、Unicode 形式である Unicode フラグの要求を設定します。</span><span class="sxs-lookup"><span data-stu-id="ac041-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="ac041-138">ただし、Unicode をサポートしていないすべてのメッセージ ストア プロバイダーであるためこのフラグを設定、のみ要求です。</span><span class="sxs-lookup"><span data-stu-id="ac041-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ac041-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac041-139">See also</span></span>



[<span data-ttu-id="ac041-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="ac041-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="ac041-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="ac041-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="ac041-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="ac041-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="ac041-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ac041-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

