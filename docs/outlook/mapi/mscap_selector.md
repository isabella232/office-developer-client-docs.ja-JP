---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417204"
---
# <a name="mscap_selector"></a><span data-ttu-id="d3465-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="d3465-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="d3465-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3465-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3465-105">ストアに返す機能を指定します。</span><span class="sxs-lookup"><span data-stu-id="d3465-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d3465-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d3465-106">Quick info</span></span>

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a><span data-ttu-id="d3465-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="d3465-107">Members</span></span>

 <span data-ttu-id="d3465-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="d3465-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="d3465-109">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d3465-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="d3465-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="d3465-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="d3465-111">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d3465-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="d3465-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="d3465-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="d3465-113">ストア上のサポート フォルダーに関する機能。</span><span class="sxs-lookup"><span data-stu-id="d3465-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="d3465-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="d3465-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="d3465-115">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d3465-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="d3465-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="d3465-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="d3465-117">ストアの制限をサポートする機能。</span><span class="sxs-lookup"><span data-stu-id="d3465-117">Capabilities about supporting restrictions on a store.</span></span>
    

