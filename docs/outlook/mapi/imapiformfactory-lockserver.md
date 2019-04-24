---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342141"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="7e0ea-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="7e0ea-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="7e0ea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e0ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e0ea-105">開いているフォームサーバーをメモリに保持します。</span><span class="sxs-lookup"><span data-stu-id="7e0ea-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="7e0ea-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7e0ea-106">Parameters</span></span>

 <span data-ttu-id="7e0ea-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7e0ea-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7e0ea-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="7e0ea-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7e0ea-109">_flockserver_</span><span class="sxs-lookup"><span data-stu-id="7e0ea-109">_fLockServer_</span></span>
  
> <span data-ttu-id="7e0ea-110">順番ロックカウントを増分する場合は true、それ以外の**場合は true** 。それ以外の場合は**false**。</span><span class="sxs-lookup"><span data-stu-id="7e0ea-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7e0ea-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="7e0ea-111">Return value</span></span>

<span data-ttu-id="7e0ea-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e0ea-112">S_OK</span></span> 
  
> <span data-ttu-id="7e0ea-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="7e0ea-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e0ea-114">解説</span><span class="sxs-lookup"><span data-stu-id="7e0ea-114">Remarks</span></span>

<span data-ttu-id="7e0ea-115">フォームビューアーは、open form サーバーアプリケーションをメモリに保持する**imapiformfactory:: lockserver**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7e0ea-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="7e0ea-116">フォームサーバーをメモリに保持すると、フォームが頻繁に作成およびリリースされるときのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="7e0ea-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7e0ea-117">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7e0ea-117">Notes to implementers</span></span>

<span data-ttu-id="7e0ea-118">**imapiformfactory:: lockserver**メソッドは、 [IClassFactory:: lockserver](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx)メソッドによく似ています。</span><span class="sxs-lookup"><span data-stu-id="7e0ea-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="7e0ea-119">基本的に、 **imapiformfactory:: lockserver**メソッドは、呼び出し回数のカウントを保持します。このカウントが0より大きい限り、このメソッドは、フォームサーバーがメモリからアンロードされないようにします。</span><span class="sxs-lookup"><span data-stu-id="7e0ea-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="7e0ea-120">[colockobjectexternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx)関数を使用して、これを実装できます。</span><span class="sxs-lookup"><span data-stu-id="7e0ea-120">You can use the [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e0ea-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e0ea-121">See also</span></span>



[<span data-ttu-id="7e0ea-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e0ea-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

