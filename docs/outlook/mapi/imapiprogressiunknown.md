---
title: imapiprogress IUnknown
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
# <a name="imapiprogress--iunknown"></a><span data-ttu-id="d27eb-103">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d27eb-103">IMAPIProgress : IUnknown</span></span>

  
  
<span data-ttu-id="d27eb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d27eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d27eb-105">クライアントアプリケーションに進行状況のインジケーターを提供する progress オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="d27eb-105">Implements a progress object that provides client applications with a progress indicator.</span></span> <span data-ttu-id="d27eb-106">進行状況インジケーターは、メッセージストア間でフォルダーをコピーするなど、操作の完了の割合を示すユーザーインターフェイスの表示です。</span><span class="sxs-lookup"><span data-stu-id="d27eb-106">A progress indicator is a user-interface display that shows the percentage of completion of an operation, such as copying folders between message stores.</span></span> <span data-ttu-id="d27eb-107">MAPI およびクライアントアプリケーションは、進行状況オブジェクトを実装し、サービスプロバイダーはそれらを使用します。</span><span class="sxs-lookup"><span data-stu-id="d27eb-107">MAPI and client applications implement progress objects and service providers use them.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d27eb-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d27eb-108">Header file:</span></span>  <br/> |<span data-ttu-id="d27eb-109">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d27eb-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d27eb-110">公開者:</span><span class="sxs-lookup"><span data-stu-id="d27eb-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="d27eb-111">進行状況オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d27eb-111">Progress objects</span></span>  <br/> |
|<span data-ttu-id="d27eb-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="d27eb-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="d27eb-113">MAPI およびクライアントアプリケーション</span><span class="sxs-lookup"><span data-stu-id="d27eb-113">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="d27eb-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d27eb-114">Called by:</span></span>  <br/> |<span data-ttu-id="d27eb-115">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="d27eb-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="d27eb-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="d27eb-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d27eb-117">IID_IMAPIProgress</span><span class="sxs-lookup"><span data-stu-id="d27eb-117">IID_IMAPIProgress</span></span>  <br/> |
|<span data-ttu-id="d27eb-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="d27eb-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="d27eb-119">LPMAPIPROGRESS</span><span class="sxs-lookup"><span data-stu-id="d27eb-119">LPMAPIPROGRESS</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d27eb-120">v の順序</span><span class="sxs-lookup"><span data-stu-id="d27eb-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d27eb-121">進行状況</span><span class="sxs-lookup"><span data-stu-id="d27eb-121">Progress</span></span>](imapiprogress-progress.md) <br/> |<span data-ttu-id="d27eb-122">操作が完了した時点で進行状況のインジケーターを更新します。</span><span class="sxs-lookup"><span data-stu-id="d27eb-122">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span>  <br/> |
|[<span data-ttu-id="d27eb-123">getflags</span><span class="sxs-lookup"><span data-stu-id="d27eb-123">GetFlags</span></span>](imapiprogress-getflags.md) <br/> |<span data-ttu-id="d27eb-124">進行状況の情報を計算する操作のレベルについて、progress オブジェクトからフラグ設定を返します。</span><span class="sxs-lookup"><span data-stu-id="d27eb-124">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>  <br/> |
|[<span data-ttu-id="d27eb-125">getmax</span><span class="sxs-lookup"><span data-stu-id="d27eb-125">GetMax</span></span>](imapiprogress-getmax.md) <br/> |<span data-ttu-id="d27eb-126">進行状況の情報が表示される操作内のアイテムの最大数を返します。</span><span class="sxs-lookup"><span data-stu-id="d27eb-126">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d27eb-127">GetMin</span><span class="sxs-lookup"><span data-stu-id="d27eb-127">GetMin</span></span>](imapiprogress-getmin.md) <br/> |<span data-ttu-id="d27eb-128">プログレス情報が表示される[setlimits](imapiprogress-setlimits.md)メソッドの最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="d27eb-128">Returns the minimum value in the [SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d27eb-129">SetLimits</span><span class="sxs-lookup"><span data-stu-id="d27eb-129">SetLimits</span></span>](imapiprogress-setlimits.md) <br/> |<span data-ttu-id="d27eb-130">操作内の項目数の下限と上限を設定します。また、操作の進行状況に関する情報の計算方法を制御するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="d27eb-130">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d27eb-131">注釈</span><span class="sxs-lookup"><span data-stu-id="d27eb-131">Remarks</span></span>

<span data-ttu-id="d27eb-132">MAPI には、潜在的に長い時間がかかる操作を実行する多くのメソッドの_lpprogress_パラメーターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d27eb-132">MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.</span></span>  <span data-ttu-id="d27eb-133">_lpprogress_は、progress オブジェクトのクライアント実装を指します。</span><span class="sxs-lookup"><span data-stu-id="d27eb-133">_lpProgress_ points to a client implementation of a progress object.</span></span> <span data-ttu-id="d27eb-134">**imapiprogress**インターフェイスを実装するクライアントは、その実装をポイントするようにこのパラメーターを設定します。**imapiprogress**を実装していないクライアントは、パラメーターを NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="d27eb-134">Clients that implement the **IMAPIProgress** interface set this parameter to point to their implementation; clients that do not implement **IMAPIProgress** set the parameter to NULL.</span></span> <span data-ttu-id="d27eb-135">操作の処理中に進行状況インジケーターを表示するために、サービスプロバイダーは、クライアントによって提供される進行状況オブジェクト (使用可能な場合) または MAPI 実装 ( _lpprogress_が NULL に設定されている場合) を使用します。</span><span class="sxs-lookup"><span data-stu-id="d27eb-135">To display a progress indicator during processing of the operation, service providers use the progress object supplied by the client, if available, or a MAPI implementation (indicated when  _lpProgress_ is set to NULL).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d27eb-136">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="d27eb-136">MFCMAPI reference</span></span>

<span data-ttu-id="d27eb-137">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d27eb-137">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d27eb-138">**Files**</span><span class="sxs-lookup"><span data-stu-id="d27eb-138">**Files**</span></span>|<span data-ttu-id="d27eb-139">**関数**</span><span class="sxs-lookup"><span data-stu-id="d27eb-139">**Function**</span></span>|<span data-ttu-id="d27eb-140">**コメント**</span><span class="sxs-lookup"><span data-stu-id="d27eb-140">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d27eb-141">MapiProgress および MapiProgress</span><span class="sxs-lookup"><span data-stu-id="d27eb-141">MapiProgress.h and MapiProgress.cpp</span></span>  <br/> |<span data-ttu-id="d27eb-142">該当しない</span><span class="sxs-lookup"><span data-stu-id="d27eb-142">Not applicable</span></span>  <br/> |<span data-ttu-id="d27eb-143">imapiprogress 設定が有効になっている場合、mfcmapi は、すべての関数に**imapiprogress**実装を渡します。この実装は、mfcmapi が呼び出す実装を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="d27eb-143">If the IMAPIProgress setting is enabled, MFCMAPI will pass an **IMAPIProgress** implementation to all functions that MFCMAPI invokes that accept an implementation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d27eb-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="d27eb-144">See also</span></span>



<span data-ttu-id="d27eb-145">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="d27eb-145">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="d27eb-146">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="d27eb-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

