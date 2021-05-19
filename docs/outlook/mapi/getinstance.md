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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418723"
---
# <a name="getinstance"></a><span data-ttu-id="6804d-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="6804d-103">GetInstance</span></span>

  
  
<span data-ttu-id="6804d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6804d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6804d-105">複数値プロパティ内の 1 つの値を、同じ型の単一値プロパティにコピーします。</span><span class="sxs-lookup"><span data-stu-id="6804d-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6804d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6804d-106">Header file:</span></span>  <br/> |<span data-ttu-id="6804d-107">MAPIUTIL。H</span><span class="sxs-lookup"><span data-stu-id="6804d-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="6804d-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="6804d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6804d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6804d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6804d-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="6804d-110">Called by:</span></span>  <br/> |<span data-ttu-id="6804d-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6804d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="6804d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6804d-112">Parameters</span></span>

 <span data-ttu-id="6804d-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="6804d-113">_pvalMv_</span></span>
  
> <span data-ttu-id="6804d-114">[in]複数値プロパティ [を定義する SPropValue](spropvalue.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6804d-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="6804d-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="6804d-115">_pvalSv_</span></span>
  
> <span data-ttu-id="6804d-116">[in]データを受信する単一値プロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6804d-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="6804d-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="6804d-117">_uliInst_</span></span>
  
> <span data-ttu-id="6804d-118">[in]  _pvalMv_ パラメーターで示される構造体からコピーされる値のインスタンス番号 (配列要素)。</span><span class="sxs-lookup"><span data-stu-id="6804d-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6804d-119">Return value</span><span class="sxs-lookup"><span data-stu-id="6804d-119">Return value</span></span>

<span data-ttu-id="6804d-120">なし。</span><span class="sxs-lookup"><span data-stu-id="6804d-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6804d-121">注釈</span><span class="sxs-lookup"><span data-stu-id="6804d-121">Remarks</span></span>

<span data-ttu-id="6804d-122">コピーされた値が割り当てられたメモリに対して大きすぎる場合 **、GetInstance** 関数は、新しいメモリを割り当てる代わりにポインターのみをコピーします。</span><span class="sxs-lookup"><span data-stu-id="6804d-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

