---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417372"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="74e7d-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="74e7d-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="74e7d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74e7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74e7d-105">フォルダーの共有のサポートに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="74e7d-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="74e7d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74e7d-106">Parameters</span></span>

 <span data-ttu-id="74e7d-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="74e7d-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="74e7d-108">[out]フォルダーが共有をサポートするかどうかを示すビットマスク。</span><span class="sxs-lookup"><span data-stu-id="74e7d-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="74e7d-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="74e7d-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="74e7d-110">フォルダーが共有をサポートしていないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="74e7d-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="74e7d-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="74e7d-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="74e7d-112">フォルダーが共有をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="74e7d-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="74e7d-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="74e7d-113">Return value</span></span>

<span data-ttu-id="74e7d-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="74e7d-114">S_OK</span></span> 
  
> <span data-ttu-id="74e7d-115">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="74e7d-115">The call was successful.</span></span>
    

