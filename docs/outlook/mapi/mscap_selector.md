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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338676"
---
# <a name="mscapselector"></a><span data-ttu-id="602d5-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="602d5-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="602d5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="602d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="602d5-105">ストアに対して返す機能を指定します。</span><span class="sxs-lookup"><span data-stu-id="602d5-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="602d5-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="602d5-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="602d5-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="602d5-107">Members</span></span>

 <span data-ttu-id="602d5-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="602d5-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="602d5-109">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="602d5-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="602d5-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="602d5-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="602d5-111">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="602d5-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="602d5-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="602d5-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="602d5-113">ストア上のフォルダーのサポートに関する機能。</span><span class="sxs-lookup"><span data-stu-id="602d5-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="602d5-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="602d5-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="602d5-115">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="602d5-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="602d5-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="602d5-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="602d5-117">ストアに対する制限のサポートに関する機能。</span><span class="sxs-lookup"><span data-stu-id="602d5-117">Capabilities about supporting restrictions on a store.</span></span>
    

