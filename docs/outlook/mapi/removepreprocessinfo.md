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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432948"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="1929d-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="1929d-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="1929d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1929d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1929d-105">[PreprocessMessage](preprocessmessage.md)ベースの関数によって作成された前処理された情報をメッセージから削除します。</span><span class="sxs-lookup"><span data-stu-id="1929d-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1929d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1929d-106">Header file:</span></span>  <br/> |<span data-ttu-id="1929d-107">Mapispi</span><span class="sxs-lookup"><span data-stu-id="1929d-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="1929d-108">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="1929d-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="1929d-109">トランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="1929d-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="1929d-110">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="1929d-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="1929d-111">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="1929d-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="1929d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1929d-112">Parameters</span></span>

 <span data-ttu-id="1929d-113">_lpmessage_</span><span class="sxs-lookup"><span data-stu-id="1929d-113">_lpMessage_</span></span>
  
> <span data-ttu-id="1929d-114">順番削除する情報があるプリプロセスされたメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1929d-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1929d-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="1929d-115">Return value</span></span>

<span data-ttu-id="1929d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1929d-116">S_OK</span></span>
  
> <span data-ttu-id="1929d-117">前処理された情報が正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="1929d-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1929d-118">注釈</span><span class="sxs-lookup"><span data-stu-id="1929d-118">Remarks</span></span>

<span data-ttu-id="1929d-119">MAPI スプーラーは、 **removepreprocessinfo**に基づいて関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1929d-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="1929d-120">トランスポートプロバイダーは、 [imapisupport:: registerpreprocessor プロセッサ](imapisupport-registerpreprocessor.md)メソッドへの呼び出しで、並列**PreprocessMessage**ベースの関数を登録するのと同時に、 **removepreprocessinfo**に基づく関数を登録します。</span><span class="sxs-lookup"><span data-stu-id="1929d-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="1929d-121">[PreprocessMessage](preprocessmessage.md)関数プロトタイプによって定義された関数によって書き込まれたプリプロセスされた情報の例として、fax 送信に適したイメージレンダリングがあります。</span><span class="sxs-lookup"><span data-stu-id="1929d-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="1929d-122">MAPI スプーラーは、通常、前処理された情報を含むメッセージを送信した後に、 **removepreprocessinfo**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1929d-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

