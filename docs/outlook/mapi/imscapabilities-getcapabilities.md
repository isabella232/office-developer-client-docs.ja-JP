---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 27db5f54f6a6feba77308a4a63fe4c16448550cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800986"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="e04ac-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="e04ac-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="e04ac-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e04ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e04ac-105">ストアのサポートに関する情報を取得は、指定されたセレクターに基づいています。</span><span class="sxs-lookup"><span data-stu-id="e04ac-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="e04ac-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e04ac-106">Parameters</span></span>

 <span data-ttu-id="e04ac-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="e04ac-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="e04ac-108">[in]セレクターを取得する機能を示します。</span><span class="sxs-lookup"><span data-stu-id="e04ac-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e04ac-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="e04ac-109">Return value</span></span>

<span data-ttu-id="e04ac-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="e04ac-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="e04ac-111">既定以外のストア内のフォルダーのホーム ページをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e04ac-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="e04ac-112">これは*mscapSelector*で**MSCAP_SEL_FOLDER**が指定されている場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="e04ac-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="e04ac-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="e04ac-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="e04ac-114">制限に無効なプロパティなどのすべての無効な引数が含まれている場合、ストアは無効な引数を無視し、有効な引数だけを処理します。</span><span class="sxs-lookup"><span data-stu-id="e04ac-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="e04ac-115">これは*mscapSelector*で**MSCAP_SEL_RESTRICTION**が指定されている場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="e04ac-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="e04ac-116">NULL</span><span class="sxs-lookup"><span data-stu-id="e04ac-116">NULL</span></span>
  
> <span data-ttu-id="e04ac-117">ストアは、指定されたセレクターに基づくすべての機能をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="e04ac-117">The store does not support any capability based on the given selector.</span></span>
    

