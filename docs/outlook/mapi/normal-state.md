---
title: 通常の状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dcc92d220f07b1c111284acacac4a65a2e3f8b6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801659"
---
# <a name="normal-state"></a><span data-ttu-id="dc9a4-103">通常の状態</span><span class="sxs-lookup"><span data-stu-id="dc9a4-103">Normal State</span></span>

  
  
<span data-ttu-id="dc9a4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc9a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc9a4-105">通常の状態では、form オブジェクトが変更を保存するか、フォームを閉じるなどの操作を開始するクライアント アプリケーションを待機して、その時間のほとんどを費やしています。</span><span class="sxs-lookup"><span data-stu-id="dc9a4-105">The Normal state is where the form object spends most of its time, waiting for client applications to initiate an action such as saving changes or closing the form.</span></span> <span data-ttu-id="dc9a4-106">次の表では、通常の状態から有効な遷移について説明します。</span><span class="sxs-lookup"><span data-stu-id="dc9a4-106">The following table describes allowed transitions from the Normal state.</span></span>
  
|<span data-ttu-id="dc9a4-107">**IPersistMessage メソッド**</span><span class="sxs-lookup"><span data-stu-id="dc9a4-107">**IPersistMessage method**</span></span>|<span data-ttu-id="dc9a4-108">**アクション**</span><span class="sxs-lookup"><span data-stu-id="dc9a4-108">**Action**</span></span>|<span data-ttu-id="dc9a4-109">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="dc9a4-109">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc9a4-110">[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage = =_ NULL _fSameAsLoad = =_ TRUE)</span><span class="sxs-lookup"><span data-stu-id="dc9a4-110">[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)</span></span>  <br/> <span data-ttu-id="dc9a4-111">または</span><span class="sxs-lookup"><span data-stu-id="dc9a4-111">-or-</span></span>  <br/> <span data-ttu-id="dc9a4-112">**IPersistMessage::Save**(_pMessage! =_ NULL _fSameAsLoad = =_ は FALSE)</span><span class="sxs-lookup"><span data-stu-id="dc9a4-112">**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)</span></span>  <br/> |<span data-ttu-id="dc9a4-113">保存に変更されたすべての埋め込み OLE オブジェクトを再帰的にします。</span><span class="sxs-lookup"><span data-stu-id="dc9a4-113">Recursively save any embedded OLE objects that have been modified.</span></span> <span data-ttu-id="dc9a4-114">メッセージ オブジェクトには、メッセージ データを保存します。</span><span class="sxs-lookup"><span data-stu-id="dc9a4-114">Save message data back to the message object.</span></span> <span data-ttu-id="dc9a4-115">[NoScribble](noscribble-state.md)状態で後で使用できる_fSameAsLoad_フラグを格納します。</span><span class="sxs-lookup"><span data-stu-id="dc9a4-115">Store the  _fSameAsLoad_ flag for later use in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="dc9a4-116">NoScribble</span><span class="sxs-lookup"><span data-stu-id="dc9a4-116">NoScribble</span></span>  <br/> |
|<span data-ttu-id="dc9a4-117">**IPersistMessage::Save**(_pMessage! =_ NULL _fSameAsLoad = =_ TRUE)</span><span class="sxs-lookup"><span data-stu-id="dc9a4-117">**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)</span></span>  <br/> |<span data-ttu-id="dc9a4-118">これは、この**保存**の呼び出しはメモリ不足の状況で使用され、メモリ不足によって失敗する必要がありますが、前の例と同じです。</span><span class="sxs-lookup"><span data-stu-id="dc9a4-118">This is the same as the previous case, except that this **Save** call is used in low-memory situations and must not fail for lack of memory.</span></span>  <br/> |<span data-ttu-id="dc9a4-119">NoScribble</span><span class="sxs-lookup"><span data-stu-id="dc9a4-119">NoScribble</span></span>  <br/> |
|[<span data-ttu-id="dc9a4-120">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="dc9a4-120">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="dc9a4-121">再帰的には、埋め込みメッセージでは、 **HandsOffMessage**メソッドまたは埋め込まれた OLE オブジェクトの OLE の[IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dc9a4-121">Recursively invoke the **HandsOffMessage** method on embedded messages or the OLE [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) method on embedded OLE objects.</span></span> <span data-ttu-id="dc9a4-122">メッセージ オブジェクトを解放し、埋め込みオブジェクトまたはメッセージ。</span><span class="sxs-lookup"><span data-stu-id="dc9a4-122">Release the message object and any embedded messages or objects.</span></span>  <br/> |[<span data-ttu-id="dc9a4-123">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="dc9a4-123">HandsOffFromNormal</span></span>](handsofffromnormal-state.md) <br/> |
|<span data-ttu-id="dc9a4-124">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)または[IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="dc9a4-124">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="dc9a4-125">最後のエラーを設定、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="dc9a4-125">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="dc9a4-126">Normal</span><span class="sxs-lookup"><span data-stu-id="dc9a4-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="dc9a4-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="dc9a4-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="dc9a4-128">最後のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="dc9a4-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="dc9a4-129">Normal</span><span class="sxs-lookup"><span data-stu-id="dc9a4-129">Normal</span></span>  <br/> |
|<span data-ttu-id="dc9a4-130">他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたはその他のインターフェイスのメソッド</span><span class="sxs-lookup"><span data-stu-id="dc9a4-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="dc9a4-131">マニュアルで説明するように実装、 [IPersistMessage: IUnknown](ipersistmessageiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="dc9a4-131">Implement as described in the documentation for the [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface.</span></span>  <br/> |<span data-ttu-id="dc9a4-132">Normal</span><span class="sxs-lookup"><span data-stu-id="dc9a4-132">Normal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc9a4-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc9a4-133">See also</span></span>



[<span data-ttu-id="dc9a4-134">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="dc9a4-134">Form States</span></span>](form-states.md)

