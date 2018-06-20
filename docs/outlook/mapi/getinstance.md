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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f65f047a73a2c06ca02251c554e5dca42352b6c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800173"
---
# <a name="getinstance"></a><span data-ttu-id="fa992-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="fa992-103">GetInstance</span></span>

  
  
<span data-ttu-id="fa992-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa992-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa992-105">同じ型の単一値プロパティに、複数値を持つプロパティ内の 1 つの値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="fa992-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa992-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fa992-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa992-107">MAPIUTIL。H</span><span class="sxs-lookup"><span data-stu-id="fa992-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="fa992-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="fa992-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fa992-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fa992-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fa992-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fa992-110">Called by:</span></span>  <br/> |<span data-ttu-id="fa992-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="fa992-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="fa992-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="fa992-112">Parameters</span></span>

 <span data-ttu-id="fa992-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="fa992-113">_pvalMv_</span></span>
  
> <span data-ttu-id="fa992-114">[in]複数値を持つプロパティを定義する[SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fa992-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="fa992-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="fa992-115">_pvalSv_</span></span>
  
> <span data-ttu-id="fa992-116">[in]データを受信する単一値のプロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fa992-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="fa992-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="fa992-117">_uliInst_</span></span>
  
> <span data-ttu-id="fa992-118">[in]インスタンス番号は、 _pvalMv_パラメーターで指定された構造体からコピーされる値の配列要素は、です。</span><span class="sxs-lookup"><span data-stu-id="fa992-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa992-119">Return value</span><span class="sxs-lookup"><span data-stu-id="fa992-119">Return value</span></span>

<span data-ttu-id="fa992-120">なし。</span><span class="sxs-lookup"><span data-stu-id="fa992-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa992-121">備考</span><span class="sxs-lookup"><span data-stu-id="fa992-121">Remarks</span></span>

<span data-ttu-id="fa992-122">コピーされる値が割り当てられたメモリに対して大きすぎる場合は、 **GetInstance**関数は新しいメモリの割り当てではなくポインターのみをコピーします。</span><span class="sxs-lookup"><span data-stu-id="fa992-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

