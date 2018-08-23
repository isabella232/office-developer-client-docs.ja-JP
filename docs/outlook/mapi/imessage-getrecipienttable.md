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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5908069f5fa887fd9d2e3f8c0df75f2e3d69515c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579537"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="9e3dd-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="9e3dd-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="9e3dd-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e3dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e3dd-105">メッセージの受信者テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="9e3dd-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="9e3dd-106">Parameters</span></span>

 <span data-ttu-id="9e3dd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e3dd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9e3dd-108">[in]テーブルの戻り値を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="9e3dd-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-109">The following flags can be set:</span></span>
    
<span data-ttu-id="9e3dd-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9e3dd-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9e3dd-111">正常に戻す、可能性のあるテーブルが呼び出し側のクライアントに完全に使用する前に**GetRecipientTable**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="9e3dd-112">テーブルが使用できない場合は、それ以降の呼び出しを行うとエラーが発生することができます。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="9e3dd-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e3dd-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9e3dd-114">文字列型の列は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="9e3dd-115">MAPI_UNICODE フラグが設定されていない場合、ANSI 形式の文字列の列を引き起こすことがあります。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="9e3dd-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="9e3dd-116">_lppTable_</span></span>
  
> <span data-ttu-id="9e3dd-117">[out]受信者テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e3dd-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9e3dd-118">Return value</span></span>

<span data-ttu-id="9e3dd-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e3dd-119">S_OK</span></span> 
  
> <span data-ttu-id="9e3dd-120">受信者テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9e3dd-121">注釈</span><span class="sxs-lookup"><span data-stu-id="9e3dd-121">Remarks</span></span>

<span data-ttu-id="9e3dd-122">**IMessage::GetRecipientTable**メソッドは、すべてのメッセージの受信者に関する情報を含むメッセージの受信者テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="9e3dd-123">すべての受信者の 1 つの行があります。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="9e3dd-124">受信者テーブルには、メッセージが送信されたかどうかに応じて、設定の異なる列があります。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="9e3dd-125">受信者テーブルの各列の一覧は、[受信者テーブル](recipient-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="9e3dd-126">いくつかの受信者テーブルのサポートまで、さまざまな制限です。そうでないです。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="9e3dd-127">制限のサポートは、メッセージ ストア プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="9e3dd-128">_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する受信者テーブルには、次の呼び出しに影響します。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="9e3dd-129">列を取得する[IMAPITable::QueryColumns](imapitable-querycolumns.md)を設定します。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="9e3dd-130">[IMAPITable::QueryRows](imapitable-queryrows.md)の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="9e3dd-131">並べ替え順序を取得するために[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)をします。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="9e3dd-132">これらの呼び出しから返される文字列の列の情報は、Unicode 形式である Unicode フラグの要求を設定します。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="9e3dd-133">ただし、Unicode をサポートしていないすべてのメッセージ ストア プロバイダーであるためこのフラグを設定、のみ要求です。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9e3dd-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9e3dd-134">Notes to callers</span></span>

<span data-ttu-id="9e3dd-135">受信者テーブルが開いている間、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを呼び出すことによって変更できます。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="9e3dd-136">**ModifyRecipients**の受信者を追加するには、受信者を削除または受信者のプロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="9e3dd-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e3dd-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e3dd-137">See also</span></span>



[<span data-ttu-id="9e3dd-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9e3dd-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="9e3dd-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="9e3dd-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="9e3dd-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="9e3dd-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="9e3dd-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9e3dd-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

