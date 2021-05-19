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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427347"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="192cf-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="192cf-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="192cf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="192cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="192cf-105">[ScInitMapiUtil](scinitmapiutil.md)関数によって明示的に、または[MAPIInitialize](mapiinitialize.md)関数によって暗黙的に呼び出されるユーティリティ関数を解放します。</span><span class="sxs-lookup"><span data-stu-id="192cf-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="192cf-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="192cf-106">Header file:</span></span>  <br/> |<span data-ttu-id="192cf-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="192cf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="192cf-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="192cf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="192cf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="192cf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="192cf-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="192cf-110">Called by:</span></span>  <br/> |<span data-ttu-id="192cf-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="192cf-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="192cf-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="192cf-112">Parameters</span></span>

<span data-ttu-id="192cf-113">なし</span><span class="sxs-lookup"><span data-stu-id="192cf-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="192cf-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="192cf-114">Return value</span></span>

<span data-ttu-id="192cf-115">なし</span><span class="sxs-lookup"><span data-stu-id="192cf-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="192cf-116">注釈</span><span class="sxs-lookup"><span data-stu-id="192cf-116">Remarks</span></span>

<span data-ttu-id="192cf-117">**DeinitMapiUtil 関数は**[、ScInitMapiUtil](scinitmapiutil.md)または [MAPIInitialize で初期化された関数を解放します](mapiinitialize.md)。</span><span class="sxs-lookup"><span data-stu-id="192cf-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="192cf-118">**ScInitMapiUtil** によって呼び出される関数の使用が完了したら **、DeinitMapiUtil** を明示的に呼び出して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="192cf-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="192cf-119">これに対し [、MAPIUninitialize は](mapiuninitialize.md) **DeinitMapiUtil を暗黙的に呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="192cf-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

