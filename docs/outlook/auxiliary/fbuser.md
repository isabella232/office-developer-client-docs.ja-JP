---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: 利用可能な空き時間情報データがない可能性がありますは、ユーザーを識別します。
ms.openlocfilehash: e83689e28f5fb6e1eae28d760bb57f5ad3796f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799307"
---
# <a name="fbuser"></a><span data-ttu-id="43bc2-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="43bc2-103">FBUser</span></span>

<span data-ttu-id="43bc2-104">利用可能な空き時間情報データがない可能性がありますは、ユーザーを識別します。</span><span class="sxs-lookup"><span data-stu-id="43bc2-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="43bc2-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="43bc2-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="43bc2-106">Members</span><span class="sxs-lookup"><span data-stu-id="43bc2-106">Members</span></span>

<span data-ttu-id="43bc2-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="43bc2-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="43bc2-108">[IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx)インターフェイスによって表される、メール ユーザーのエントリ ID の長さ。</span><span class="sxs-lookup"><span data-stu-id="43bc2-108">The length of the entry ID of the mail user as represented by the [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) interface.</span></span> 
    
<span data-ttu-id="43bc2-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="43bc2-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="43bc2-110">**IMailUser**インターフェイスによって表される、メール ユーザーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="43bc2-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="43bc2-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="43bc2-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="43bc2-112">このパラメーターは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="43bc2-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="43bc2-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="43bc2-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="43bc2-114">このパラメーターは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="43bc2-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43bc2-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="43bc2-115">See also</span></span>

- [<span data-ttu-id="43bc2-116">空き時間情報 API について</span><span class="sxs-lookup"><span data-stu-id="43bc2-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="43bc2-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="43bc2-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

