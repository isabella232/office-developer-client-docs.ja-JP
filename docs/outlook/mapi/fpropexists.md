---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429489"
---
# <a name="fpropexists"></a><span data-ttu-id="61bca-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="61bca-103">FPropExists</span></span>

  
  
<span data-ttu-id="61bca-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61bca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61bca-105">[imapiprop](imapipropiunknown.md)インターフェイス内の指定されたプロパティタグ、または**imapiprop**( [IMessage](imessageimapiprop.md)や[imapiprop](imapifolderimapicontainer.md)など) から派生したインターフェイスを検索します。</span><span class="sxs-lookup"><span data-stu-id="61bca-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61bca-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="61bca-106">Header file:</span></span>  <br/> |<span data-ttu-id="61bca-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="61bca-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="61bca-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="61bca-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="61bca-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="61bca-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="61bca-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="61bca-110">Called by:</span></span>  <br/> |<span data-ttu-id="61bca-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="61bca-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="61bca-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="61bca-112">Parameters</span></span>

 <span data-ttu-id="61bca-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="61bca-113">_pobj_</span></span>
  
> <span data-ttu-id="61bca-114">順番プロパティタグを検索する**imapiprop**から派生した**imapiprop**インターフェイスまたはインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="61bca-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="61bca-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="61bca-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="61bca-116">順番検索するプロパティタグを指定します。</span><span class="sxs-lookup"><span data-stu-id="61bca-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="61bca-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="61bca-117">Return value</span></span>

<span data-ttu-id="61bca-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="61bca-118">TRUE</span></span> 
  
> <span data-ttu-id="61bca-119">指定したプロパティタグに一致するものが見つかりました。</span><span class="sxs-lookup"><span data-stu-id="61bca-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="61bca-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="61bca-120">FALSE</span></span> 
  
> <span data-ttu-id="61bca-121">指定されたプロパティタグに一致するものが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="61bca-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61bca-122">注釈</span><span class="sxs-lookup"><span data-stu-id="61bca-122">Remarks</span></span>

<span data-ttu-id="61bca-123">_ulPropTag_パラメーターの property タグに type PT_UNSPECIFIED が指定されている場合、 **fpropexists**関数は、プロパティ識別子のみに基づいて一致を検索します。</span><span class="sxs-lookup"><span data-stu-id="61bca-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="61bca-124">それ以外の場合は、型を含むプロパティタグ全体の一致が照合されます。</span><span class="sxs-lookup"><span data-stu-id="61bca-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

