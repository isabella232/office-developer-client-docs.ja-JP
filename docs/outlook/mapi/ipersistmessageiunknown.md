---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 346a2bce6d5709490ad11da842ed4f3e794b1996
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569191"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="dcbac-103">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dcbac-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="dcbac-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcbac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcbac-105">フォームのさまざまな状態間の遷移にストレージを処理するためにフォームのビューアーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="dcbac-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dcbac-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dcbac-106">Header file:</span></span>  <br/> |<span data-ttu-id="dcbac-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="dcbac-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="dcbac-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="dcbac-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="dcbac-109">メッセージ オブジェクトを永続化します。</span><span class="sxs-lookup"><span data-stu-id="dcbac-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="dcbac-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="dcbac-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="dcbac-111">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="dcbac-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="dcbac-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="dcbac-112">Called by:</span></span>  <br/> |<span data-ttu-id="dcbac-113">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="dcbac-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="dcbac-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="dcbac-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="dcbac-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="dcbac-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="dcbac-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="dcbac-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="dcbac-117">LPPERSISTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="dcbac-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="dcbac-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="dcbac-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="dcbac-119">発生しました</span><span class="sxs-lookup"><span data-stu-id="dcbac-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="dcbac-120">フォーム オブジェクトでは、前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="dcbac-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="dcbac-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="dcbac-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="dcbac-122">フォームを管理するフォームのサーバーを表す識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="dcbac-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="dcbac-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="dcbac-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="dcbac-124">最後の保存以降に加えた変更のフォームをチェックします。</span><span class="sxs-lookup"><span data-stu-id="dcbac-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="dcbac-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="dcbac-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="dcbac-126">新しいメッセージを初期化します。</span><span class="sxs-lookup"><span data-stu-id="dcbac-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="dcbac-127">Load</span><span class="sxs-lookup"><span data-stu-id="dcbac-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="dcbac-128">指定されたメッセージのフォームが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="dcbac-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="dcbac-129">Save</span><span class="sxs-lookup"><span data-stu-id="dcbac-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="dcbac-130">変更後のフォームを元に読み込みまたは作成したメッセージに保存します。</span><span class="sxs-lookup"><span data-stu-id="dcbac-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="dcbac-131">SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="dcbac-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="dcbac-132">フォームに通知する、保存操作が完了しました。</span><span class="sxs-lookup"><span data-stu-id="dcbac-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="dcbac-133">HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="dcbac-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="dcbac-134">フォームの現在のメッセージを解放するが発生します。</span><span class="sxs-lookup"><span data-stu-id="dcbac-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcbac-135">注釈</span><span class="sxs-lookup"><span data-stu-id="dcbac-135">Remarks</span></span>

<span data-ttu-id="dcbac-136">すべてのフォームは、 **IPersistMessage**インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcbac-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="dcbac-137">**IPersistMessage**は、[すること](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)の OLE インターフェイスと同様に動作します。</span><span class="sxs-lookup"><span data-stu-id="dcbac-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="dcbac-138">詳細については、**すること**の方法を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dcbac-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dcbac-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="dcbac-139">See also</span></span>



[<span data-ttu-id="dcbac-140">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="dcbac-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

