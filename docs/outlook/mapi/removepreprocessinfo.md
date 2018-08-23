---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c90b569414c1710cc1065fdb4fd72738e265ebff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588833"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="e8dd6-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="e8dd6-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="e8dd6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8dd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8dd6-105">削除は、メッセージから、 [PreprocessMessage](preprocessmessage.md)ベースの関数によって書き込まれた情報をプリプロセスします。</span><span class="sxs-lookup"><span data-stu-id="e8dd6-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8dd6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e8dd6-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8dd6-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="e8dd6-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="e8dd6-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="e8dd6-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e8dd6-109">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e8dd6-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="e8dd6-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e8dd6-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e8dd6-111">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="e8dd6-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="e8dd6-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e8dd6-112">Parameters</span></span>

 <span data-ttu-id="e8dd6-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="e8dd6-113">_lpMessage_</span></span>
  
> <span data-ttu-id="e8dd6-114">[in]削除する元となる情報は、プリプロセス済みのメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8dd6-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8dd6-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e8dd6-115">Return value</span></span>

<span data-ttu-id="e8dd6-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8dd6-116">S_OK</span></span>
  
> <span data-ttu-id="e8dd6-117">プリプロセス済みの情報が正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="e8dd6-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8dd6-118">注釈</span><span class="sxs-lookup"><span data-stu-id="e8dd6-118">Remarks</span></span>

<span data-ttu-id="e8dd6-119">MAPI スプーラーは、 **RemovePreprocessInfo**に基づく関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e8dd6-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="e8dd6-120">トランスポート プロバイダーは、同時並行の**PreprocessMessage**ベースの関数を登録するときに、 [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md)メソッドの呼び出しで**RemovePreprocessInfo**ベースの関数を登録します。</span><span class="sxs-lookup"><span data-stu-id="e8dd6-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="e8dd6-121">Fax 転送のための適切なレンダリング イメージは、 [PreprocessMessage](preprocessmessage.md)関数のプロトタイプで定義された関数が記述したプリプロセス済みの情報の例です。</span><span class="sxs-lookup"><span data-stu-id="e8dd6-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="e8dd6-122">通常、MAPI スプーラーは、プリプロセス済みの情報を含むメッセージを送信した後は**RemovePreprocessInfo**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e8dd6-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

