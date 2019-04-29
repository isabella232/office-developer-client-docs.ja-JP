---
title: imapisupportcompletemsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411191"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="e8a51-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="e8a51-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="e8a51-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8a51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8a51-105">メッセージに対して後処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8a51-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e8a51-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e8a51-106">Parameters</span></span>

 <span data-ttu-id="e8a51-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e8a51-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e8a51-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="e8a51-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e8a51-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e8a51-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="e8a51-110">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="e8a51-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e8a51-111">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="e8a51-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="e8a51-112">順番処理するメッセージのエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8a51-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8a51-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="e8a51-113">Return value</span></span>

<span data-ttu-id="e8a51-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8a51-114">S_OK</span></span> 
  
> <span data-ttu-id="e8a51-115">後処理が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="e8a51-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8a51-116">注釈</span><span class="sxs-lookup"><span data-stu-id="e8a51-116">Remarks</span></span>

<span data-ttu-id="e8a51-117">**imapisupport::** "は、メッセージストアプロバイダーのサポートオブジェクトに対して実装されており、トランスポートプロバイダーと密接に結合されたメッセージストアプロバイダーのみが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e8a51-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="e8a51-118">密結合ストアプロバイダーは、メッセージをポスト処理するように MAPI スプーラーに指示する**imapisupport:: completemsg**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e8a51-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e8a51-119">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e8a51-119">Notes to callers</span></span>

<span data-ttu-id="e8a51-120">呼び出し\*\*\*\* の待機は、トランスポートプロバイダーに密接に結合している場合にのみ、すべてのメッセージの受信者を処理でき、次の条件のいずれかが存在することになります。</span><span class="sxs-lookup"><span data-stu-id="e8a51-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="e8a51-121">メッセージが前処理されました。</span><span class="sxs-lookup"><span data-stu-id="e8a51-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="e8a51-122">このメッセージには、MAPI スプーラーによる後処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="e8a51-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8a51-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8a51-123">See also</span></span>



[<span data-ttu-id="e8a51-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8a51-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

