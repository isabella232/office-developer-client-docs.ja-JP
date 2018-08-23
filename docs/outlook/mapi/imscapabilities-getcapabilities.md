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
ms.openlocfilehash: 0211a326e94c5847c040040e0e0e4e9ddd1d760d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583275"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="85ef3-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="85ef3-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="85ef3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85ef3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85ef3-105">ストアのサポートに関する情報を取得は、指定されたセレクターに基づいています。</span><span class="sxs-lookup"><span data-stu-id="85ef3-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="85ef3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85ef3-106">Parameters</span></span>

 <span data-ttu-id="85ef3-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="85ef3-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="85ef3-108">[in]セレクターを取得する機能を示します。</span><span class="sxs-lookup"><span data-stu-id="85ef3-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="85ef3-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="85ef3-109">Return value</span></span>

<span data-ttu-id="85ef3-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="85ef3-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="85ef3-111">既定以外のストア内のフォルダーのホーム ページをサポートします。</span><span class="sxs-lookup"><span data-stu-id="85ef3-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="85ef3-112">これは*mscapSelector*で**MSCAP_SEL_FOLDER**が指定されている場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="85ef3-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="85ef3-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="85ef3-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="85ef3-114">制限に無効なプロパティなどのすべての無効な引数が含まれている場合、ストアは無効な引数を無視し、有効な引数だけを処理します。</span><span class="sxs-lookup"><span data-stu-id="85ef3-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="85ef3-115">これは*mscapSelector*で**MSCAP_SEL_RESTRICTION**が指定されている場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="85ef3-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="85ef3-116">NULL</span><span class="sxs-lookup"><span data-stu-id="85ef3-116">NULL</span></span>
  
> <span data-ttu-id="85ef3-117">ストアは、指定されたセレクターに基づくすべての機能をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="85ef3-117">The store does not support any capability based on the given selector.</span></span>
    

