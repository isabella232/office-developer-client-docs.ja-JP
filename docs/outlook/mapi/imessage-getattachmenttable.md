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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349274"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="d8f9c-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="d8f9c-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="d8f9c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8f9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8f9c-105">メッセージの添付ファイルテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="d8f9c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d8f9c-106">Parameters</span></span>

 <span data-ttu-id="d8f9c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d8f9c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d8f9c-108">順番テーブルの作成に関連するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="d8f9c-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="d8f9c-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d8f9c-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d8f9c-111">文字列列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="d8f9c-112">MAPI_UNICODE フラグが設定されていない場合、文字列列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="d8f9c-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d8f9c-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d8f9c-114">呼び出し元クライアントがテーブルを完全に使用できるようになる前に、 **getattachmenttable**を正常に返すことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="d8f9c-115">テーブルを使用できない場合は、その後の呼び出しを行うとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="d8f9c-116">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="d8f9c-116">_lppTable_</span></span>
  
> <span data-ttu-id="d8f9c-117">読み上げ添付ファイルテーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d8f9c-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="d8f9c-118">Return value</span></span>

<span data-ttu-id="d8f9c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d8f9c-119">S_OK</span></span> 
  
> <span data-ttu-id="d8f9c-120">添付ファイルテーブルが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8f9c-121">解説</span><span class="sxs-lookup"><span data-stu-id="d8f9c-121">Remarks</span></span>

<span data-ttu-id="d8f9c-122">**IMessage:: getattachmenttable**メソッドは、メッセージの添付ファイルテーブルへのポインターを返します。このオブジェクトには、メッセージ内のすべての添付ファイルに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="d8f9c-123">クライアントは、添付ファイルテーブルを介してのみ添付ファイルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="d8f9c-124">添付ファイルの番号を取得することにより、クライアントはいくつかの**IMessage**メソッドを使用して添付ファイルを操作することができます**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="d8f9c-125">添付ファイルごとに1つの行があります。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-125">There is one row for each attachment.</span></span> <span data-ttu-id="d8f9c-126">添付ファイルテーブルの列の完全な一覧については、「 [attachment Tables](attachment-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="d8f9c-127">添付ファイルは、通常、添付ファイルとメッセージが[imapiprop:: SaveChanges](imapiprop-savechanges.md)の呼び出しと共に保存されている限り、添付ファイルテーブルに表示されません。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="d8f9c-128">添付ファイルテーブルは動的です。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="d8f9c-129">クライアントが新しい添付ファイルを作成した場合、既存の添付ファイルを削除した場合、または1つまたは複数のプロパティを変更した場合は、メッセージの添付ファイルに対して**SaveChanges**呼び出しを行った後に、添付ファイルテーブルが更新され、新しい情報が反映されます。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="d8f9c-130">一部の添付ファイルテーブルでは、さまざまな制限がサポートしています。それ以外の場合は含まれません。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="d8f9c-131">制限のサポートは、メッセージストアプロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="d8f9c-132">最初に開かれたときには、添付ファイルテーブルが特定の順序で並べ替えられるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="d8f9c-133">_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、添付ファイルテーブルへの次の呼び出しに影響します。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="d8f9c-134">[IMAPITable:: querycolumns](imapitable-querycolumns.md)は、列セットを取得します。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="d8f9c-135">[IMAPITable:: QueryRows](imapitable-queryrows.md)が行を取得します。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="d8f9c-136">[IMAPITable:: querysortorder](imapitable-querysortorder.md)は、並べ替えの順序を取得します。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="d8f9c-137">unicode フラグを設定すると、これらの呼び出しから返される文字列列の情報は unicode 形式になります。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="d8f9c-138">ただし、すべてのメッセージストアプロバイダーが Unicode をサポートしているわけではないため、このフラグの設定は要求だけになります。</span><span class="sxs-lookup"><span data-stu-id="d8f9c-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d8f9c-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8f9c-139">See also</span></span>



[<span data-ttu-id="d8f9c-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="d8f9c-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="d8f9c-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="d8f9c-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="d8f9c-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="d8f9c-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="d8f9c-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d8f9c-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

