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
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309605"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="1f1b0-103">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f1b0-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="1f1b0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f1b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f1b0-105">フォームビューアーがフォームのストレージを処理し、さまざまな状態を切り替えることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f1b0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1f1b0-106">Header file:</span></span>  <br/> |<span data-ttu-id="1f1b0-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="1f1b0-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="1f1b0-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="1f1b0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="1f1b0-109">メッセージオブジェクトを保持する</span><span class="sxs-lookup"><span data-stu-id="1f1b0-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="1f1b0-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="1f1b0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="1f1b0-111">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="1f1b0-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="1f1b0-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="1f1b0-112">Called by:</span></span>  <br/> |<span data-ttu-id="1f1b0-113">フォームビューアー</span><span class="sxs-lookup"><span data-stu-id="1f1b0-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="1f1b0-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="1f1b0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1f1b0-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="1f1b0-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="1f1b0-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="1f1b0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="1f1b0-117">lppersistmessage</span><span class="sxs-lookup"><span data-stu-id="1f1b0-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1f1b0-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="1f1b0-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1f1b0-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="1f1b0-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="1f1b0-120">form オブジェクトの前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="1f1b0-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="1f1b0-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="1f1b0-122">フォームを管理できるフォームサーバーを表す識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="1f1b0-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="1f1b0-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="1f1b0-124">前回の保存以降に加えられた変更について、フォームをチェックします。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="1f1b0-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="1f1b0-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="1f1b0-126">新しいメッセージを初期化します。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="1f1b0-127">Load</span><span class="sxs-lookup"><span data-stu-id="1f1b0-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="1f1b0-128">指定したメッセージのフォームを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="1f1b0-129">Save</span><span class="sxs-lookup"><span data-stu-id="1f1b0-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="1f1b0-130">変更したフォームを、読み込みまたは作成されたメッセージに保存し直します。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="1f1b0-131">SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="1f1b0-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="1f1b0-132">保存操作が完了したことをフォームに通知します。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="1f1b0-133">「soffmessage」</span><span class="sxs-lookup"><span data-stu-id="1f1b0-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="1f1b0-134">フォームに現在のメッセージを解放させます。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f1b0-135">解説</span><span class="sxs-lookup"><span data-stu-id="1f1b0-135">Remarks</span></span>

<span data-ttu-id="1f1b0-136">**IPersistMessage**インターフェイスを実装するには、すべてのフォームが必要です。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="1f1b0-137">**IPersistMessage**は、OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)インターフェイスと同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="1f1b0-138">詳細については、 **IPersistStorage**メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1f1b0-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f1b0-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f1b0-139">See also</span></span>



[<span data-ttu-id="1f1b0-140">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="1f1b0-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

