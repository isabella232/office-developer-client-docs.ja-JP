---
title: NoScribble 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 41f5acddf273de39a7d5952ccb00e868170c692d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801669"
---
# <a name="noscribble-state"></a><span data-ttu-id="9776a-103">NoScribble 状態</span><span class="sxs-lookup"><span data-stu-id="9776a-103">NoScribble State</span></span>

  
  
<span data-ttu-id="9776a-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9776a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9776a-105">NoScribble 状態では、メッセージに対する変更が保存されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="9776a-105">The NoScribble state indicates that changes to a message are being saved.</span></span> <span data-ttu-id="9776a-106">クライアント アプリケーションによってフォーム オブジェクトの[IPersistMessage::Save](ipersistmessage-save.md)メソッドが呼び出されたときに、フォーム オブジェクトのユーザー インターフェイスに格納されている値の実際の保存が発生します。</span><span class="sxs-lookup"><span data-stu-id="9776a-106">The actual saving of values stored in the form object's user interface occurs when the form object's [IPersistMessage::Save](ipersistmessage-save.md) method is called by the client application.</span></span> <span data-ttu-id="9776a-107">次の表では、NoScribble の状態から有効な遷移について説明します。</span><span class="sxs-lookup"><span data-stu-id="9776a-107">The following table describes allowed transitions from the NoScribble state.</span></span> 
  
|<span data-ttu-id="9776a-108">* IPersistMessage * 方法 * *</span><span class="sxs-lookup"><span data-stu-id="9776a-108">****IPersistMessage** method**</span></span>|<span data-ttu-id="9776a-109">**操作**</span><span class="sxs-lookup"><span data-stu-id="9776a-109">**Action**</span></span>|<span data-ttu-id="9776a-110">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="9776a-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9776a-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage = =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="9776a-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="9776a-112">_FSameAsLoad_フラグが TRUE の場合、NoScribble の状態と、メッセージを入力するフォームの原因となった[IPersistMessage::Save](ipersistmessage-save.md)の呼び出しが変更されて、内部的にマークの変更を保存して[IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md)を呼び出すメソッドです。</span><span class="sxs-lookup"><span data-stu-id="9776a-112">If  _fSameAsLoad_ flag was TRUE on the [IPersistMessage::Save](ipersistmessage-save.md) call that caused the form to enter the NoScribble state and the message has been modified, internally mark the changes as saved and call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method.</span></span>  <br/> |[<span data-ttu-id="9776a-113">Normal</span><span class="sxs-lookup"><span data-stu-id="9776a-113">Normal</span></span>](normal-state.md) <br/> |
|<span data-ttu-id="9776a-114">**IPersistMessage::SaveCompleted**(_pMessage! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="9776a-114">**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="9776a-115">**SaveCompleted**の通常の操作の後に (OLE [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx)メソッドのような) [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9776a-115">Call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method (similar to the OLE [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) method) followed by the normal **SaveCompleted** actions.</span></span> <span data-ttu-id="9776a-116">**SaveCompleted**が成功した場合は、通常の状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="9776a-116">If **SaveCompleted** was successful, enter the Normal state.</span></span> <span data-ttu-id="9776a-117">それ以外の場合、 [HandsOffAfterSave](handsoffaftersave-state.md)の状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="9776a-117">Otherwise, enter the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span>  <br/> |<span data-ttu-id="9776a-118">標準または HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="9776a-118">Normal or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="9776a-119">**HandsOffMessage**</span><span class="sxs-lookup"><span data-stu-id="9776a-119">**HandsOffMessage**</span></span> <br/> |<span data-ttu-id="9776a-120">再帰的には、埋め込みメッセージでは、 **HandsOffMessage**メソッドまたは埋め込まれた OLE オブジェクトの OLE の**IPersistStorage::HandsOffStorage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9776a-120">Recursively invoke the **HandsOffMessage** method on embedded messages or the OLE **IPersistStorage::HandsOffStorage** method on embedded OLE objects.</span></span> <span data-ttu-id="9776a-121">メッセージ オブジェクトを解放し、埋め込みオブジェクトまたはメッセージ。</span><span class="sxs-lookup"><span data-stu-id="9776a-121">Release the message object and any embedded messages or objects.</span></span>  <br/> |<span data-ttu-id="9776a-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="9776a-122">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="9776a-123">**保存**、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)、または[IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="9776a-123">**Save**, [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="9776a-124">最後のエラーを設定、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="9776a-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="9776a-125">NoScribble</span><span class="sxs-lookup"><span data-stu-id="9776a-125">NoScribble</span></span>  <br/> |
|[<span data-ttu-id="9776a-126">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9776a-126">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="9776a-127">最後のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="9776a-127">Return the last error.</span></span>  <br/> |<span data-ttu-id="9776a-128">NoScribble</span><span class="sxs-lookup"><span data-stu-id="9776a-128">NoScribble</span></span>  <br/> |
|<span data-ttu-id="9776a-129">他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたはその他のインターフェイスのメソッド</span><span class="sxs-lookup"><span data-stu-id="9776a-129">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="9776a-130">最後のエラーを設定、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="9776a-130">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="9776a-131">NoScribble</span><span class="sxs-lookup"><span data-stu-id="9776a-131">NoScribble</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9776a-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="9776a-132">See also</span></span>



[<span data-ttu-id="9776a-133">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="9776a-133">Form States</span></span>](form-states.md)

