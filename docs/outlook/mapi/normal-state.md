---
title: 通常の状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335744"
---
# <a name="normal-state"></a><span data-ttu-id="ce7ed-103">通常の状態</span><span class="sxs-lookup"><span data-stu-id="ce7ed-103">Normal State</span></span>

  
  
<span data-ttu-id="ce7ed-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce7ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce7ed-105">通常の状態とは、フォームオブジェクトが最も多くの時間を費やしている場所で、クライアントアプリケーションが変更を保存したり、フォームを閉じたりするなどの操作を開始するのを待機します。</span><span class="sxs-lookup"><span data-stu-id="ce7ed-105">The Normal state is where the form object spends most of its time, waiting for client applications to initiate an action such as saving changes or closing the form.</span></span> <span data-ttu-id="ce7ed-106">次の表は、通常の状態から許可される遷移を示しています。</span><span class="sxs-lookup"><span data-stu-id="ce7ed-106">The following table describes allowed transitions from the Normal state.</span></span>
  
|<span data-ttu-id="ce7ed-107">**IPersistMessage メソッド**</span><span class="sxs-lookup"><span data-stu-id="ce7ed-107">**IPersistMessage method**</span></span>|<span data-ttu-id="ce7ed-108">**Action**</span><span class="sxs-lookup"><span data-stu-id="ce7ed-108">**Action**</span></span>|<span data-ttu-id="ce7ed-109">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="ce7ed-109">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce7ed-110">[IPersistMessage:: 保存](ipersistmessage-save.md)(_pmessage = =_ NULL、 _fsameasload = =_ TRUE)</span><span class="sxs-lookup"><span data-stu-id="ce7ed-110">[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)</span></span>  <br/> <span data-ttu-id="ce7ed-111">または</span><span class="sxs-lookup"><span data-stu-id="ce7ed-111">-or-</span></span>  <br/> <span data-ttu-id="ce7ed-112">**IPersistMessage:: 保存**(_pmessage! =_ NULL、 _fsameasload = =_ FALSE)</span><span class="sxs-lookup"><span data-stu-id="ce7ed-112">**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)</span></span>  <br/> |<span data-ttu-id="ce7ed-113">変更されたすべての埋め込み OLE オブジェクトを、再帰的に保存します。</span><span class="sxs-lookup"><span data-stu-id="ce7ed-113">Recursively save any embedded OLE objects that have been modified.</span></span> <span data-ttu-id="ce7ed-114">メッセージのデータをメッセージオブジェクトに保存します。</span><span class="sxs-lookup"><span data-stu-id="ce7ed-114">Save message data back to the message object.</span></span> <span data-ttu-id="ce7ed-115">今後使用するために_fsameasload_フラグを[noscribble](noscribble-state.md)状態で保存します。</span><span class="sxs-lookup"><span data-stu-id="ce7ed-115">Store the  _fSameAsLoad_ flag for later use in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="ce7ed-116">NoScribble</span><span class="sxs-lookup"><span data-stu-id="ce7ed-116">NoScribble</span></span>  <br/> |
|<span data-ttu-id="ce7ed-117">**IPersistMessage:: 保存**(_pmessage! =_ NULL、 _fsameasload = =_ TRUE)</span><span class="sxs-lookup"><span data-stu-id="ce7ed-117">**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)</span></span>  <br/> |<span data-ttu-id="ce7ed-118">これは前の例と同じですが、この**Save**呼び出しはメモリが不足している状況では使用されていますが、メモリ不足の場合は失敗しません。</span><span class="sxs-lookup"><span data-stu-id="ce7ed-118">This is the same as the previous case, except that this **Save** call is used in low-memory situations and must not fail for lack of memory.</span></span>  <br/> |<span data-ttu-id="ce7ed-119">NoScribble</span><span class="sxs-lookup"><span data-stu-id="ce7ed-119">NoScribble</span></span>  <br/> |
|[<span data-ttu-id="ce7ed-120">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="ce7ed-120">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="ce7ed-121">埋め込まれ\*\*\*\* たメッセージに対して、または ole [IPersistStorage:: 配布用](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx)の ole オブジェクトに対して、配布のために、このメソッドを再帰的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ce7ed-121">Recursively invoke the **HandsOffMessage** method on embedded messages or the OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) method on embedded OLE objects.</span></span> <span data-ttu-id="ce7ed-122">メッセージオブジェクトおよび埋め込まれたメッセージまたはオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="ce7ed-122">Release the message object and any embedded messages or objects.</span></span>  <br/> |[<span data-ttu-id="ce7ed-123">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="ce7ed-123">HandsOffFromNormal</span></span>](handsofffromnormal-state.md) <br/> |
|<span data-ttu-id="ce7ed-124">[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage:: InitNew](ipersistmessage-initnew.md)または[IPersistMessage:: Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="ce7ed-124">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="ce7ed-125">最後のエラーをに設定し、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="ce7ed-125">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="ce7ed-126">標準</span><span class="sxs-lookup"><span data-stu-id="ce7ed-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="ce7ed-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ce7ed-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="ce7ed-128">直前のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="ce7ed-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="ce7ed-129">標準</span><span class="sxs-lookup"><span data-stu-id="ce7ed-129">Normal</span></span>  <br/> |
|<span data-ttu-id="ce7ed-130">その他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたは他のインターフェイスからのメソッド</span><span class="sxs-lookup"><span data-stu-id="ce7ed-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="ce7ed-131">[IPersistMessage: IUnknown](ipersistmessageiunknown.md)インターフェイスのドキュメントで説明されているとおりに実装します。</span><span class="sxs-lookup"><span data-stu-id="ce7ed-131">Implement as described in the documentation for the [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface.</span></span>  <br/> |<span data-ttu-id="ce7ed-132">標準</span><span class="sxs-lookup"><span data-stu-id="ce7ed-132">Normal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce7ed-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="ce7ed-133">See also</span></span>



[<span data-ttu-id="ce7ed-134">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="ce7ed-134">Form States</span></span>](form-states.md)

