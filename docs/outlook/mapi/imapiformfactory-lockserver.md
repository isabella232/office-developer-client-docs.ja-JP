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
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="149c2-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="149c2-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="149c2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="149c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="149c2-105">開いているフォーム サーバーをメモリに保持します。</span><span class="sxs-lookup"><span data-stu-id="149c2-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="149c2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="149c2-106">Parameters</span></span>

 <span data-ttu-id="149c2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="149c2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="149c2-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="149c2-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="149c2-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="149c2-109">_fLockServer_</span></span>
  
> <span data-ttu-id="149c2-110">[in] **ロック数** を増やす場合は true。それ以外の場合は **false です**。</span><span class="sxs-lookup"><span data-stu-id="149c2-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="149c2-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="149c2-111">Return value</span></span>

<span data-ttu-id="149c2-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="149c2-112">S_OK</span></span> 
  
> <span data-ttu-id="149c2-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="149c2-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="149c2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="149c2-114">Remarks</span></span>

<span data-ttu-id="149c2-115">フォーム ビューアーは **IMAPIFormFactory::LockServer** メソッドを呼び出して、開いているフォーム サーバー アプリケーションをメモリに保持します。</span><span class="sxs-lookup"><span data-stu-id="149c2-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="149c2-116">フォーム サーバーをメモリに保持すると、フォームが頻繁に作成およびリリースされる場合のパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="149c2-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="149c2-117">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="149c2-117">Notes to implementers</span></span>

<span data-ttu-id="149c2-118">**IMAPIFormFactory::LockServer** メソッドは [、IClassFactory::LockServer メソッドと非常に似](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx)ています。</span><span class="sxs-lookup"><span data-stu-id="149c2-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="149c2-119">基本的に **、IMAPIFormFactory::LockServer** メソッドは、呼び出された回数のカウントを保持します。この数が 0 より大きい限り、フォーム サーバーはメモリからアンロードされません。</span><span class="sxs-lookup"><span data-stu-id="149c2-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="149c2-120">これを実装するには [、CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) 関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="149c2-120">You can use the [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="149c2-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="149c2-121">See also</span></span>



[<span data-ttu-id="149c2-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="149c2-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

