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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424610"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="e9928-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="e9928-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="e9928-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9928-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9928-105">メッセージの受信者テーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="e9928-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="e9928-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9928-106">Parameters</span></span>

 <span data-ttu-id="e9928-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e9928-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e9928-108">[in]テーブルの戻り値を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e9928-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="e9928-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e9928-109">The following flags can be set:</span></span>
    
<span data-ttu-id="e9928-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e9928-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e9928-111">**テーブルが呼び出** し元のクライアントで完全に使用できる前に、GetRecipientTable が正常に返されるのを許可します。</span><span class="sxs-lookup"><span data-stu-id="e9928-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="e9928-112">テーブルが使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e9928-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="e9928-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e9928-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e9928-114">文字列列は Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9928-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="e9928-115">このフラグMAPI_UNICODE設定しない場合、文字列列は ANSI 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9928-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="e9928-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="e9928-116">_lppTable_</span></span>
  
> <span data-ttu-id="e9928-117">[out]受信者テーブルへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="e9928-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e9928-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9928-118">Return value</span></span>

<span data-ttu-id="e9928-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9928-119">S_OK</span></span> 
  
> <span data-ttu-id="e9928-120">受信者テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="e9928-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9928-121">注釈</span><span class="sxs-lookup"><span data-stu-id="e9928-121">Remarks</span></span>

<span data-ttu-id="e9928-122">**IMessage::GetRecipientTable** メソッドは、メッセージのすべての受信者に関する情報を含む、メッセージの受信者テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="e9928-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="e9928-123">受信者ごとに 1 行があります。</span><span class="sxs-lookup"><span data-stu-id="e9928-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="e9928-124">受信者テーブルの列セットは、メッセージが送信されたかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e9928-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="e9928-125">受信者テーブル内の列の完全な一覧については、「受信者テーブル」 [を参照してください](recipient-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="e9928-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="e9928-126">一部の受信者テーブルでは、さまざまな制限がサポートされています。他のユーザーはそうではありません。</span><span class="sxs-lookup"><span data-stu-id="e9928-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="e9928-127">制限のサポートは、メッセージ ストア プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e9928-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="e9928-128">_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると、受信者テーブルへの次の呼び出しに影響します。</span><span class="sxs-lookup"><span data-stu-id="e9928-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="e9928-129">[列セットを取得する IMAPITable::QueryColumns。](imapitable-querycolumns.md)</span><span class="sxs-lookup"><span data-stu-id="e9928-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="e9928-130">[IMAPITable::QueryRows を使用して行](imapitable-queryrows.md) を取得します。</span><span class="sxs-lookup"><span data-stu-id="e9928-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="e9928-131">[並べ替え順序を取得する IMAPITable::QuerySortOrder。](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="e9928-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="e9928-132">Unicode フラグを設定すると、これらの呼び出しから返される文字列列の情報を Unicode 形式で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9928-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="e9928-133">ただし、すべてのメッセージ ストア プロバイダーが Unicode をサポートしているわけではありませんので、このフラグの設定は要求のみです。</span><span class="sxs-lookup"><span data-stu-id="e9928-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e9928-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e9928-134">Notes to callers</span></span>

<span data-ttu-id="e9928-135">[IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを呼び出すことによって、受信者テーブルを開いている間に変更できます。</span><span class="sxs-lookup"><span data-stu-id="e9928-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="e9928-136">**ModifyRecipients は** 、受信者の追加、受信者の削除、または受信者のプロパティの変更を行います。</span><span class="sxs-lookup"><span data-stu-id="e9928-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9928-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9928-137">See also</span></span>



[<span data-ttu-id="e9928-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="e9928-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="e9928-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e9928-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="e9928-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="e9928-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="e9928-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e9928-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

