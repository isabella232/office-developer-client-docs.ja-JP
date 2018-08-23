---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e84dbc0976f5c438a7e0b5fd7cddcbf1c0659f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574798"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="5f92a-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="5f92a-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="5f92a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f92a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f92a-105">ユーティリティ関数が明示的に呼び出される[ScInitMapiUtil](scinitmapiutil.md)関数によって、暗黙的に[生じます](mapiinitialize.md)を解放します。</span><span class="sxs-lookup"><span data-stu-id="5f92a-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5f92a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5f92a-106">Header file:</span></span>  <br/> |<span data-ttu-id="5f92a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5f92a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5f92a-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="5f92a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5f92a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5f92a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5f92a-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5f92a-110">Called by:</span></span>  <br/> |<span data-ttu-id="5f92a-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5f92a-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="5f92a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5f92a-112">Parameters</span></span>

<span data-ttu-id="5f92a-113">なし</span><span class="sxs-lookup"><span data-stu-id="5f92a-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="5f92a-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="5f92a-114">Return value</span></span>

<span data-ttu-id="5f92a-115">なし</span><span class="sxs-lookup"><span data-stu-id="5f92a-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5f92a-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5f92a-116">Remarks</span></span>

<span data-ttu-id="5f92a-117">**DeinitMapiUtil**関数は、 [ScInitMapiUtil](scinitmapiutil.md)または[生じます](mapiinitialize.md)を使用して初期化関数を解放します。</span><span class="sxs-lookup"><span data-stu-id="5f92a-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="5f92a-118">**ScInitMapiUtil**によって呼び出される関数の使用が完了すると、それらを解放する**DeinitMapiUtil**を明示的に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f92a-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="5f92a-119">[MAPIUninitialize](mapiuninitialize.md)は対照的に、 **DeinitMapiUtil**を暗黙的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5f92a-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

