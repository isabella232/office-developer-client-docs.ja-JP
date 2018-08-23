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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ccfb503f62ef039700f79cd8852883685f329dfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800123"
---
# <a name="fpropexists"></a><span data-ttu-id="23a51-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="23a51-103">FPropExists</span></span>

  
  
<span data-ttu-id="23a51-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23a51-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23a51-105">**IMAPIProp**、 [IMessage](imessageimapiprop.md)や[IMAPIFolder](imapifolderimapicontainer.md)などから派生した[IMAPIProp](imapipropiunknown.md)インターフェイスまたはインターフェイスの指定されたプロパティ タグを検索します。</span><span class="sxs-lookup"><span data-stu-id="23a51-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23a51-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="23a51-106">Header file:</span></span>  <br/> |<span data-ttu-id="23a51-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="23a51-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="23a51-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="23a51-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="23a51-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="23a51-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="23a51-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="23a51-110">Called by:</span></span>  <br/> |<span data-ttu-id="23a51-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="23a51-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="23a51-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23a51-112">Parameters</span></span>

 <span data-ttu-id="23a51-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="23a51-113">_pobj_</span></span>
  
> <span data-ttu-id="23a51-114">[in]**IMAPIProp**インターフェイス内のプロパティ タグを検索する**IMAPIProp**から派生したインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="23a51-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="23a51-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="23a51-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="23a51-116">[in]検索するプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="23a51-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="23a51-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="23a51-117">Return value</span></span>

<span data-ttu-id="23a51-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="23a51-118">TRUE</span></span> 
  
> <span data-ttu-id="23a51-119">指定されたプロパティ タグの一致が見つかりました。</span><span class="sxs-lookup"><span data-stu-id="23a51-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="23a51-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="23a51-120">FALSE</span></span> 
  
> <span data-ttu-id="23a51-121">指定されたプロパティ タグの一致は見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="23a51-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="23a51-122">注釈</span><span class="sxs-lookup"><span data-stu-id="23a51-122">Remarks</span></span>

<span data-ttu-id="23a51-123">型 PT_UNSPECIFIED、 _ulPropTag_パラメーターのプロパティ タグの場合、 **FPropExists**関数は、プロパティの識別子にのみ基づいて一致するを探します。</span><span class="sxs-lookup"><span data-stu-id="23a51-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="23a51-124">それ以外の場合、一致が、型を含め、全体のプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="23a51-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

