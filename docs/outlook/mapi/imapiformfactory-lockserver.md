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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c33fea8a2aba875fcdc06dea3343add4b7ac5dde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800522"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="a6bad-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="a6bad-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="a6bad-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6bad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6bad-105">開いているフォームのサーバーは、メモリ内に保持します。</span><span class="sxs-lookup"><span data-stu-id="a6bad-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="a6bad-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="a6bad-106">Parameters</span></span>

 <span data-ttu-id="a6bad-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6bad-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a6bad-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a6bad-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a6bad-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="a6bad-109">_fLockServer_</span></span>
  
> <span data-ttu-id="a6bad-110">[in]の**場合は true**ロック カウントをインクリメントするのにはそれ以外の場合、 **false を指定**します。</span><span class="sxs-lookup"><span data-stu-id="a6bad-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6bad-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a6bad-111">Return value</span></span>

<span data-ttu-id="a6bad-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6bad-112">S_OK</span></span> 
  
> <span data-ttu-id="a6bad-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a6bad-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6bad-114">����</span><span class="sxs-lookup"><span data-stu-id="a6bad-114">Remarks</span></span>

<span data-ttu-id="a6bad-115">フォーム ビューアーは、開いているフォームのサーバー アプリケーションをメモリに保持する**IMAPIFormFactory::LockServer**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a6bad-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="a6bad-116">フォーム サーバーをメモリに保持では、頻繁にフォームが作成され、リリースされたときに、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="a6bad-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a6bad-117">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="a6bad-117">Notes to implementers</span></span>

<span data-ttu-id="a6bad-118">**IMAPIFormFactory::LockServer**メソッドでは、 [IClassFactory::LockServer](http://msdn.microsoft.com/ja-jp/library/ms682332%28v=VS.85%29.aspx)メソッドによく似ています。</span><span class="sxs-lookup"><span data-stu-id="a6bad-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](http://msdn.microsoft.com/ja-jp/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="a6bad-119">本質的に、 **IMAPIFormFactory::LockServer**メソッドを維持何度の数が呼び出されました。そのカウントが 0 より大きい場合に限り、メソッドは、メモリからアンロードされるフォームのサーバーを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="a6bad-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="a6bad-120">[CoLockObjectExternal](http://msdn.microsoft.com/ja-jp/library/ms680592%28VS.85%29.aspx)関数を使用すると、この機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="a6bad-120">You can use the [CoLockObjectExternal](http://msdn.microsoft.com/ja-jp/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6bad-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6bad-121">See also</span></span>



[<span data-ttu-id="a6bad-122">IMAPIFormFactory: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6bad-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

