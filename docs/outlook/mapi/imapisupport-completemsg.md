---
title: IMAPISupportCompleteMsg
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: db28d9684f1bb679ce36f99346f4ecc67a1a93e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800729"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="6bc34-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="6bc34-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="6bc34-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6bc34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6bc34-105">メッセージのポスト プロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="6bc34-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="6bc34-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="6bc34-106">Parameters</span></span>

 <span data-ttu-id="6bc34-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6bc34-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6bc34-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="6bc34-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6bc34-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6bc34-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="6bc34-110">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="6bc34-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6bc34-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6bc34-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="6bc34-112">[in]メッセージを処理するためのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6bc34-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6bc34-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6bc34-113">Return value</span></span>

<span data-ttu-id="6bc34-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="6bc34-114">S_OK</span></span> 
  
> <span data-ttu-id="6bc34-115">後処理が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="6bc34-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6bc34-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="6bc34-116">Remarks</span></span>

<span data-ttu-id="6bc34-117">**IMAPISupport::CompleteMsg**メソッドは、メッセージ ストア プロバイダーのサポートのオブジェクトに実装されており、トランスポート プロバイダーと緊密に結合されているメッセージ ストア プロバイダーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bc34-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="6bc34-118">密結合のストア プロバイダーは、メッセージをポスト プロセスに MAPI スプーラーに指示するために**IMAPISupport::CompleteMsg**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6bc34-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6bc34-119">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="6bc34-119">Notes to callers</span></span>

<span data-ttu-id="6bc34-120">トランスポート プロバイダーと密に結合する、すべてのメッセージの受信者を処理することができ、次の条件のいずれかが存在する場合にのみ、 **CompleteMsg**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6bc34-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="6bc34-121">メッセージをプリプロセスされました。</span><span class="sxs-lookup"><span data-stu-id="6bc34-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="6bc34-122">メッセージには、MAPI スプーラーによって後処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="6bc34-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6bc34-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="6bc34-123">See also</span></span>



[<span data-ttu-id="6bc34-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6bc34-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

