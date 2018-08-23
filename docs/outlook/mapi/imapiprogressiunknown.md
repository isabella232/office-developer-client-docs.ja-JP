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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 975c01457515a400d1d442fedc432dc000f06665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800651"
---
# <a name="imapiprogress--iunknown"></a><span data-ttu-id="9c7d5-103">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c7d5-103">IMAPIProgress : IUnknown</span></span>

  
  
<span data-ttu-id="9c7d5-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c7d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c7d5-105">進行状況インジケーターが表示されて、クライアント アプリケーションを提供する進行中のオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-105">Implements a progress object that provides client applications with a progress indicator.</span></span> <span data-ttu-id="9c7d5-106">進行状況のインジケーターは、メッセージ ストア間でフォルダーをコピーするなど、操作の完了の割合が表示されるユーザー インターフェイスの表示です。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-106">A progress indicator is a user-interface display that shows the percentage of completion of an operation, such as copying folders between message stores.</span></span> <span data-ttu-id="9c7d5-107">MAPI およびクライアント アプリケーションが実行中オブジェクトを実装し、サービス ・ プロバイダーを使用しています。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-107">MAPI and client applications implement progress objects and service providers use them.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c7d5-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9c7d5-108">Header file:</span></span>  <br/> |<span data-ttu-id="9c7d5-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c7d5-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9c7d5-110">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="9c7d5-111">オブジェクトの進行状況</span><span class="sxs-lookup"><span data-stu-id="9c7d5-111">Progress objects</span></span>  <br/> |
|<span data-ttu-id="9c7d5-112">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="9c7d5-113">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="9c7d5-113">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="9c7d5-114">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-114">Called by:</span></span>  <br/> |<span data-ttu-id="9c7d5-115">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="9c7d5-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="9c7d5-116">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9c7d5-117">IID_IMAPIProgress</span><span class="sxs-lookup"><span data-stu-id="9c7d5-117">IID_IMAPIProgress</span></span>  <br/> |
|<span data-ttu-id="9c7d5-118">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="9c7d5-119">LPMAPIPROGRESS</span><span class="sxs-lookup"><span data-stu-id="9c7d5-119">LPMAPIPROGRESS</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9c7d5-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="9c7d5-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9c7d5-121">Progress</span><span class="sxs-lookup"><span data-stu-id="9c7d5-121">Progress</span></span>](imapiprogress-progress.md) <br/> |<span data-ttu-id="9c7d5-122">加えられると、操作の完了までの進捗状況の表示と進行状況のインジケーターが更新されます。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-122">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span>  <br/> |
|[<span data-ttu-id="9c7d5-123">GetFlags</span><span class="sxs-lookup"><span data-stu-id="9c7d5-123">GetFlags</span></span>](imapiprogress-getflags.md) <br/> |<span data-ttu-id="9c7d5-124">返します。 操作の進行状況に関する情報は、計算対象のレベルに進行中のオブジェクトから設定にフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-124">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>  <br/> |
|[<span data-ttu-id="9c7d5-125">GetMax</span><span class="sxs-lookup"><span data-stu-id="9c7d5-125">GetMax</span></span>](imapiprogress-getmax.md) <br/> |<span data-ttu-id="9c7d5-126">情報を表示する進行中の操作では、アイテムの最大数を返します。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-126">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="9c7d5-127">GetMin</span><span class="sxs-lookup"><span data-stu-id="9c7d5-127">GetMin</span></span>](imapiprogress-getmin.md) <br/> |<span data-ttu-id="9c7d5-128">進捗状況の情報が表示されます、 [SetLimits](imapiprogress-setlimits.md)メソッドでは、最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-128">Returns the minimum value in the [SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="9c7d5-129">SetLimits</span><span class="sxs-lookup"><span data-stu-id="9c7d5-129">SetLimits</span></span>](imapiprogress-setlimits.md) <br/> |<span data-ttu-id="9c7d5-130">操作、および操作の進行状況の情報を計算する方法を制御するフラグでは、アイテム数の上限と下限の制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-130">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c7d5-131">注釈</span><span class="sxs-lookup"><span data-stu-id="9c7d5-131">Remarks</span></span>

<span data-ttu-id="9c7d5-132">MAPI には、時間のかかる可能性のある操作を実行するメソッドの多くに、 _lpProgress_パラメーターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-132">MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.</span></span>  <span data-ttu-id="9c7d5-133">_lpProgress_は、実行中のオブジェクトのクライアントの実装を示しています。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-133">_lpProgress_ points to a client implementation of a progress object.</span></span> <span data-ttu-id="9c7d5-134">**IMAPIProgress**インターフェイスを実装するクライアントは、それぞれの実装を指すには、このパラメーターを設定します。**IMAPIProgress**を実装していないクライアントは、パラメーターを NULL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-134">Clients that implement the **IMAPIProgress** interface set this parameter to point to their implementation; clients that do not implement **IMAPIProgress** set the parameter to NULL.</span></span> <span data-ttu-id="9c7d5-135">操作の処理中に進行状況のインジケーターを表示するには、サービス プロバイダーは、可能な場合は、クライアントによって提供される進行中のオブジェクトまたは MAPI 実装では、( _lpProgress_は NULL に設定するときに示されます) を使用します。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-135">To display a progress indicator during processing of the operation, service providers use the progress object supplied by the client, if available, or a MAPI implementation (indicated when  _lpProgress_ is set to NULL).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9c7d5-136">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="9c7d5-136">MFCMAPI reference</span></span>

<span data-ttu-id="9c7d5-137">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="9c7d5-137">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9c7d5-138">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="9c7d5-138">**Files**</span></span>|<span data-ttu-id="9c7d5-139">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="9c7d5-139">**Function**</span></span>|<span data-ttu-id="9c7d5-140">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="9c7d5-140">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9c7d5-141">MapiProgress.h と MapiProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="9c7d5-141">MapiProgress.h and MapiProgress.cpp</span></span>  <br/> |<span data-ttu-id="9c7d5-142">該当なし</span><span class="sxs-lookup"><span data-stu-id="9c7d5-142">Not applicable</span></span>  <br/> |<span data-ttu-id="9c7d5-143">IMAPIProgress の設定を有効にすると、MFCMAPI 通過**IMAPIProgress**実装すべての関数 MFCMAPI を起動するに実装を受け入れることにします。</span><span class="sxs-lookup"><span data-stu-id="9c7d5-143">If the IMAPIProgress setting is enabled, MFCMAPI will pass an **IMAPIProgress** implementation to all functions that MFCMAPI invokes that accept an implementation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c7d5-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c7d5-144">See also</span></span>



<span data-ttu-id="9c7d5-145">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9c7d5-145">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="9c7d5-146">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9c7d5-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

