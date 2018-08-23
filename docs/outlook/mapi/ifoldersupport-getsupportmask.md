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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c51f4a7266e67be08f31daa5afbf23ce0b256252
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567854"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="660d2-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="660d2-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="660d2-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="660d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="660d2-105">共有フォルダーのサポートに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="660d2-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="660d2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="660d2-106">Parameters</span></span>

 <span data-ttu-id="660d2-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="660d2-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="660d2-108">[out]フォルダーが共有をサポートしているかを示すビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="660d2-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="660d2-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="660d2-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="660d2-110">フォルダーを共有するサポートしていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="660d2-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="660d2-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="660d2-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="660d2-112">共有フォルダーをサポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="660d2-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="660d2-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="660d2-113">Return value</span></span>

<span data-ttu-id="660d2-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="660d2-114">S_OK</span></span> 
  
> <span data-ttu-id="660d2-115">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="660d2-115">The call was successful.</span></span>
    

