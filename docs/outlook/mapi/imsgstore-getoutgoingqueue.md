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
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="16ab1-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="16ab1-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="16ab1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16ab1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16ab1-105">メッセージ ストアの送信キュー内のすべてのメッセージに関する情報を含む、送信キュー テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="16ab1-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="16ab1-106">このメソッドは、MAPI スプーラーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="16ab1-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="16ab1-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="16ab1-107">Parameters</span></span>

 <span data-ttu-id="16ab1-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="16ab1-108">_ulFlags_</span></span>
  
> <span data-ttu-id="16ab1-109">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="16ab1-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="16ab1-110">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="16ab1-110">_lppTable_</span></span>
  
> <span data-ttu-id="16ab1-111">[out]送信キュー テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="16ab1-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="16ab1-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="16ab1-112">Return value</span></span>

<span data-ttu-id="16ab1-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="16ab1-113">S_OK</span></span> 
  
> <span data-ttu-id="16ab1-114">送信キュー テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="16ab1-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16ab1-115">注釈</span><span class="sxs-lookup"><span data-stu-id="16ab1-115">Remarks</span></span>

<span data-ttu-id="16ab1-116">**IMsgStore::GetOutgoingQueue** メソッドは、メッセージ ストアの送信メッセージのキューを示すテーブルへのアクセス権を MAPI スプーラーに提供します。</span><span class="sxs-lookup"><span data-stu-id="16ab1-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="16ab1-117">通常、メッセージは [IMessage::SubmitMessage](imessage-submitmessage.md) メソッドが呼び出された後に送信キュー テーブルに配置されます。</span><span class="sxs-lookup"><span data-stu-id="16ab1-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="16ab1-118">ただし、送信の順序は、トランスポート プロバイダーへの前処理と送信の順序に影響を与えるので、送信用にマークされている一部のメッセージが送信キュー テーブルにすぐに表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="16ab1-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="16ab1-119">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="16ab1-119">Notes to implementers</span></span>

<span data-ttu-id="16ab1-120">送信キュー テーブルに列として含める必要があるプロパティの一覧については、「送信キュー テーブル」 [を参照してください](outgoing-queue-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="16ab1-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="16ab1-121">MAPI スプーラーは、送信時刻の昇順でメッセージ ストアからのメッセージを受け入れするように設計されています。MAPI スプーラーは、この順序に一致するように送信キュー テーブルを並べ替えるか、既定の並べ替え順序として確立できます。</span><span class="sxs-lookup"><span data-stu-id="16ab1-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="16ab1-122">送信メッセージ キュー テーブルの通知をサポートし、キューの内容が変更された場合に MAPI スプーラーに通知を受け取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ab1-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16ab1-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="16ab1-123">See also</span></span>



[<span data-ttu-id="16ab1-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="16ab1-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="16ab1-125">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="16ab1-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

