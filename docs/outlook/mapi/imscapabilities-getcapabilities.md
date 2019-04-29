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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409259"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="b6456-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="b6456-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="b6456-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6456-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6456-105">指定したセレクターに基づいてストアがサポートできる内容に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="b6456-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="b6456-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b6456-106">Parameters</span></span>

 <span data-ttu-id="b6456-107">*getcapabilities*</span><span class="sxs-lookup"><span data-stu-id="b6456-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="b6456-108">順番返す機能を示すセレクター。</span><span class="sxs-lookup"><span data-stu-id="b6456-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b6456-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="b6456-109">Return value</span></span>

<span data-ttu-id="b6456-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="b6456-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="b6456-111">既定以外のストアでのフォルダー homepages のサポート。</span><span class="sxs-lookup"><span data-stu-id="b6456-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="b6456-112">これは、 **MSCAP_SEL_FOLDER**が*getcapabilities*で指定されている場合に返されることがあります。</span><span class="sxs-lookup"><span data-stu-id="b6456-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="b6456-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="b6456-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="b6456-114">無効なプロパティなどの無効な引数が制限に含まれている場合、ストアは無効な引数を無視し、有効な引数のみを処理します。</span><span class="sxs-lookup"><span data-stu-id="b6456-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="b6456-115">これは、 **MSCAP_SEL_RESTRICTION**が*getcapabilities*で指定されている場合に返されることがあります。</span><span class="sxs-lookup"><span data-stu-id="b6456-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="b6456-116">NULL</span><span class="sxs-lookup"><span data-stu-id="b6456-116">NULL</span></span>
  
> <span data-ttu-id="b6456-117">ストアは、指定されたセレクターに基づく機能をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b6456-117">The store does not support any capability based on the given selector.</span></span>
    

