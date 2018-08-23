---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0d8d1b8509f699b20f6e436d8af2c1d0d97cf4ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800048"
---
# <a name="fequalnames"></a><span data-ttu-id="595f8-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="595f8-103">FEqualNames</span></span>

  
  
<span data-ttu-id="595f8-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="595f8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="595f8-105">2 つの MAPI 名前付きプロパティが同じかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="595f8-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="595f8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="595f8-106">Header file:</span></span>  <br/> |<span data-ttu-id="595f8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="595f8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="595f8-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="595f8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="595f8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="595f8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="595f8-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="595f8-110">Called by:</span></span>  <br/> |<span data-ttu-id="595f8-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="595f8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="595f8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="595f8-112">Parameters</span></span>

 <span data-ttu-id="595f8-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="595f8-113">_lpName1_</span></span>
  
> <span data-ttu-id="595f8-114">[in]最初の名前付きプロパティを記述する[MAPINAMEID](mapinameid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="595f8-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="595f8-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="595f8-115">_lpName2_</span></span>
  
> <span data-ttu-id="595f8-116">[in]2 番目の名前付きプロパティを記述する**MAPINAMEID**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="595f8-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="595f8-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="595f8-117">Return value</span></span>

<span data-ttu-id="595f8-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="595f8-118">TRUE</span></span> 
  
> <span data-ttu-id="595f8-119">2 つのプロパティ名は、同じです。</span><span class="sxs-lookup"><span data-stu-id="595f8-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="595f8-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="595f8-120">FALSE</span></span> 
  
> <span data-ttu-id="595f8-121">2 つのプロパティ名が等しくないです。</span><span class="sxs-lookup"><span data-stu-id="595f8-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="595f8-122">注釈</span><span class="sxs-lookup"><span data-stu-id="595f8-122">Remarks</span></span>

<span data-ttu-id="595f8-123">**FEqualNames**関数は、 **MAPINAMEID**構造体は[GUID](guid.md)が含まれていて、複数の方法でプロパティ名自体を表すことができますので便利です。</span><span class="sxs-lookup"><span data-stu-id="595f8-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="595f8-124">つまり、バイナリの簡単な方法で 2 つの構造体を比較することはできません。</span><span class="sxs-lookup"><span data-stu-id="595f8-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="595f8-125">テスト プロセスは、プロパティ名の文字列の大文字小文字を区別します。</span><span class="sxs-lookup"><span data-stu-id="595f8-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

