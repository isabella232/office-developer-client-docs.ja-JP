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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3176280de33bda01bfd09ebaafc31d326d455a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575036"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="4a4dc-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="4a4dc-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="4a4dc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a4dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a4dc-105">[ユーティリティ関数だけを使用する場合に[生じます](mapiinitialize.md)を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="4a4dc-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a4dc-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4a4dc-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a4dc-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4a4dc-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4a4dc-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="4a4dc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4a4dc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4a4dc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4a4dc-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4a4dc-110">Called by:</span></span>  <br/> |<span data-ttu-id="4a4dc-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="4a4dc-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4a4dc-112">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="4a4dc-112">Parameters</span></span>

 <span data-ttu-id="4a4dc-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4a4dc-113">_ulFlags_</span></span>
  
> <span data-ttu-id="4a4dc-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="4a4dc-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4a4dc-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="4a4dc-115">Return value</span></span>

<span data-ttu-id="4a4dc-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4a4dc-116">S_OK</span></span> 
  
> <span data-ttu-id="4a4dc-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="4a4dc-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4a4dc-118">����</span><span class="sxs-lookup"><span data-stu-id="4a4dc-118">Remarks</span></span>

<span data-ttu-id="4a4dc-119">[生じます](mapiinitialize.md)コアとユーティリティを呼び出すのではなく、機能の選択のユーティリティ関数を解放し、 **ScInitMapiUtil**および[DeinitMapiUtil](deinitmapiutil.md)関数が協力します。</span><span class="sxs-lookup"><span data-stu-id="4a4dc-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="4a4dc-120">**ScInitMapiUtil**では、ユーティリティ関数を呼び出すと、も、必要なメモリを初期化します。</span><span class="sxs-lookup"><span data-stu-id="4a4dc-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="4a4dc-121">**ScInitMapiUtil**が呼び出されている関数の使用が完了すると、それらを解放する**DeinitMapiUtil**を明示的に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a4dc-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="4a4dc-122">**生じます**は対照的に、 **DeinitMapiUtil**を暗黙的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4a4dc-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4a4dc-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="4a4dc-123">See also</span></span>



[<span data-ttu-id="4a4dc-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="4a4dc-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

