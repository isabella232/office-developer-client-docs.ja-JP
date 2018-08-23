---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c4e5d2847b53988fb75e23fc6c4dfc386ea678f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579264"
---
# <a name="getinstance"></a><span data-ttu-id="cff2a-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="cff2a-103">GetInstance</span></span>

  
  
<span data-ttu-id="cff2a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cff2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cff2a-105">同じ型の単一値プロパティに、複数値を持つプロパティ内の 1 つの値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="cff2a-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cff2a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cff2a-106">Header file:</span></span>  <br/> |<span data-ttu-id="cff2a-107">MAPIUTIL。H</span><span class="sxs-lookup"><span data-stu-id="cff2a-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="cff2a-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="cff2a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cff2a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cff2a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cff2a-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="cff2a-110">Called by:</span></span>  <br/> |<span data-ttu-id="cff2a-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cff2a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="cff2a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cff2a-112">Parameters</span></span>

 <span data-ttu-id="cff2a-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="cff2a-113">_pvalMv_</span></span>
  
> <span data-ttu-id="cff2a-114">[in]複数値を持つプロパティを定義する[SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cff2a-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="cff2a-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="cff2a-115">_pvalSv_</span></span>
  
> <span data-ttu-id="cff2a-116">[in]データを受信する単一値のプロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cff2a-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="cff2a-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="cff2a-117">_uliInst_</span></span>
  
> <span data-ttu-id="cff2a-118">[in]インスタンス番号は、 _pvalMv_パラメーターで指定された構造体からコピーされる値の配列要素は、です。</span><span class="sxs-lookup"><span data-stu-id="cff2a-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cff2a-119">Return value</span><span class="sxs-lookup"><span data-stu-id="cff2a-119">Return value</span></span>

<span data-ttu-id="cff2a-120">なし。</span><span class="sxs-lookup"><span data-stu-id="cff2a-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cff2a-121">注釈</span><span class="sxs-lookup"><span data-stu-id="cff2a-121">Remarks</span></span>

<span data-ttu-id="cff2a-122">コピーされる値が割り当てられたメモリに対して大きすぎる場合は、 **GetInstance**関数は新しいメモリの割り当てではなくポインターのみをコピーします。</span><span class="sxs-lookup"><span data-stu-id="cff2a-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

