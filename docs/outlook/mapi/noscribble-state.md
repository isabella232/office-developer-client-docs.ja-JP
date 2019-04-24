---
title: noscribble 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326202"
---
# <a name="noscribble-state"></a><span data-ttu-id="02477-103">noscribble 状態</span><span class="sxs-lookup"><span data-stu-id="02477-103">NoScribble State</span></span>

  
  
<span data-ttu-id="02477-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02477-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02477-105">noscribble 状態は、メッセージの変更が保存されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="02477-105">The NoScribble state indicates that changes to a message are being saved.</span></span> <span data-ttu-id="02477-106">form オブジェクトのユーザーインターフェイスに格納されている値は、クライアントアプリケーションによってフォームオブジェクトの[IPersistMessage:: Save](ipersistmessage-save.md)メソッドが呼び出されたときに実際に保存されます。</span><span class="sxs-lookup"><span data-stu-id="02477-106">The actual saving of values stored in the form object's user interface occurs when the form object's [IPersistMessage::Save](ipersistmessage-save.md) method is called by the client application.</span></span> <span data-ttu-id="02477-107">次の表は、noscribble 状態から許可される遷移を示しています。</span><span class="sxs-lookup"><span data-stu-id="02477-107">The following table describes allowed transitions from the NoScribble state.</span></span> 
  
|<span data-ttu-id="02477-108">IPersistMessage \* \* メソッド \* \*</span><span class="sxs-lookup"><span data-stu-id="02477-108">\*\*\*\*IPersistMessage\*\* method\*\*</span></span>|<span data-ttu-id="02477-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="02477-109">**Action**</span></span>|<span data-ttu-id="02477-110">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="02477-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="02477-111">[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md)(_pmessage = =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="02477-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="02477-112">フォームが noscribble 状態に入り、メッセージが変更されたという[IPersistMessage:: Save](ipersistmessage-save.md)呼び出しで、 _fsameasload_フラグが TRUE に設定されている場合は、変更を保存済みとして内部的にマークして、 [IMAPIViewAdviseSink:: onsaved](imapiviewadvisesink-onsaved.md)を呼び出します。手段.</span><span class="sxs-lookup"><span data-stu-id="02477-112">If  _fSameAsLoad_ flag was TRUE on the [IPersistMessage::Save](ipersistmessage-save.md) call that caused the form to enter the NoScribble state and the message has been modified, internally mark the changes as saved and call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method.</span></span>  <br/> |[<span data-ttu-id="02477-113">Normal</span><span class="sxs-lookup"><span data-stu-id="02477-113">Normal</span></span>](normal-state.md) <br/> |
|<span data-ttu-id="02477-114">**IPersistMessage:: SaveCompleted**(_pmessage! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="02477-114">**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="02477-115">[IPersistMessage::](ipersistmessage-handsoffmessage.md)配布 (OLE [IPersistStorage:: soffstorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx)メソッドと同様の) メソッドを呼び出します。その後に通常の**SaveCompleted**アクションが続きます。</span><span class="sxs-lookup"><span data-stu-id="02477-115">Call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method (similar to the OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) method) followed by the normal **SaveCompleted** actions.</span></span> <span data-ttu-id="02477-116">**SaveCompleted**が正常に終了した場合は、通常の状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="02477-116">If **SaveCompleted** was successful, enter the Normal state.</span></span> <span data-ttu-id="02477-117">それ以外の場合は、[[保存](handsoffaftersave-state.md)の状態] を入力します。</span><span class="sxs-lookup"><span data-stu-id="02477-117">Otherwise, enter the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span>  <br/> |<span data-ttu-id="02477-118">Normal または標準の保存</span><span class="sxs-lookup"><span data-stu-id="02477-118">Normal or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="02477-119">**「soffmessage」**</span><span class="sxs-lookup"><span data-stu-id="02477-119">**HandsOffMessage**</span></span> <br/> |<span data-ttu-id="02477-120">埋め込まれ\*\*\*\* たメッセージに対して、または ole **IPersistStorage:: 配布用**の ole オブジェクトに対して、配布のために、このメソッドを再帰的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02477-120">Recursively invoke the **HandsOffMessage** method on embedded messages or the OLE **IPersistStorage::HandsOffStorage** method on embedded OLE objects.</span></span> <span data-ttu-id="02477-121">メッセージオブジェクトおよび埋め込まれたメッセージまたはオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="02477-121">Release the message object and any embedded messages or objects.</span></span>  <br/> |<span data-ttu-id="02477-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="02477-122">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="02477-123">**Save**、 [IPersistMessage:: InitNew](ipersistmessage-initnew.md)、または[IPersistMessage:: Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="02477-123">**Save**, [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="02477-124">最後のエラーをに設定し、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="02477-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="02477-125">NoScribble</span><span class="sxs-lookup"><span data-stu-id="02477-125">NoScribble</span></span>  <br/> |
|[<span data-ttu-id="02477-126">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="02477-126">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="02477-127">直前のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="02477-127">Return the last error.</span></span>  <br/> |<span data-ttu-id="02477-128">NoScribble</span><span class="sxs-lookup"><span data-stu-id="02477-128">NoScribble</span></span>  <br/> |
|<span data-ttu-id="02477-129">その他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたは他のインターフェイスからのメソッド</span><span class="sxs-lookup"><span data-stu-id="02477-129">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="02477-130">最後のエラーをに設定し、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="02477-130">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="02477-131">NoScribble</span><span class="sxs-lookup"><span data-stu-id="02477-131">NoScribble</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02477-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="02477-132">See also</span></span>



[<span data-ttu-id="02477-133">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="02477-133">Form States</span></span>](form-states.md)

