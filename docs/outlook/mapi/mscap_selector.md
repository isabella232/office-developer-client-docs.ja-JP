---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 420b2661e766ecf97a5e9e488e9c18f29cd91329
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19801645"
---
# <a name="mscapselector"></a><span data-ttu-id="87402-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="87402-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="87402-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87402-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="87402-105">ストアを取得する機能を指定します。</span><span class="sxs-lookup"><span data-stu-id="87402-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="87402-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="87402-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="87402-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="87402-107">Members</span></span>

 <span data-ttu-id="87402-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="87402-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="87402-109">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="87402-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="87402-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="87402-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="87402-111">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="87402-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="87402-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="87402-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="87402-113">ストアにフォルダーをサポートする機能です。</span><span class="sxs-lookup"><span data-stu-id="87402-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="87402-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="87402-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="87402-115">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="87402-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="87402-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="87402-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="87402-117">ストアの制限をサポートする機能です。</span><span class="sxs-lookup"><span data-stu-id="87402-117">Capabilities about supporting restrictions on a store.</span></span>
    

