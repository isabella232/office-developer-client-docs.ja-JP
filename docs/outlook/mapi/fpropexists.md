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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ccfb503f62ef039700f79cd8852883685f329dfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800123"
---
# <a name="fpropexists"></a><span data-ttu-id="57429-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="57429-103">FPropExists</span></span>

  
  
<span data-ttu-id="57429-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="57429-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="57429-105">**IMAPIProp**、 [IMessage](imessageimapiprop.md)や[IMAPIFolder](imapifolderimapicontainer.md)などから派生した[IMAPIProp](imapipropiunknown.md)インターフェイスまたはインターフェイスの指定されたプロパティ タグを検索します。</span><span class="sxs-lookup"><span data-stu-id="57429-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57429-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="57429-106">Header file:</span></span>  <br/> |<span data-ttu-id="57429-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="57429-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="57429-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="57429-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="57429-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="57429-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="57429-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="57429-110">Called by:</span></span>  <br/> |<span data-ttu-id="57429-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="57429-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="57429-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="57429-112">Parameters</span></span>

 <span data-ttu-id="57429-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="57429-113">_pobj_</span></span>
  
> <span data-ttu-id="57429-114">[in]**IMAPIProp**インターフェイス内のプロパティ タグを検索する**IMAPIProp**から派生したインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="57429-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="57429-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="57429-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="57429-116">[in]検索するプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="57429-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57429-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="57429-117">Return value</span></span>

<span data-ttu-id="57429-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="57429-118">TRUE</span></span> 
  
> <span data-ttu-id="57429-119">指定されたプロパティ タグの一致が見つかりました。</span><span class="sxs-lookup"><span data-stu-id="57429-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="57429-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="57429-120">FALSE</span></span> 
  
> <span data-ttu-id="57429-121">指定されたプロパティ タグの一致は見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="57429-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57429-122">備考</span><span class="sxs-lookup"><span data-stu-id="57429-122">Remarks</span></span>

<span data-ttu-id="57429-123">型 PT_UNSPECIFIED、 _ulPropTag_パラメーターのプロパティ タグの場合、 **FPropExists**関数は、プロパティの識別子にのみ基づいて一致するを探します。</span><span class="sxs-lookup"><span data-stu-id="57429-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="57429-124">それ以外の場合、一致が、型を含め、全体のプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="57429-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

