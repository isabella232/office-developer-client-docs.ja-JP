---
title: 保存の状態を処理する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299525"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="8625d-103">保存の状態を処理する</span><span class="sxs-lookup"><span data-stu-id="8625d-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="8625d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8625d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8625d-105">[保存の状態を維持するのは、フォームの内容を永続的なストレージに保存するプロセスの一部です。</span><span class="sxs-lookup"><span data-stu-id="8625d-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="8625d-106">この状態では、フォームオブジェクトは、メッセージのプロパティの値のメモリ内コピーを変更しないようにする必要があります。これらの変更を保存する機会が他にはない可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="8625d-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="8625d-107">次の表では、保存の状態から許可される遷移について説明します。</span><span class="sxs-lookup"><span data-stu-id="8625d-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="8625d-108">**IPersistMessage メソッド**</span><span class="sxs-lookup"><span data-stu-id="8625d-108">**IPersistMessage method**</span></span>|<span data-ttu-id="8625d-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="8625d-109">**Action**</span></span>|<span data-ttu-id="8625d-110">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="8625d-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8625d-111">[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md)(_pmessage! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="8625d-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="8625d-112">埋め込みオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="8625d-112">Open any embedded objects.</span></span> <span data-ttu-id="8625d-113">_pmessage_に格納されているメッセージのデータは、前の[IPersistMessage:: Save](ipersistmessage-save.md)呼び出しのメッセージと同じであることが保証されています。</span><span class="sxs-lookup"><span data-stu-id="8625d-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="8625d-114">**SaveCompleted**の呼び出しが成功した場合は、通常の状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="8625d-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="8625d-115">それ以外の場合は、最後のエラーを E_OUTOFMEMORY に設定し、[保存の状態] のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="8625d-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="8625d-116">[Normal](normal-state.md)または標準の保存</span><span class="sxs-lookup"><span data-stu-id="8625d-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="8625d-117">**IPersistMessage:: SaveCompleted**(_pmessage = =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="8625d-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="8625d-118">最後のエラーを E_INVALIDARG または E_UNEXPECTED に設定します。</span><span class="sxs-lookup"><span data-stu-id="8625d-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="8625d-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8625d-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="8625d-120">[IPersistMessage:: IPersistMessage soffmessage](ipersistmessage-handsoffmessage.md)、 **Save**、または[:: InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="8625d-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="8625d-121">最後のエラーをに設定し、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="8625d-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="8625d-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8625d-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="8625d-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="8625d-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="8625d-124">form オブジェクトに対象のメッセージのデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="8625d-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="8625d-125">この呼び出しは、フォームオブジェクトがフォルダー内の次または前のメッセージに送られるときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8625d-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="8625d-126">標準</span><span class="sxs-lookup"><span data-stu-id="8625d-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="8625d-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8625d-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="8625d-128">直前のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="8625d-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="8625d-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8625d-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="8625d-130">その他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたは他のインターフェイスからのメソッド</span><span class="sxs-lookup"><span data-stu-id="8625d-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="8625d-131">最後のエラーをに設定し、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="8625d-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="8625d-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8625d-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8625d-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="8625d-133">See also</span></span>



[<span data-ttu-id="8625d-134">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="8625d-134">Form States</span></span>](form-states.md)

