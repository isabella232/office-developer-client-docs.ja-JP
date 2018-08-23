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
ms.openlocfilehash: cb0630ba30f8d3d7ae38c165c5da60bbc12077c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592333"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="1c8c8-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="1c8c8-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="1c8c8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c8c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c8c8-105">既定の MAPI のメモリ割り当て関数のアドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="1c8c8-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c8c8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1c8c8-106">Header file:</span></span>  <br/> |<span data-ttu-id="1c8c8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1c8c8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1c8c8-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="1c8c8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1c8c8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1c8c8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1c8c8-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1c8c8-110">Called by:</span></span>  <br/> |<span data-ttu-id="1c8c8-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1c8c8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="1c8c8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1c8c8-112">Parameters</span></span>

<span data-ttu-id="1c8c8-113">なし。</span><span class="sxs-lookup"><span data-stu-id="1c8c8-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="1c8c8-114">Return value</span><span class="sxs-lookup"><span data-stu-id="1c8c8-114">Return value</span></span>

<span data-ttu-id="1c8c8-115">**MAPIGetDefaultMalloc**関数は、既定の MAPI のメモリ割り当て関数にポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="1c8c8-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

