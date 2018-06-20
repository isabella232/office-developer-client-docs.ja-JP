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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b236b24c10a241dbdecc28bf2e04de5f69e989e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801490"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="dd2a0-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="dd2a0-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="dd2a0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dd2a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dd2a0-105">既定の MAPI のメモリ割り当て関数のアドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="dd2a0-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd2a0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dd2a0-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd2a0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dd2a0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dd2a0-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="dd2a0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dd2a0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dd2a0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dd2a0-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="dd2a0-110">Called by:</span></span>  <br/> |<span data-ttu-id="dd2a0-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="dd2a0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="dd2a0-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="dd2a0-112">Parameters</span></span>

<span data-ttu-id="dd2a0-113">なし。</span><span class="sxs-lookup"><span data-stu-id="dd2a0-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="dd2a0-114">Return value</span><span class="sxs-lookup"><span data-stu-id="dd2a0-114">Return value</span></span>

<span data-ttu-id="dd2a0-115">**MAPIGetDefaultMalloc**関数は、既定の MAPI のメモリ割り当て関数にポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="dd2a0-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

