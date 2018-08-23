---
title: HandsOffFromNormal 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d0b7baf4ab17d12145170961a43ca4be252146a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800208"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="c92c3-103">HandsOffFromNormal 状態</span><span class="sxs-lookup"><span data-stu-id="c92c3-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="c92c3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c92c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c92c3-105">HandsOffFromNormal 状態では、 [HandsOffAfterSave](handsoffaftersave-state.md)の状態に非常に似ています。</span><span class="sxs-lookup"><span data-stu-id="c92c3-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="c92c3-106">恒久的ストレージにフォームの内容を保存するプロセスの一部です。</span><span class="sxs-lookup"><span data-stu-id="c92c3-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="c92c3-107">この状態のときにフォーム オブジェクト避ける必要がある、メモリ内のコピー、メッセージのプロパティの値を変更するため、別の機会をこれらの変更を保存することができません。</span><span class="sxs-lookup"><span data-stu-id="c92c3-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="c92c3-108">次の表では、HandsOffFromNormal の状態から有効な遷移について説明します。</span><span class="sxs-lookup"><span data-stu-id="c92c3-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="c92c3-109">* IPersistMessage * 方法 * *</span><span class="sxs-lookup"><span data-stu-id="c92c3-109">****IPersistMessage** method**</span></span>|<span data-ttu-id="c92c3-110">**操作**</span><span class="sxs-lookup"><span data-stu-id="c92c3-110">**Action**</span></span>|<span data-ttu-id="c92c3-111">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="c92c3-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c92c3-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="c92c3-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="c92c3-113">メッセージ オブジェクトのメッセージを交換して、 [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)の以前の呼び出しによって無効にするメッセージの交換が_pMessage_と。</span><span class="sxs-lookup"><span data-stu-id="c92c3-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="c92c3-114">失効したメッセージと同じにする、新しいメッセージ内のデータが保証されます。</span><span class="sxs-lookup"><span data-stu-id="c92c3-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="c92c3-115">メッセージがクリーンとしてマークされていない必要がありますもする必要があります[IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md)はこの呼び出しの後呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c92c3-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="c92c3-116">**SaveCompleted**の呼び出しが成功した場合は、[通常](normal-state.md)の状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="c92c3-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="c92c3-117">それ以外の場合、HandsOffFromNormal の状態のままです。</span><span class="sxs-lookup"><span data-stu-id="c92c3-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="c92c3-118">標準または HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="c92c3-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="c92c3-119">**IPersistMessage::SaveCompleted**(_pMessage = =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="c92c3-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="c92c3-120">E_UNEXPECTED を最後にエラーを設定します。</span><span class="sxs-lookup"><span data-stu-id="c92c3-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="c92c3-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="c92c3-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="c92c3-122">**HandsOffMessage**、 [IPersistMessage::Save](ipersistmessage-save.md)、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)、または[IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="c92c3-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="c92c3-123">E_UNEXPECTED を最後にエラーを設定します。</span><span class="sxs-lookup"><span data-stu-id="c92c3-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="c92c3-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="c92c3-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="c92c3-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c92c3-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="c92c3-126">最後のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="c92c3-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="c92c3-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="c92c3-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="c92c3-128">他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたはその他のインターフェイスのメソッド</span><span class="sxs-lookup"><span data-stu-id="c92c3-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="c92c3-129">E_UNEXPECTED を最後にエラーを設定します。</span><span class="sxs-lookup"><span data-stu-id="c92c3-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="c92c3-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="c92c3-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c92c3-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="c92c3-131">See also</span></span>



[<span data-ttu-id="c92c3-132">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="c92c3-132">Form States</span></span>](form-states.md)

