---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: 空き時間情報データを使用できるユーザーまたは使用できない可能性があるユーザーを識別します。
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317662"
---
# <a name="fbuser"></a><span data-ttu-id="4aa13-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="4aa13-103">FBUser</span></span>

<span data-ttu-id="4aa13-104">空き時間情報データを使用できるユーザーまたは使用できない可能性があるユーザーを識別します。</span><span class="sxs-lookup"><span data-stu-id="4aa13-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4aa13-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="4aa13-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="4aa13-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="4aa13-106">Members</span></span>

<span data-ttu-id="4aa13-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="4aa13-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="4aa13-108">[IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops)インターフェイスで表されるメール ユーザーのエントリ ID の長さ。</span><span class="sxs-lookup"><span data-stu-id="4aa13-108">The length of the entry ID of the mail user as represented by the [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) interface.</span></span> 
    
<span data-ttu-id="4aa13-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="4aa13-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="4aa13-110">IMailUser インターフェイスで表されるメール ユーザー **のエントリ ID。**</span><span class="sxs-lookup"><span data-stu-id="4aa13-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="4aa13-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="4aa13-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="4aa13-112">このパラメーターは、内部Outlook使用するために予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4aa13-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="4aa13-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="4aa13-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="4aa13-114">このパラメーターは、内部Outlook使用するために予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4aa13-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4aa13-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="4aa13-115">See also</span></span>

- [<span data-ttu-id="4aa13-116">空き時間情報 API について</span><span class="sxs-lookup"><span data-stu-id="4aa13-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="4aa13-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="4aa13-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

