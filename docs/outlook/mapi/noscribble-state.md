---
title: NoScribble 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326202"
---
# <a name="noscribble-state"></a><span data-ttu-id="c5e88-103">NoScribble 状態</span><span class="sxs-lookup"><span data-stu-id="c5e88-103">NoScribble State</span></span>

  
  
<span data-ttu-id="c5e88-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5e88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5e88-105">NoScribble 状態は、メッセージに対する変更が保存されている状態を示します。</span><span class="sxs-lookup"><span data-stu-id="c5e88-105">The NoScribble state indicates that changes to a message are being saved.</span></span> <span data-ttu-id="c5e88-106">フォーム オブジェクトのユーザー インターフェイスに格納されている値の実際の保存は、フォーム オブジェクトの [IPersistMessage::Save](ipersistmessage-save.md) メソッドがクライアント アプリケーションによって呼び出された場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="c5e88-106">The actual saving of values stored in the form object's user interface occurs when the form object's [IPersistMessage::Save](ipersistmessage-save.md) method is called by the client application.</span></span> <span data-ttu-id="c5e88-107">次の表では、NoScribble 状態からの許可された移行について説明します。</span><span class="sxs-lookup"><span data-stu-id="c5e88-107">The following table describes allowed transitions from the NoScribble state.</span></span> 
  
|<span data-ttu-id="c5e88-108">IPersistMessage\*\* メソッド\*\*</span><span class="sxs-lookup"><span data-stu-id="c5e88-108">\*\*\*\*IPersistMessage\*\* method\*\*</span></span>|<span data-ttu-id="c5e88-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="c5e88-109">**Action**</span></span>|<span data-ttu-id="c5e88-110">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="c5e88-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c5e88-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="c5e88-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="c5e88-112">フォームが NoScribble 状態に入り、メッセージが変更された [IPersistMessage::Save](ipersistmessage-save.md)呼び出しで _fSameAsLoad_ フラグが TRUE の場合は、内部的に変更を保存済みとしてマークし [、IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c5e88-112">If  _fSameAsLoad_ flag was TRUE on the [IPersistMessage::Save](ipersistmessage-save.md) call that caused the form to enter the NoScribble state and the message has been modified, internally mark the changes as saved and call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method.</span></span>  <br/> |[<span data-ttu-id="c5e88-113">Normal</span><span class="sxs-lookup"><span data-stu-id="c5e88-113">Normal</span></span>](normal-state.md) <br/> |
|<span data-ttu-id="c5e88-114">**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)</span><span class="sxs-lookup"><span data-stu-id="c5e88-114">**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="c5e88-115">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッド (OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx)メソッドと同様) を呼び出し、その後に通常の **SaveCompleted** アクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c5e88-115">Call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method (similar to the OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) method) followed by the normal **SaveCompleted** actions.</span></span> <span data-ttu-id="c5e88-116">**SaveCompleted が成功した** 場合は、Normal 状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="c5e88-116">If **SaveCompleted** was successful, enter the Normal state.</span></span> <span data-ttu-id="c5e88-117">それ以外の場合は [、HandsOffAfterSave 状態を入力](handsoffaftersave-state.md) します。</span><span class="sxs-lookup"><span data-stu-id="c5e88-117">Otherwise, enter the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span>  <br/> |<span data-ttu-id="c5e88-118">Normal または HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="c5e88-118">Normal or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="c5e88-119">**HandsOffMessage**</span><span class="sxs-lookup"><span data-stu-id="c5e88-119">**HandsOffMessage**</span></span> <br/> |<span data-ttu-id="c5e88-120">埋め込みメッセージ **の HandsOffMessage** メソッド、または埋め込み OLE オブジェクトの OLE **IPersistStorage::HandsOffStorage** メソッドを再帰的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c5e88-120">Recursively invoke the **HandsOffMessage** method on embedded messages or the OLE **IPersistStorage::HandsOffStorage** method on embedded OLE objects.</span></span> <span data-ttu-id="c5e88-121">メッセージ オブジェクトと埋め込みメッセージまたはオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="c5e88-121">Release the message object and any embedded messages or objects.</span></span>  <br/> |<span data-ttu-id="c5e88-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="c5e88-122">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="c5e88-123">**Save** [、IPersistMessage::InitNew、](ipersistmessage-initnew.md)[または IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="c5e88-123">**Save**, [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="c5e88-124">最後のエラーを設定し、エラーを返E_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="c5e88-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="c5e88-125">NoScribble</span><span class="sxs-lookup"><span data-stu-id="c5e88-125">NoScribble</span></span>  <br/> |
|[<span data-ttu-id="c5e88-126">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c5e88-126">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="c5e88-127">最後のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="c5e88-127">Return the last error.</span></span>  <br/> |<span data-ttu-id="c5e88-128">NoScribble</span><span class="sxs-lookup"><span data-stu-id="c5e88-128">NoScribble</span></span>  <br/> |
|<span data-ttu-id="c5e88-129">その [他の IPersistMessage : 他のインターフェイスからの IUnknown](ipersistmessageiunknown.md) メソッドまたはメソッド</span><span class="sxs-lookup"><span data-stu-id="c5e88-129">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="c5e88-130">最後のエラーを設定し、エラーを返E_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="c5e88-130">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="c5e88-131">NoScribble</span><span class="sxs-lookup"><span data-stu-id="c5e88-131">NoScribble</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5e88-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="c5e88-132">See also</span></span>



[<span data-ttu-id="c5e88-133">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="c5e88-133">Form States</span></span>](form-states.md)

