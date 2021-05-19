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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421173"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="d7d46-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="d7d46-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="d7d46-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7d46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7d46-105">メッセージの添付ファイル テーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="d7d46-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="d7d46-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d7d46-106">Parameters</span></span>

 <span data-ttu-id="d7d46-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7d46-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d7d46-108">[in]テーブルの作成に関連するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d7d46-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="d7d46-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d7d46-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="d7d46-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d7d46-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d7d46-111">文字列列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="d7d46-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="d7d46-112">このフラグMAPI_UNICODE設定されていない場合、文字列列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="d7d46-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="d7d46-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d7d46-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d7d46-114">**GetAttachmentTable は、** 呼び出し元のクライアントがテーブルを完全に利用できる前に、正常に返す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d7d46-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="d7d46-115">テーブルが使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d7d46-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="d7d46-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="d7d46-116">_lppTable_</span></span>
  
> <span data-ttu-id="d7d46-117">[out]添付ファイル テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d7d46-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7d46-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="d7d46-118">Return value</span></span>

<span data-ttu-id="d7d46-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7d46-119">S_OK</span></span> 
  
> <span data-ttu-id="d7d46-120">添付ファイル テーブルが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="d7d46-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7d46-121">注釈</span><span class="sxs-lookup"><span data-stu-id="d7d46-121">Remarks</span></span>

<span data-ttu-id="d7d46-122">**IMessage::GetAttachmentTable** メソッドは、メッセージ内のすべての添付ファイルに関する情報を含む、メッセージの添付ファイル テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="d7d46-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="d7d46-123">クライアントは、添付ファイル テーブルを通じてのみ添付ファイルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d7d46-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="d7d46-124">添付ファイルの番号をPR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティを取得すると、クライアントはいくつかの **IMessage** メソッドを使用して添付ファイルを処理できます。</span><span class="sxs-lookup"><span data-stu-id="d7d46-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="d7d46-125">添付ファイルごとに 1 行があります。</span><span class="sxs-lookup"><span data-stu-id="d7d46-125">There is one row for each attachment.</span></span> <span data-ttu-id="d7d46-126">添付ファイル テーブル内の列の完全な一覧については、「添付ファイル テーブル」 [を参照してください](attachment-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="d7d46-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="d7d46-127">添付ファイルは、通常 [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)への呼び出しで添付ファイルとメッセージの両方が保存されるまで、添付ファイルテーブルに表示されません。</span><span class="sxs-lookup"><span data-stu-id="d7d46-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="d7d46-128">添付ファイル テーブルは動的です。</span><span class="sxs-lookup"><span data-stu-id="d7d46-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="d7d46-129">クライアントが新しい添付ファイルを作成したり、既存の添付ファイルを削除したり、メッセージの添付ファイルで **SaveChanges** 呼び出しが行われたら、1 つ以上のプロパティを変更すると、新しい情報を反映するように添付ファイル テーブルが更新されます。</span><span class="sxs-lookup"><span data-stu-id="d7d46-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="d7d46-130">一部の添付ファイル テーブルでは、さまざまな制限がサポートされています。他のユーザーはそうではありません。</span><span class="sxs-lookup"><span data-stu-id="d7d46-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="d7d46-131">制限のサポートは、メッセージ ストア プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d7d46-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="d7d46-132">最初に開いた場合、添付ファイル テーブルは必ずしも特定の順序で並べ替えされません。</span><span class="sxs-lookup"><span data-stu-id="d7d46-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="d7d46-133">_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると、添付ファイル テーブルへの次の呼び出しに影響します。</span><span class="sxs-lookup"><span data-stu-id="d7d46-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="d7d46-134">[列セットを取得する IMAPITable::QueryColumns。](imapitable-querycolumns.md)</span><span class="sxs-lookup"><span data-stu-id="d7d46-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="d7d46-135">[IMAPITable::QueryRows を使用して行](imapitable-queryrows.md) を取得します。</span><span class="sxs-lookup"><span data-stu-id="d7d46-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="d7d46-136">[並べ替え順序を取得する IMAPITable::QuerySortOrder。](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="d7d46-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="d7d46-137">Unicode フラグを設定すると、これらの呼び出しから返される文字列列の情報を Unicode 形式で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7d46-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="d7d46-138">ただし、すべてのメッセージ ストア プロバイダーが Unicode をサポートしているわけではありませんので、このフラグの設定は要求のみです。</span><span class="sxs-lookup"><span data-stu-id="d7d46-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7d46-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7d46-139">See also</span></span>



[<span data-ttu-id="d7d46-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="d7d46-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="d7d46-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="d7d46-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="d7d46-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="d7d46-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="d7d46-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d7d46-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

