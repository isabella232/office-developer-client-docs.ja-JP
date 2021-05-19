---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419647"
---
# <a name="imapiprogress--iunknown"></a><span data-ttu-id="57f15-103">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="57f15-103">IMAPIProgress : IUnknown</span></span>

  
  
<span data-ttu-id="57f15-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57f15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57f15-105">進行状況インジケーターをクライアント アプリケーションに提供する進行状況オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="57f15-105">Implements a progress object that provides client applications with a progress indicator.</span></span> <span data-ttu-id="57f15-106">進行状況インジケーターは、メッセージ ストア間のフォルダーのコピーなど、操作の完了率を示すユーザー インターフェイス表示です。</span><span class="sxs-lookup"><span data-stu-id="57f15-106">A progress indicator is a user-interface display that shows the percentage of completion of an operation, such as copying folders between message stores.</span></span> <span data-ttu-id="57f15-107">MAPI およびクライアント アプリケーションは進行状況オブジェクトを実装し、サービス プロバイダーはそれらを使用します。</span><span class="sxs-lookup"><span data-stu-id="57f15-107">MAPI and client applications implement progress objects and service providers use them.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57f15-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="57f15-108">Header file:</span></span>  <br/> |<span data-ttu-id="57f15-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57f15-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="57f15-110">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="57f15-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="57f15-111">進行状況オブジェクト</span><span class="sxs-lookup"><span data-stu-id="57f15-111">Progress objects</span></span>  <br/> |
|<span data-ttu-id="57f15-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="57f15-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="57f15-113">MAPI およびクライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="57f15-113">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="57f15-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="57f15-114">Called by:</span></span>  <br/> |<span data-ttu-id="57f15-115">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="57f15-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="57f15-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="57f15-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="57f15-117">IID_IMAPIProgress</span><span class="sxs-lookup"><span data-stu-id="57f15-117">IID_IMAPIProgress</span></span>  <br/> |
|<span data-ttu-id="57f15-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="57f15-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="57f15-119">LPMAPIPROGRESS</span><span class="sxs-lookup"><span data-stu-id="57f15-119">LPMAPIPROGRESS</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="57f15-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="57f15-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="57f15-121">進行状況</span><span class="sxs-lookup"><span data-stu-id="57f15-121">Progress</span></span>](imapiprogress-progress.md) <br/> |<span data-ttu-id="57f15-122">進行状況インジケーターを更新し、操作の完了に向けて進行状況を表示します。</span><span class="sxs-lookup"><span data-stu-id="57f15-122">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span>  <br/> |
|[<span data-ttu-id="57f15-123">GetFlags</span><span class="sxs-lookup"><span data-stu-id="57f15-123">GetFlags</span></span>](imapiprogress-getflags.md) <br/> |<span data-ttu-id="57f15-124">進行状況の情報を計算する操作レベルの進行状況オブジェクトからフラグ設定を返します。</span><span class="sxs-lookup"><span data-stu-id="57f15-124">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>  <br/> |
|[<span data-ttu-id="57f15-125">GetMax</span><span class="sxs-lookup"><span data-stu-id="57f15-125">GetMax</span></span>](imapiprogress-getmax.md) <br/> |<span data-ttu-id="57f15-126">進行状況情報が表示される操作内のアイテムの最大数を返します。</span><span class="sxs-lookup"><span data-stu-id="57f15-126">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="57f15-127">GetMin</span><span class="sxs-lookup"><span data-stu-id="57f15-127">GetMin</span></span>](imapiprogress-getmin.md) <br/> |<span data-ttu-id="57f15-128">進行状況情報が表示される [SetLimits](imapiprogress-setlimits.md) メソッドの最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="57f15-128">Returns the minimum value in the [SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="57f15-129">SetLimits</span><span class="sxs-lookup"><span data-stu-id="57f15-129">SetLimits</span></span>](imapiprogress-setlimits.md) <br/> |<span data-ttu-id="57f15-130">操作のアイテム数の下限と上限、および操作の進行状況情報の計算方法を制御するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="57f15-130">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57f15-131">注釈</span><span class="sxs-lookup"><span data-stu-id="57f15-131">Remarks</span></span>

<span data-ttu-id="57f15-132">MAPI には、潜在的に長い操作を実行する多くのメソッドに  _lpProgress_ パラメーターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="57f15-132">MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.</span></span>  <span data-ttu-id="57f15-133">_lpProgress は_ 、進行状況オブジェクトのクライアント実装を示しています。</span><span class="sxs-lookup"><span data-stu-id="57f15-133">_lpProgress_ points to a client implementation of a progress object.</span></span> <span data-ttu-id="57f15-134">**IMAPIProgress インターフェイスを実装する** クライアントは、実装を指すこのパラメーターを設定します。**IMAPIProgress を実装しないクライアントは、** パラメーターを NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="57f15-134">Clients that implement the **IMAPIProgress** interface set this parameter to point to their implementation; clients that do not implement **IMAPIProgress** set the parameter to NULL.</span></span> <span data-ttu-id="57f15-135">操作の処理中に進行状況インジケーターを表示するには、サービス プロバイダーは、クライアントによって提供される進行状況オブジェクト (使用可能な場合)、または MAPI 実装  _(lpProgress が_ NULL に設定されている場合に示される) を使用します。</span><span class="sxs-lookup"><span data-stu-id="57f15-135">To display a progress indicator during processing of the operation, service providers use the progress object supplied by the client, if available, or a MAPI implementation (indicated when  _lpProgress_ is set to NULL).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="57f15-136">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="57f15-136">MFCMAPI reference</span></span>

<span data-ttu-id="57f15-137">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57f15-137">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="57f15-138">**Files**</span><span class="sxs-lookup"><span data-stu-id="57f15-138">**Files**</span></span>|<span data-ttu-id="57f15-139">**関数**</span><span class="sxs-lookup"><span data-stu-id="57f15-139">**Function**</span></span>|<span data-ttu-id="57f15-140">**コメント**</span><span class="sxs-lookup"><span data-stu-id="57f15-140">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="57f15-141">MapiProgress.h と MapiProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="57f15-141">MapiProgress.h and MapiProgress.cpp</span></span>  <br/> |<span data-ttu-id="57f15-142">該当なし</span><span class="sxs-lookup"><span data-stu-id="57f15-142">Not applicable</span></span>  <br/> |<span data-ttu-id="57f15-143">IMAPIProgresss 設定が有効になっている場合、MFCMAPI は、実装を受け入れる MFCMAPI が呼び出すすべての関数に **IMAPIProgress** 実装を渡します。</span><span class="sxs-lookup"><span data-stu-id="57f15-143">If the IMAPIProgress setting is enabled, MFCMAPI will pass an **IMAPIProgress** implementation to all functions that MFCMAPI invokes that accept an implementation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57f15-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="57f15-144">See also</span></span>



<span data-ttu-id="57f15-145">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="57f15-145">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="57f15-146">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="57f15-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

