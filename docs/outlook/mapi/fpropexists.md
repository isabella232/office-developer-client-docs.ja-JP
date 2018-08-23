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
ms.openlocfilehash: 0d016c83678d9c1c94ee4ad4b8e12723c03f7bda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570437"
---
# <a name="fpropexists"></a><span data-ttu-id="d205c-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="d205c-103">FPropExists</span></span>

  
  
<span data-ttu-id="d205c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d205c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d205c-105">**IMAPIProp**、 [IMessage](imessageimapiprop.md)や[IMAPIFolder](imapifolderimapicontainer.md)などから派生した[IMAPIProp](imapipropiunknown.md)インターフェイスまたはインターフェイスの指定されたプロパティ タグを検索します。</span><span class="sxs-lookup"><span data-stu-id="d205c-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d205c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d205c-106">Header file:</span></span>  <br/> |<span data-ttu-id="d205c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d205c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d205c-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="d205c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d205c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d205c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d205c-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d205c-110">Called by:</span></span>  <br/> |<span data-ttu-id="d205c-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="d205c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="d205c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d205c-112">Parameters</span></span>

 <span data-ttu-id="d205c-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="d205c-113">_pobj_</span></span>
  
> <span data-ttu-id="d205c-114">[in]**IMAPIProp**インターフェイス内のプロパティ タグを検索する**IMAPIProp**から派生したインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d205c-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="d205c-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="d205c-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="d205c-116">[in]検索するプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="d205c-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d205c-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="d205c-117">Return value</span></span>

<span data-ttu-id="d205c-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="d205c-118">TRUE</span></span> 
  
> <span data-ttu-id="d205c-119">指定されたプロパティ タグの一致が見つかりました。</span><span class="sxs-lookup"><span data-stu-id="d205c-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="d205c-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="d205c-120">FALSE</span></span> 
  
> <span data-ttu-id="d205c-121">指定されたプロパティ タグの一致は見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="d205c-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d205c-122">注釈</span><span class="sxs-lookup"><span data-stu-id="d205c-122">Remarks</span></span>

<span data-ttu-id="d205c-123">型 PT_UNSPECIFIED、 _ulPropTag_パラメーターのプロパティ タグの場合、 **FPropExists**関数は、プロパティの識別子にのみ基づいて一致するを探します。</span><span class="sxs-lookup"><span data-stu-id="d205c-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="d205c-124">それ以外の場合、一致が、型を含め、全体のプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="d205c-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

