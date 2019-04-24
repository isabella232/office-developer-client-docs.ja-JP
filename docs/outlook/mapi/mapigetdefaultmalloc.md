---
title: MAPIGetDefaultMalloc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIGetDefaultMalloc
api_type:
- HeaderDef
ms.assetid: 148695dd-d886-4a06-9cfe-749059ae91ed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 635f22c97ed27889245becbebb990ab3995b70b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345778"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="4a7b0-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="4a7b0-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="4a7b0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a7b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a7b0-105">既定の MAPI メモリ割り当て関数のアドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="4a7b0-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a7b0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4a7b0-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a7b0-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="4a7b0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4a7b0-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="4a7b0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4a7b0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4a7b0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4a7b0-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="4a7b0-110">Called by:</span></span>  <br/> |<span data-ttu-id="4a7b0-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="4a7b0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="4a7b0-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4a7b0-112">Parameters</span></span>

<span data-ttu-id="4a7b0-113">なし。</span><span class="sxs-lookup"><span data-stu-id="4a7b0-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="4a7b0-114">Return value</span><span class="sxs-lookup"><span data-stu-id="4a7b0-114">Return value</span></span>

<span data-ttu-id="4a7b0-115">**mapigetdefaultmalloc**関数は、既定の MAPI メモリ割り当て関数へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="4a7b0-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

