---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: 利用可能な空き時間情報データがない可能性がありますは、ユーザーを識別します。
ms.openlocfilehash: edfc9980445fcc2e111045650667d93bffa94153
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565138"
---
# <a name="fbuser"></a><span data-ttu-id="6b3c4-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="6b3c4-103">FBUser</span></span>

<span data-ttu-id="6b3c4-104">利用可能な空き時間情報データがない可能性がありますは、ユーザーを識別します。</span><span class="sxs-lookup"><span data-stu-id="6b3c4-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6b3c4-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="6b3c4-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="6b3c4-106">Members</span><span class="sxs-lookup"><span data-stu-id="6b3c4-106">Members</span></span>

<span data-ttu-id="6b3c4-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="6b3c4-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="6b3c4-108">[IMailUser](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops)インターフェイスによって表される、メール ユーザーのエントリ ID の長さ。</span><span class="sxs-lookup"><span data-stu-id="6b3c4-108">The length of the entry ID of the mail user as represented by the [IMailUser](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) interface.</span></span> 
    
<span data-ttu-id="6b3c4-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="6b3c4-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="6b3c4-110">**IMailUser**インターフェイスによって表される、メール ユーザーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="6b3c4-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="6b3c4-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="6b3c4-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="6b3c4-112">このパラメーターは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6b3c4-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="6b3c4-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="6b3c4-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="6b3c4-114">このパラメーターは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6b3c4-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b3c4-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b3c4-115">See also</span></span>

- [<span data-ttu-id="6b3c4-116">空き時間情報 API について</span><span class="sxs-lookup"><span data-stu-id="6b3c4-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="6b3c4-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="6b3c4-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

