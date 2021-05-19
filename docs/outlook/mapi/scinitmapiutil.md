---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420592"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="bc49a-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="bc49a-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="bc49a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc49a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc49a-105">選択ユーティリティ [関数のみを使用している場合は、MAPIInitialize](mapiinitialize.md) を置き換える。</span><span class="sxs-lookup"><span data-stu-id="bc49a-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc49a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bc49a-106">Header file:</span></span>  <br/> |<span data-ttu-id="bc49a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="bc49a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bc49a-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="bc49a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bc49a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bc49a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bc49a-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="bc49a-110">Called by:</span></span>  <br/> |<span data-ttu-id="bc49a-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="bc49a-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bc49a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bc49a-112">Parameters</span></span>

 <span data-ttu-id="bc49a-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc49a-113">_ulFlags_</span></span>
  
> <span data-ttu-id="bc49a-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="bc49a-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bc49a-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="bc49a-115">Return value</span></span>

<span data-ttu-id="bc49a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc49a-116">S_OK</span></span> 
  
> <span data-ttu-id="bc49a-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="bc49a-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc49a-118">注釈</span><span class="sxs-lookup"><span data-stu-id="bc49a-118">Remarks</span></span>

<span data-ttu-id="bc49a-119">**ScInitMapiUtil** 関数と [DeinitMapiUtil](deinitmapiutil.md)関数は [、MAPIInitialize](mapiinitialize.md)ではなく、選択したユーティリティ関数を呼び出して解放するために協力します。これは、コア関数とユーティリティ関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bc49a-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="bc49a-120">**ScInitMapiUtil がユーティリティ** 関数を呼び出す場合は、必要なメモリも初期化します。</span><span class="sxs-lookup"><span data-stu-id="bc49a-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="bc49a-121">**ScInitMapiUtil** が呼び出した関数の使用が完了したら **、DeinitMapiUtil** を明示的に呼び出して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc49a-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="bc49a-122">これに対し **、MAPIInitialize は** **DeinitMapiUtil を暗黙的に呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="bc49a-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc49a-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc49a-123">See also</span></span>



[<span data-ttu-id="bc49a-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="bc49a-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

