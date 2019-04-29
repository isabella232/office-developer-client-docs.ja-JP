---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8ccb732dd587b2e5107290b2db7c48e85d0145d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434152"
---
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="20b3c-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="20b3c-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="20b3c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20b3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20b3c-105">送信キューテーブル (メッセージストアの送信キューにあるすべてのメッセージに関する情報を含むテーブル) へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="20b3c-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="20b3c-106">このメソッドは、MAPI スプーラーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20b3c-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="20b3c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20b3c-107">Parameters</span></span>

 <span data-ttu-id="20b3c-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20b3c-108">_ulFlags_</span></span>
  
> <span data-ttu-id="20b3c-109">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="20b3c-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="20b3c-110">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="20b3c-110">_lppTable_</span></span>
  
> <span data-ttu-id="20b3c-111">読み上げ送信キューテーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="20b3c-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="20b3c-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="20b3c-112">Return value</span></span>

<span data-ttu-id="20b3c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="20b3c-113">S_OK</span></span> 
  
> <span data-ttu-id="20b3c-114">送信キューテーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="20b3c-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20b3c-115">注釈</span><span class="sxs-lookup"><span data-stu-id="20b3c-115">Remarks</span></span>

<span data-ttu-id="20b3c-116">**IMsgStore:: getoutgoingqueue**メソッドは、メッセージストアの送信メッセージのキューを示すテーブルへのアクセス権を MAPI スプーラーに提供します。</span><span class="sxs-lookup"><span data-stu-id="20b3c-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="20b3c-117">通常、メッセージは[IMessage:: submitmessage](imessage-submitmessage.md)メソッドが呼び出された後に、送信キューテーブルに配置されます。</span><span class="sxs-lookup"><span data-stu-id="20b3c-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="20b3c-118">ただし、送信の順序は、トランスポートプロバイダーへの前処理と送信の順序に影響するため、送信用にマークされているメッセージの一部は、すぐに送信キューテーブルに表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="20b3c-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="20b3c-119">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="20b3c-119">Notes to implementers</span></span>

<span data-ttu-id="20b3c-120">送信キューテーブルに列として含める必要があるプロパティの一覧については、「[送信キューテーブル](outgoing-queue-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20b3c-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="20b3c-121">mapi スプーラーは、送信時間の昇順でメッセージストアからのメッセージを受信するように設計されているため、mapi スプーラーで送信キューテーブルを並べ替えて、この順序に一致するようにするか、または既定の並べ替え順序として設定することができます。</span><span class="sxs-lookup"><span data-stu-id="20b3c-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="20b3c-122">キューの内容が変更されたときに MAPI スプーラーに通知されるように、送信メッセージキューテーブルの通知をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="20b3c-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20b3c-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="20b3c-123">See also</span></span>



[<span data-ttu-id="20b3c-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="20b3c-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="20b3c-125">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="20b3c-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

