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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1b59071758aad9c71939eb9efc029005806b2a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801009"
---
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="fbf14-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="fbf14-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="fbf14-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fbf14-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fbf14-105">発信キュー テーブル、メッセージ ストアの送信キュー内のすべてのメッセージに関する情報が含まれているテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="fbf14-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="fbf14-106">このメソッドは、MAPI スプーラーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fbf14-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="fbf14-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="fbf14-107">Parameters</span></span>

 <span data-ttu-id="fbf14-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fbf14-108">_ulFlags_</span></span>
  
> <span data-ttu-id="fbf14-109">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="fbf14-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="fbf14-110">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="fbf14-110">_lppTable_</span></span>
  
> <span data-ttu-id="fbf14-111">[out]発信キュー テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fbf14-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fbf14-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fbf14-112">Return value</span></span>

<span data-ttu-id="fbf14-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="fbf14-113">S_OK</span></span> 
  
> <span data-ttu-id="fbf14-114">発信キューのテーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="fbf14-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fbf14-115">備考</span><span class="sxs-lookup"><span data-stu-id="fbf14-115">Remarks</span></span>

<span data-ttu-id="fbf14-116">**IMsgStore::GetOutgoingQueue**メソッドでは、MAPI スプーラーに送信メッセージのメッセージ ストアのキューを表示するテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="fbf14-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="fbf14-117">通常、メッセージは、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドが呼び出された後、発信キュー テーブルに配置されます。</span><span class="sxs-lookup"><span data-stu-id="fbf14-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="fbf14-118">ただし、提出書類の順序は、前処理およびトランスポート プロバイダーへの送信の順序に影響するためいくつかのメッセージを送信するためにマークされている可能性がありますテーブルに表示されない、送信キューすぐにします。</span><span class="sxs-lookup"><span data-stu-id="fbf14-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fbf14-119">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="fbf14-119">Notes to implementers</span></span>

<span data-ttu-id="fbf14-120">発信キュー テーブル内の列として含める必要があるプロパティの一覧では、[送信キューのテーブル](outgoing-queue-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fbf14-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="fbf14-121">MAPI スプーラーが送信時の順序を昇順でのメッセージ ストアからメッセージを受け付けるように設計されているためか、この順序と一致または既定の並べ替え順序として設定する発信キュー テーブルを並べ替えるには、MAPI スプーラーを許可します。</span><span class="sxs-lookup"><span data-stu-id="fbf14-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="fbf14-122">通知を送信メッセージ キュー テーブルのサポート キューの内容を変更すると、MAPI スプーラーに通知することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbf14-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fbf14-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="fbf14-123">See also</span></span>



[<span data-ttu-id="fbf14-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="fbf14-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="fbf14-125">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fbf14-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

