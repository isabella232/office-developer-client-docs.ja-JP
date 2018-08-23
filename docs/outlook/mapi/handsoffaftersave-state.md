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
ms.openlocfilehash: 4bc4d680903d81b51a39ed39db3861597443d116
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800200"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="30a09-103">HandsOffAfterSave 状態</span><span class="sxs-lookup"><span data-stu-id="30a09-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="30a09-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30a09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30a09-105">HandsOffAfterSave の状態は、恒久的に保存するフォームの内容を保存するプロセスの一部です。</span><span class="sxs-lookup"><span data-stu-id="30a09-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="30a09-106">この状態のときにフォーム オブジェクト避ける必要がある、メモリ内のコピー、メッセージのプロパティの値を変更するため、別の機会をこれらの変更を保存することができません。</span><span class="sxs-lookup"><span data-stu-id="30a09-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="30a09-107">次の表では、HandsOffAfterSave の状態から有効な遷移について説明します。</span><span class="sxs-lookup"><span data-stu-id="30a09-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="30a09-108">**IPersistMessage メソッド**</span><span class="sxs-lookup"><span data-stu-id="30a09-108">**IPersistMessage method**</span></span>|<span data-ttu-id="30a09-109">**操作**</span><span class="sxs-lookup"><span data-stu-id="30a09-109">**Action**</span></span>|<span data-ttu-id="30a09-110">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="30a09-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30a09-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="30a09-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="30a09-112">埋め込みオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="30a09-112">Open any embedded objects.</span></span> <span data-ttu-id="30a09-113">_PMessage_に格納されているメッセージ内のデータを保証して、以前の[IPersistMessage::Save](ipersistmessage-save.md)の呼び出し内のメッセージと同じであります。</span><span class="sxs-lookup"><span data-stu-id="30a09-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="30a09-114">**SaveCompleted**の呼び出しが成功した場合は、通常の状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="30a09-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="30a09-115">それ以外の場合、E_OUTOFMEMORY を最後にエラーを設定し、HandsOffAfterSave 状態のままです。</span><span class="sxs-lookup"><span data-stu-id="30a09-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="30a09-116">[標準](normal-state.md)または HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="30a09-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="30a09-117">**IPersistMessage::SaveCompleted**(_pMessage = =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="30a09-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="30a09-118">E_INVALIDARG、E_UNEXPECTED を最後にエラーを設定します。</span><span class="sxs-lookup"><span data-stu-id="30a09-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="30a09-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="30a09-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="30a09-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)、**保存**、または[IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="30a09-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="30a09-121">最後のエラーを設定、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="30a09-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="30a09-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="30a09-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="30a09-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="30a09-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="30a09-124">移行先のメッセージには、フォーム オブジェクトにデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="30a09-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="30a09-125">この呼び出しは、フォーム オブジェクトがフォルダー内の次または前のメッセージを移動したときに発生します。</span><span class="sxs-lookup"><span data-stu-id="30a09-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="30a09-126">Normal</span><span class="sxs-lookup"><span data-stu-id="30a09-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="30a09-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="30a09-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="30a09-128">最後のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="30a09-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="30a09-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="30a09-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="30a09-130">他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたはその他のインターフェイスのメソッド</span><span class="sxs-lookup"><span data-stu-id="30a09-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="30a09-131">最後のエラーを設定、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="30a09-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="30a09-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="30a09-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30a09-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="30a09-133">See also</span></span>



[<span data-ttu-id="30a09-134">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="30a09-134">Form States</span></span>](form-states.md)

