---
title: 初期化されていない状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425562"
---
# <a name="uninitialized-state"></a><span data-ttu-id="ad9c2-103">初期化されていない状態</span><span class="sxs-lookup"><span data-stu-id="ad9c2-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="ad9c2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad9c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad9c2-105">初期化されていない状態は、最初に作成する際にオブジェクトが最初に含む必要がある初期状態のフォーム オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="ad9c2-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="ad9c2-106">クライアント アプリケーションがフォーム オブジェクトの [IPersistMessage::InitNew](ipersistmessage-initnew.md) または [IPersistMessage::Load](ipersistmessage-load.md) メソッドを呼び出す場合、フォーム オブジェクトはメッセージ データで初期化されます。</span><span class="sxs-lookup"><span data-stu-id="ad9c2-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="ad9c2-107">次の表では、Unitialized 状態からの許可された移行について説明します。</span><span class="sxs-lookup"><span data-stu-id="ad9c2-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="ad9c2-108">**IPersistMessage メソッド**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-108">**IPersistMessage method**</span></span>|<span data-ttu-id="ad9c2-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-109">**Action**</span></span>|<span data-ttu-id="ad9c2-110">**新しい状態**</span><span class="sxs-lookup"><span data-stu-id="ad9c2-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad9c2-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="ad9c2-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="ad9c2-112">既定のデータを使用してフォーム オブジェクトを読み込む。</span><span class="sxs-lookup"><span data-stu-id="ad9c2-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="ad9c2-113">Normal</span><span class="sxs-lookup"><span data-stu-id="ad9c2-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="ad9c2-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="ad9c2-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="ad9c2-115">ターゲット メッセージのデータを含むフォーム オブジェクトを読み込む。</span><span class="sxs-lookup"><span data-stu-id="ad9c2-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="ad9c2-116">標準</span><span class="sxs-lookup"><span data-stu-id="ad9c2-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="ad9c2-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="ad9c2-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="ad9c2-118">成功を返す、または最後のエラーをに設定し、E_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="ad9c2-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="ad9c2-119">初期化されていません</span><span class="sxs-lookup"><span data-stu-id="ad9c2-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="ad9c2-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ad9c2-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="ad9c2-121">最後のエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="ad9c2-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="ad9c2-122">初期化されていません</span><span class="sxs-lookup"><span data-stu-id="ad9c2-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="ad9c2-123">その [他の IPersistMessage : 他のインターフェイスからの IUnknown](ipersistmessageiunknown.md) メソッドまたはメソッド</span><span class="sxs-lookup"><span data-stu-id="ad9c2-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="ad9c2-124">最後のエラーを設定し、エラーを返E_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="ad9c2-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="ad9c2-125">初期化されていません</span><span class="sxs-lookup"><span data-stu-id="ad9c2-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad9c2-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad9c2-126">See also</span></span>



[<span data-ttu-id="ad9c2-127">標準状態</span><span class="sxs-lookup"><span data-stu-id="ad9c2-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="ad9c2-128">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="ad9c2-128">Form States</span></span>](form-states.md)

