---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349281"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="5ecce-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="5ecce-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="5ecce-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ecce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ecce-105">メッセージの recipient テーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="5ecce-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5ecce-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5ecce-106">Parameters</span></span>

 <span data-ttu-id="5ecce-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5ecce-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5ecce-108">順番テーブルの戻り値を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5ecce-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="5ecce-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5ecce-109">The following flags can be set:</span></span>
    
<span data-ttu-id="5ecce-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5ecce-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5ecce-111">呼び出し元のクライアントがテーブルを完全に使用できるようになる前に、 **getrecipienttable**を正常に返すことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="5ecce-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="5ecce-112">テーブルを使用できない場合は、その後の呼び出しを行うとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5ecce-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="5ecce-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5ecce-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5ecce-114">文字列列は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ecce-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="5ecce-115">MAPI_UNICODE フラグが設定されていない場合、文字列列は ANSI 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ecce-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="5ecce-116">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="5ecce-116">_lppTable_</span></span>
  
> <span data-ttu-id="5ecce-117">読み上げ受信者テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5ecce-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5ecce-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="5ecce-118">Return value</span></span>

<span data-ttu-id="5ecce-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ecce-119">S_OK</span></span> 
  
> <span data-ttu-id="5ecce-120">受信者テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="5ecce-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ecce-121">解説</span><span class="sxs-lookup"><span data-stu-id="5ecce-121">Remarks</span></span>

<span data-ttu-id="5ecce-122">**IMessage:: get table**メソッドは、メッセージの受信者テーブルへのポインターを返します。これには、メッセージのすべての受信者に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5ecce-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="5ecce-123">すべての受信者に1つの行があります。</span><span class="sxs-lookup"><span data-stu-id="5ecce-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="5ecce-124">受信者テーブルは、メッセージが送信されたかどうかに応じて異なる列セットを持ちます。</span><span class="sxs-lookup"><span data-stu-id="5ecce-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="5ecce-125">受信者テーブルの列の完全な一覧については、「 [recipient Tables](recipient-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ecce-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="5ecce-126">一部の受信者テーブルでは、さまざまな制限がサポートしています。それ以外の場合は含まれません。</span><span class="sxs-lookup"><span data-stu-id="5ecce-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="5ecce-127">制限のサポートは、メッセージストアプロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="5ecce-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="5ecce-128">_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、受信者テーブルへの次の呼び出しに影響します。</span><span class="sxs-lookup"><span data-stu-id="5ecce-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="5ecce-129">[IMAPITable:: querycolumns](imapitable-querycolumns.md)は、列セットを取得します。</span><span class="sxs-lookup"><span data-stu-id="5ecce-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="5ecce-130">[IMAPITable:: QueryRows](imapitable-queryrows.md)が行を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ecce-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="5ecce-131">[IMAPITable:: querysortorder](imapitable-querysortorder.md)は、並べ替えの順序を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ecce-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="5ecce-132">unicode フラグを設定すると、これらの呼び出しから返される文字列列の情報は unicode 形式になります。</span><span class="sxs-lookup"><span data-stu-id="5ecce-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="5ecce-133">ただし、すべてのメッセージストアプロバイダーが Unicode をサポートしているわけではないため、このフラグの設定は要求だけになります。</span><span class="sxs-lookup"><span data-stu-id="5ecce-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="5ecce-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5ecce-134">Notes to callers</span></span>

<span data-ttu-id="5ecce-135">[IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドを呼び出すことによって、受信者テーブルを開いたまま変更することができます。</span><span class="sxs-lookup"><span data-stu-id="5ecce-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="5ecce-136">**modifyrecipients**受信者の追加、受信者の削除、または受信者のプロパティの変更を行います。</span><span class="sxs-lookup"><span data-stu-id="5ecce-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ecce-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ecce-137">See also</span></span>



[<span data-ttu-id="5ecce-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="5ecce-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="5ecce-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="5ecce-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="5ecce-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="5ecce-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="5ecce-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5ecce-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

