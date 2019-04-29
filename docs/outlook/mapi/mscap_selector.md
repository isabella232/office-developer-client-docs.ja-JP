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
# <a name="mscapselector"></a><span data-ttu-id="120cb-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="120cb-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="120cb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="120cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="120cb-105">ストアに対して返す機能を指定します。</span><span class="sxs-lookup"><span data-stu-id="120cb-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="120cb-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="120cb-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="120cb-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="120cb-107">Members</span></span>

 <span data-ttu-id="120cb-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="120cb-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="120cb-109">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="120cb-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="120cb-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="120cb-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="120cb-111">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="120cb-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="120cb-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="120cb-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="120cb-113">ストア上のフォルダーのサポートに関する機能。</span><span class="sxs-lookup"><span data-stu-id="120cb-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="120cb-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="120cb-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="120cb-115">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="120cb-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="120cb-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="120cb-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="120cb-117">ストアに対する制限のサポートに関する機能。</span><span class="sxs-lookup"><span data-stu-id="120cb-117">Capabilities about supporting restrictions on a store.</span></span>
    

