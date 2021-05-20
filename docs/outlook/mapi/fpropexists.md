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
# <a name="fpropexists"></a><span data-ttu-id="06404-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="06404-103">FPropExists</span></span>

  
  
<span data-ttu-id="06404-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06404-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06404-105">[IMAPIProp](imapipropiunknown.md)インターフェイスまたは [IMessage](imessageimapiprop.md)や **IMAPIFolder などの IMAPIProp** から派生したインターフェイスで、特定のプロパティ タグ [を検索します](imapifolderimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="06404-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06404-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="06404-106">Header file:</span></span>  <br/> |<span data-ttu-id="06404-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="06404-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="06404-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="06404-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="06404-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="06404-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="06404-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="06404-110">Called by:</span></span>  <br/> |<span data-ttu-id="06404-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="06404-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="06404-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="06404-112">Parameters</span></span>

 <span data-ttu-id="06404-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="06404-113">_pobj_</span></span>
  
> <span data-ttu-id="06404-114">[in]プロパティ タグを **検索する IMAPIProp** から派生した **IMAPIProp** インターフェイスまたはインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="06404-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="06404-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="06404-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="06404-116">[in]検索するプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="06404-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="06404-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="06404-117">Return value</span></span>

<span data-ttu-id="06404-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="06404-118">TRUE</span></span> 
  
> <span data-ttu-id="06404-119">指定されたプロパティ タグの一致が見つかりました。</span><span class="sxs-lookup"><span data-stu-id="06404-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="06404-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="06404-120">FALSE</span></span> 
  
> <span data-ttu-id="06404-121">指定されたプロパティ タグの一致が見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="06404-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="06404-122">注釈</span><span class="sxs-lookup"><span data-stu-id="06404-122">Remarks</span></span>

<span data-ttu-id="06404-123">_ulPropTag_ パラメーターのプロパティ タグに型 PT_UNSPECIFIED がある場合 **、FPropExists** 関数はプロパティ識別子にのみ基づいて一致を検索します。</span><span class="sxs-lookup"><span data-stu-id="06404-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="06404-124">それ以外の場合は、型を含むプロパティ タグ全体が一致します。</span><span class="sxs-lookup"><span data-stu-id="06404-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

