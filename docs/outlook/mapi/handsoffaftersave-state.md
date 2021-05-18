---
title: HandsOffAfterSave 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406606"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="1f2b6-103">HandsOffAfterSave 状態</span><span class="sxs-lookup"><span data-stu-id="1f2b6-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="1f2b6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f2b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f2b6-105">HandsOffAfterSave 状態は、フォームの内容を永続的な記憶域に保存するプロセスの一部です。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="1f2b6-106">この状態の場合、フォーム オブジェクトは、メッセージのプロパティの値のメモリ内コピーに変更を加えるのを控える必要があります。これらの変更を保存する別の機会が存在しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="1f2b6-107">次の表では、HandsOffAfterSave 状態からの許可された移行について説明します。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="1f2b6-108">**IPersistMessage メソッド**</span><span class="sxs-lookup"><span data-stu-id="1f2b6-108">**IPersistMessage method**</span></span>|<span data-ttu-id="1f2b6-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="1f2b6-109">**Action**</span></span>|<span data-ttu-id="1f2b6-110">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="1f2b6-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1f2b6-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span><span class="sxs-lookup"><span data-stu-id="1f2b6-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="1f2b6-112">埋め込みオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-112">Open any embedded objects.</span></span> <span data-ttu-id="1f2b6-113">_pMessage_ に格納されているメッセージ内のデータは、前の [IPersistMessage::Save](ipersistmessage-save.md)呼び出しのメッセージと同じになる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="1f2b6-114">**SaveCompleted 呼び出しが** 成功した場合は、Normal 状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="1f2b6-115">それ以外の場合は、最後のエラーを [E_OUTOFMEMORYに設定し、HandsOffAfterSave 状態に残ります。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="1f2b6-116">[Normal または](normal-state.md) HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="1f2b6-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="1f2b6-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="1f2b6-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="1f2b6-118">最後のエラーを[エラー] または [E_INVALIDARG] にE_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="1f2b6-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="1f2b6-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="1f2b6-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) **、Save、**[または IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="1f2b6-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="1f2b6-121">最後のエラーを設定し、エラーを返E_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="1f2b6-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="1f2b6-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="1f2b6-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="1f2b6-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="1f2b6-124">ターゲット メッセージのデータを含むフォーム オブジェクトを読み込む。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="1f2b6-125">この呼び出しは、フォーム オブジェクトがフォルダー内の次または前のメッセージに移動するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="1f2b6-126">標準</span><span class="sxs-lookup"><span data-stu-id="1f2b6-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="1f2b6-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1f2b6-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="1f2b6-128">最後のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="1f2b6-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="1f2b6-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="1f2b6-130">その [他の IPersistMessage : 他のインターフェイスからの IUnknown](ipersistmessageiunknown.md) メソッドまたはメソッド</span><span class="sxs-lookup"><span data-stu-id="1f2b6-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="1f2b6-131">最後のエラーを設定し、エラーを返E_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="1f2b6-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="1f2b6-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="1f2b6-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f2b6-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f2b6-133">See also</span></span>



[<span data-ttu-id="1f2b6-134">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="1f2b6-134">Form States</span></span>](form-states.md)

