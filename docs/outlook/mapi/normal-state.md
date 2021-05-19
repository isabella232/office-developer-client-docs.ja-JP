---
title: 標準状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335744"
---
# <a name="normal-state"></a><span data-ttu-id="7c003-103">標準状態</span><span class="sxs-lookup"><span data-stu-id="7c003-103">Normal State</span></span>

  
  
<span data-ttu-id="7c003-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c003-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c003-105">Normal 状態は、フォーム オブジェクトがほとんどの時間を費やし、クライアント アプリケーションが変更の保存やフォームの終了などのアクションを開始するのを待つ状態です。</span><span class="sxs-lookup"><span data-stu-id="7c003-105">The Normal state is where the form object spends most of its time, waiting for client applications to initiate an action such as saving changes or closing the form.</span></span> <span data-ttu-id="7c003-106">次の表に、Normal 状態からの移行を許可する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7c003-106">The following table describes allowed transitions from the Normal state.</span></span>
  
|<span data-ttu-id="7c003-107">**IPersistMessage メソッド**</span><span class="sxs-lookup"><span data-stu-id="7c003-107">**IPersistMessage method**</span></span>|<span data-ttu-id="7c003-108">**Action**</span><span class="sxs-lookup"><span data-stu-id="7c003-108">**Action**</span></span>|<span data-ttu-id="7c003-109">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="7c003-109">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7c003-110">[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)</span><span class="sxs-lookup"><span data-stu-id="7c003-110">[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)</span></span>  <br/> <span data-ttu-id="7c003-111">または</span><span class="sxs-lookup"><span data-stu-id="7c003-111">-or-</span></span>  <br/> <span data-ttu-id="7c003-112">**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)</span><span class="sxs-lookup"><span data-stu-id="7c003-112">**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)</span></span>  <br/> |<span data-ttu-id="7c003-113">変更された埋め込み OLE オブジェクトを再帰的に保存します。</span><span class="sxs-lookup"><span data-stu-id="7c003-113">Recursively save any embedded OLE objects that have been modified.</span></span> <span data-ttu-id="7c003-114">メッセージ データをメッセージ オブジェクトに保存します。</span><span class="sxs-lookup"><span data-stu-id="7c003-114">Save message data back to the message object.</span></span> <span data-ttu-id="7c003-115">後で  _使用する fSameAsLoad_ フラグを [NoScribble 状態に格納](noscribble-state.md) します。</span><span class="sxs-lookup"><span data-stu-id="7c003-115">Store the  _fSameAsLoad_ flag for later use in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="7c003-116">NoScribble</span><span class="sxs-lookup"><span data-stu-id="7c003-116">NoScribble</span></span>  <br/> |
|<span data-ttu-id="7c003-117">**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)</span><span class="sxs-lookup"><span data-stu-id="7c003-117">**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)</span></span>  <br/> |<span data-ttu-id="7c003-118">これは、前のケースと同じですが、このSave 呼び出しはメモリ不足の状況で使用され、メモリ不足のために失敗しはしません。</span><span class="sxs-lookup"><span data-stu-id="7c003-118">This is the same as the previous case, except that this **Save** call is used in low-memory situations and must not fail for lack of memory.</span></span>  <br/> |<span data-ttu-id="7c003-119">NoScribble</span><span class="sxs-lookup"><span data-stu-id="7c003-119">NoScribble</span></span>  <br/> |
|[<span data-ttu-id="7c003-120">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="7c003-120">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="7c003-121">埋め込みメッセージ **の HandsOffMessage** メソッド、または埋め込み OLE オブジェクトの OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) メソッドを再帰的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7c003-121">Recursively invoke the **HandsOffMessage** method on embedded messages or the OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) method on embedded OLE objects.</span></span> <span data-ttu-id="7c003-122">メッセージ オブジェクトと埋め込みメッセージまたはオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="7c003-122">Release the message object and any embedded messages or objects.</span></span>  <br/> |[<span data-ttu-id="7c003-123">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7c003-123">HandsOffFromNormal</span></span>](handsofffromnormal-state.md) <br/> |
|<span data-ttu-id="7c003-124">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) または [IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="7c003-124">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="7c003-125">最後のエラーを設定し、エラーを返E_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="7c003-125">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7c003-126">標準</span><span class="sxs-lookup"><span data-stu-id="7c003-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="7c003-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7c003-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="7c003-128">最後のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="7c003-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="7c003-129">標準</span><span class="sxs-lookup"><span data-stu-id="7c003-129">Normal</span></span>  <br/> |
|<span data-ttu-id="7c003-130">その [他の IPersistMessage : 他のインターフェイスからの IUnknown](ipersistmessageiunknown.md) メソッドまたはメソッド</span><span class="sxs-lookup"><span data-stu-id="7c003-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="7c003-131">[IPersistMessage : IUnknown](ipersistmessageiunknown.md)インターフェイスのドキュメントで説明されているとおりに実装します。</span><span class="sxs-lookup"><span data-stu-id="7c003-131">Implement as described in the documentation for the [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface.</span></span>  <br/> |<span data-ttu-id="7c003-132">標準</span><span class="sxs-lookup"><span data-stu-id="7c003-132">Normal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c003-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c003-133">See also</span></span>



[<span data-ttu-id="7c003-134">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="7c003-134">Form States</span></span>](form-states.md)

