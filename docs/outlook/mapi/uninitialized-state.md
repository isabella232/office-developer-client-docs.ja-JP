---
title: Uninitialized 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 95ed80a6d0ea6a6a7c8cc768b32981ac899b69e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578249"
---
# <a name="uninitialized-state"></a><span data-ttu-id="f4b84-103">Uninitialized 状態</span><span class="sxs-lookup"><span data-stu-id="f4b84-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="f4b84-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4b84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4b84-105">初期化されていない状態は、オブジェクトが最初に作成されたときにする必要があります初期状態のフォームです。</span><span class="sxs-lookup"><span data-stu-id="f4b84-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="f4b84-106">フォーム オブジェクトは、クライアント アプリケーションは、フォーム オブジェクトの[IPersistMessage::InitNew](ipersistmessage-initnew.md)または[IPersistMessage::Load](ipersistmessage-load.md)メソッドを呼び出すと、メッセージ データで初期化になります。</span><span class="sxs-lookup"><span data-stu-id="f4b84-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="f4b84-107">次の表では、Unitialized の状態から有効な遷移について説明します。</span><span class="sxs-lookup"><span data-stu-id="f4b84-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="f4b84-108">**IPersistMessage メソッド**</span><span class="sxs-lookup"><span data-stu-id="f4b84-108">**IPersistMessage method**</span></span>|<span data-ttu-id="f4b84-109">**操作**</span><span class="sxs-lookup"><span data-stu-id="f4b84-109">**Action**</span></span>|<span data-ttu-id="f4b84-110">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="f4b84-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f4b84-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="f4b84-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="f4b84-112">フォーム オブジェクトに既定のデータをロードします。</span><span class="sxs-lookup"><span data-stu-id="f4b84-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="f4b84-113">Normal</span><span class="sxs-lookup"><span data-stu-id="f4b84-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="f4b84-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="f4b84-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="f4b84-115">移行先のメッセージには、フォーム オブジェクトにデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="f4b84-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="f4b84-116">Normal</span><span class="sxs-lookup"><span data-stu-id="f4b84-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="f4b84-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="f4b84-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="f4b84-118">成功した場合、または最後のエラーに設定を返し、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="f4b84-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="f4b84-119">初期化されていません</span><span class="sxs-lookup"><span data-stu-id="f4b84-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="f4b84-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f4b84-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="f4b84-121">最後のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="f4b84-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="f4b84-122">初期化されていません</span><span class="sxs-lookup"><span data-stu-id="f4b84-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="f4b84-123">他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたはその他のインターフェイスのメソッド</span><span class="sxs-lookup"><span data-stu-id="f4b84-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="f4b84-124">最後のエラーを設定、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="f4b84-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="f4b84-125">初期化されていません</span><span class="sxs-lookup"><span data-stu-id="f4b84-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4b84-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f4b84-126">See also</span></span>



[<span data-ttu-id="f4b84-127">Normal 状態</span><span class="sxs-lookup"><span data-stu-id="f4b84-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="f4b84-128">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="f4b84-128">Form States</span></span>](form-states.md)

