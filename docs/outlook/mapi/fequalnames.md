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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414803"
---
# <a name="fequalnames"></a><span data-ttu-id="ebc0b-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="ebc0b-103">FEqualNames</span></span>

  
  
<span data-ttu-id="ebc0b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebc0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebc0b-105">2つの MAPI 名前付きプロパティが同じかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="ebc0b-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ebc0b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ebc0b-106">Header file:</span></span>  <br/> |<span data-ttu-id="ebc0b-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="ebc0b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ebc0b-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="ebc0b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ebc0b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ebc0b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ebc0b-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ebc0b-110">Called by:</span></span>  <br/> |<span data-ttu-id="ebc0b-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="ebc0b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="ebc0b-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ebc0b-112">Parameters</span></span>

 <span data-ttu-id="ebc0b-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="ebc0b-113">_lpName1_</span></span>
  
> <span data-ttu-id="ebc0b-114">順番最初の名前付きプロパティを説明する[mapinameid](mapinameid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ebc0b-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="ebc0b-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="ebc0b-115">_lpName2_</span></span>
  
> <span data-ttu-id="ebc0b-116">順番2番目の名前付きプロパティを説明する**mapinameid**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ebc0b-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ebc0b-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="ebc0b-117">Return value</span></span>

<span data-ttu-id="ebc0b-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="ebc0b-118">TRUE</span></span> 
  
> <span data-ttu-id="ebc0b-119">2つのプロパティ名は同じです。</span><span class="sxs-lookup"><span data-stu-id="ebc0b-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="ebc0b-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="ebc0b-120">FALSE</span></span> 
  
> <span data-ttu-id="ebc0b-121">2つのプロパティ名は同じではありません。</span><span class="sxs-lookup"><span data-stu-id="ebc0b-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ebc0b-122">注釈</span><span class="sxs-lookup"><span data-stu-id="ebc0b-122">Remarks</span></span>

<span data-ttu-id="ebc0b-123">**mapinameid**構造には[GUID](guid.md)が含まれ、プロパティ名自体を複数の方法で表すことができるので、 **FEqualNames**関数は便利です。</span><span class="sxs-lookup"><span data-stu-id="ebc0b-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="ebc0b-124">これは、2つの構造体を単純な binary メソッドと比較できないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="ebc0b-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="ebc0b-125">テストプロセスでは、プロパティ名文字列の大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="ebc0b-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

