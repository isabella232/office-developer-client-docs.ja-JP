---
title: HandsOffFromNormal State
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426472"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="92ae6-103">HandsOffFromNormal State</span><span class="sxs-lookup"><span data-stu-id="92ae6-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="92ae6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92ae6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92ae6-105">HandsOffFromNormal 状態は [、HandsOffAfterSave 状態と非常に似](handsoffaftersave-state.md) ています。</span><span class="sxs-lookup"><span data-stu-id="92ae6-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="92ae6-106">これは、フォームの内容を永続的な記憶域に保存するプロセスの一部です。</span><span class="sxs-lookup"><span data-stu-id="92ae6-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="92ae6-107">この状態の場合、フォーム オブジェクトは、メッセージのプロパティの値のメモリ内コピーに変更を加えるのを控える必要があります。これらの変更を保存する別の機会が存在しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="92ae6-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="92ae6-108">次の表では、HandsOffFromNormal 状態からの許可された移行について説明します。</span><span class="sxs-lookup"><span data-stu-id="92ae6-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="92ae6-109">IPersistMessage\*\* メソッド\*\*</span><span class="sxs-lookup"><span data-stu-id="92ae6-109">\*\*\*\*IPersistMessage\*\* method\*\*</span></span>|<span data-ttu-id="92ae6-110">**Action**</span><span class="sxs-lookup"><span data-stu-id="92ae6-110">**Action**</span></span>|<span data-ttu-id="92ae6-111">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="92ae6-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="92ae6-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span><span class="sxs-lookup"><span data-stu-id="92ae6-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="92ae6-113">メッセージ オブジェクトのメッセージを  _pMessage_ に置き換え [、IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)の前の呼び出しによって取り消されたメッセージの代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="92ae6-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="92ae6-114">新しいメッセージのデータは、取り消されたメッセージと同じになる必要があります。</span><span class="sxs-lookup"><span data-stu-id="92ae6-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="92ae6-115">メッセージをクリーンとしてマークしたり [、IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) をこの呼び出し後に呼び出したりする必要もありません。</span><span class="sxs-lookup"><span data-stu-id="92ae6-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="92ae6-116">**SaveCompleted 呼び出しが** 成功した場合は、Normal 状態 [を入力](normal-state.md)します。</span><span class="sxs-lookup"><span data-stu-id="92ae6-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="92ae6-117">それ以外の場合は、HandsOffFromNormal 状態にとどまります。</span><span class="sxs-lookup"><span data-stu-id="92ae6-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="92ae6-118">Normal または HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="92ae6-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="92ae6-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="92ae6-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="92ae6-120">最後のエラーを [エラー] にE_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="92ae6-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="92ae6-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="92ae6-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="92ae6-122">**HandsOffMessage**、 [IPersistMessage::Save](ipersistmessage-save.md)、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)、 [または IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="92ae6-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="92ae6-123">最後のエラーを [エラー] にE_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="92ae6-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="92ae6-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="92ae6-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="92ae6-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="92ae6-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="92ae6-126">最後のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="92ae6-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="92ae6-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="92ae6-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="92ae6-128">その [他の IPersistMessage : 他のインターフェイスからの IUnknown](ipersistmessageiunknown.md) メソッドまたはメソッド</span><span class="sxs-lookup"><span data-stu-id="92ae6-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="92ae6-129">最後のエラーを [エラー] にE_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="92ae6-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="92ae6-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="92ae6-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92ae6-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="92ae6-131">See also</span></span>



[<span data-ttu-id="92ae6-132">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="92ae6-132">Form States</span></span>](form-states.md)

