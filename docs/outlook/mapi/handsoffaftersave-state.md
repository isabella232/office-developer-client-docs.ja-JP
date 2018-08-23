---
title: HandsOffAfterSave 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 274e7206171e1874e3625896952f861d25f3b382
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564536"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="cf2f0-103">HandsOffAfterSave 状態</span><span class="sxs-lookup"><span data-stu-id="cf2f0-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="cf2f0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf2f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf2f0-105">HandsOffAfterSave の状態は、恒久的に保存するフォームの内容を保存するプロセスの一部です。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="cf2f0-106">この状態のときにフォーム オブジェクト避ける必要がある、メモリ内のコピー、メッセージのプロパティの値を変更するため、別の機会をこれらの変更を保存することができません。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="cf2f0-107">次の表では、HandsOffAfterSave の状態から有効な遷移について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="cf2f0-108">**IPersistMessage メソッド**</span><span class="sxs-lookup"><span data-stu-id="cf2f0-108">**IPersistMessage method**</span></span>|<span data-ttu-id="cf2f0-109">**操作**</span><span class="sxs-lookup"><span data-stu-id="cf2f0-109">**Action**</span></span>|<span data-ttu-id="cf2f0-110">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="cf2f0-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf2f0-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="cf2f0-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="cf2f0-112">埋め込みオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-112">Open any embedded objects.</span></span> <span data-ttu-id="cf2f0-113">_PMessage_に格納されているメッセージ内のデータを保証して、以前の[IPersistMessage::Save](ipersistmessage-save.md)の呼び出し内のメッセージと同じであります。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="cf2f0-114">**SaveCompleted**の呼び出しが成功した場合は、通常の状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="cf2f0-115">それ以外の場合、E_OUTOFMEMORY を最後にエラーを設定し、HandsOffAfterSave 状態のままです。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="cf2f0-116">[標準](normal-state.md)または HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="cf2f0-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="cf2f0-117">**IPersistMessage::SaveCompleted**(_pMessage = =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="cf2f0-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="cf2f0-118">E_INVALIDARG、E_UNEXPECTED を最後にエラーを設定します。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="cf2f0-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="cf2f0-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="cf2f0-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)、**保存**、または[IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="cf2f0-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="cf2f0-121">最後のエラーを設定、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="cf2f0-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="cf2f0-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="cf2f0-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="cf2f0-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="cf2f0-124">移行先のメッセージには、フォーム オブジェクトにデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="cf2f0-125">この呼び出しは、フォーム オブジェクトがフォルダー内の次または前のメッセージを移動したときに発生します。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="cf2f0-126">Normal</span><span class="sxs-lookup"><span data-stu-id="cf2f0-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="cf2f0-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="cf2f0-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="cf2f0-128">最後のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="cf2f0-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="cf2f0-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="cf2f0-130">他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたはその他のインターフェイスのメソッド</span><span class="sxs-lookup"><span data-stu-id="cf2f0-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="cf2f0-131">最後のエラーを設定、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="cf2f0-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="cf2f0-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="cf2f0-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf2f0-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf2f0-133">See also</span></span>



[<span data-ttu-id="cf2f0-134">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="cf2f0-134">Form States</span></span>](form-states.md)

