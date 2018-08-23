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
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800436"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="03dcd-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="03dcd-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="03dcd-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03dcd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03dcd-105">共有フォルダーのサポートに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="03dcd-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="03dcd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="03dcd-106">Parameters</span></span>

 <span data-ttu-id="03dcd-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="03dcd-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="03dcd-108">[out]フォルダーが共有をサポートしているかを示すビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="03dcd-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="03dcd-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="03dcd-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="03dcd-110">フォルダーを共有するサポートしていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="03dcd-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="03dcd-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="03dcd-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="03dcd-112">共有フォルダーをサポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="03dcd-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="03dcd-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="03dcd-113">Return value</span></span>

<span data-ttu-id="03dcd-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="03dcd-114">S_OK</span></span> 
  
> <span data-ttu-id="03dcd-115">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="03dcd-115">The call was successful.</span></span>
    

