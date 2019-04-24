---
title: 標準の状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299469"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="25660-103">標準の状態</span><span class="sxs-lookup"><span data-stu-id="25660-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="25660-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25660-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25660-105">標準の状態は、[標準として[保存](handsoffaftersave-state.md)する (標準)。</span><span class="sxs-lookup"><span data-stu-id="25660-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="25660-106">これは、フォームの内容を永続的なストレージに保存するプロセスの一部です。</span><span class="sxs-lookup"><span data-stu-id="25660-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="25660-107">この状態では、フォームオブジェクトは、メッセージのプロパティの値のメモリ内コピーを変更しないようにする必要があります。これらの変更を保存する機会が他にはない可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="25660-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="25660-108">次の表では、標準状態からの使用可能な移行について説明します。</span><span class="sxs-lookup"><span data-stu-id="25660-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="25660-109">IPersistMessage \* \* メソッド \* \*</span><span class="sxs-lookup"><span data-stu-id="25660-109">\*\*\*\*IPersistMessage\*\* method\*\*</span></span>|<span data-ttu-id="25660-110">**Action**</span><span class="sxs-lookup"><span data-stu-id="25660-110">**Action**</span></span>|<span data-ttu-id="25660-111">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="25660-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="25660-112">[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md)(_pmessage! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="25660-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="25660-113">メッセージオブジェクトのメッセージを_pmessage_に置き換えます。これは、前の呼び出しによって取り消されたメッセージの置換である[IPersistMessage::](ipersistmessage-handsoffmessage.md)[配布] [メッセージ] に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="25660-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="25660-114">新しいメッセージのデータは、失効したメッセージと同じであることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="25660-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="25660-115">この呼び出しの後に、メッセージを clean としてマークしたり、 [IMAPIViewAdviseSink:: onsaved](imapiviewadvisesink-onsaved.md)を呼び出すことができないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="25660-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="25660-116">**SaveCompleted**の呼び出しが成功した場合は、[通常](normal-state.md)の状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="25660-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="25660-117">それ以外の場合は、[標準] をそのままにします。</span><span class="sxs-lookup"><span data-stu-id="25660-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="25660-118">通常または標準の標準</span><span class="sxs-lookup"><span data-stu-id="25660-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="25660-119">**IPersistMessage:: SaveCompleted**(_pmessage = =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="25660-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="25660-120">最後のエラーを E_UNEXPECTED に設定します。</span><span class="sxs-lookup"><span data-stu-id="25660-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="25660-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="25660-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="25660-122">\*\*\*\* [IPersistMessage:: Save](ipersistmessage-save.md)、 [IPersistMessage:: InitNew](ipersistmessage-initnew.md)、または[IPersistMessage:: Load](ipersistmessage-load.md)を実行します。</span><span class="sxs-lookup"><span data-stu-id="25660-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="25660-123">最後のエラーを E_UNEXPECTED に設定します。</span><span class="sxs-lookup"><span data-stu-id="25660-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="25660-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="25660-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="25660-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="25660-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="25660-126">直前のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="25660-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="25660-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="25660-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="25660-128">その他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたは他のインターフェイスからのメソッド</span><span class="sxs-lookup"><span data-stu-id="25660-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="25660-129">最後のエラーを E_UNEXPECTED に設定します。</span><span class="sxs-lookup"><span data-stu-id="25660-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="25660-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="25660-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25660-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="25660-131">See also</span></span>



[<span data-ttu-id="25660-132">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="25660-132">Form States</span></span>](form-states.md)

