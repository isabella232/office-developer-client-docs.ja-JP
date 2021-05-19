---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411009"
---
# <a name="sccopyprops"></a><span data-ttu-id="7ca25-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="7ca25-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="7ca25-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ca25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ca25-105">[SPropValue](spropvalue.md)構造体の配列で定義されたプロパティを新しい宛先にコピーします。</span><span class="sxs-lookup"><span data-stu-id="7ca25-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ca25-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7ca25-106">Header file:</span></span>  <br/> |<span data-ttu-id="7ca25-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7ca25-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7ca25-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="7ca25-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7ca25-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7ca25-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7ca25-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="7ca25-110">Called by:</span></span>  <br/> |<span data-ttu-id="7ca25-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="7ca25-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="7ca25-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7ca25-112">Parameters</span></span>

 <span data-ttu-id="7ca25-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="7ca25-113">_cprop_</span></span>
  
> <span data-ttu-id="7ca25-114">[in]コピーするプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="7ca25-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="7ca25-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="7ca25-115">_rgprop_</span></span>
  
> <span data-ttu-id="7ca25-116">[in]コピーするプロパティを [定義する SPropValue](spropvalue.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7ca25-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="7ca25-117">_rgprop パラメーター_ は、配列の先頭を指す必要はないが、配列内の **SPropValue** 構造体の 1 つの先頭を指している必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ca25-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="7ca25-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="7ca25-118">_pvDst_</span></span>
  
> <span data-ttu-id="7ca25-119">[in]この関数がプロパティをコピーするメモリ内の初期位置へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7ca25-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="7ca25-120">_pcb_</span><span class="sxs-lookup"><span data-stu-id="7ca25-120">_pcb_</span></span>
  
> <span data-ttu-id="7ca25-121">[out]  _pvDst_ パラメーターが指すメモリ ブロックのサイズ (バイト単位) へのオプションのポインター。</span><span class="sxs-lookup"><span data-stu-id="7ca25-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7ca25-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="7ca25-122">Return value</span></span>

<span data-ttu-id="7ca25-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ca25-123">S_OK</span></span>
  
> <span data-ttu-id="7ca25-124">プロパティが正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="7ca25-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="7ca25-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7ca25-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="7ca25-126">不明なプロパティの種類が検出されました。</span><span class="sxs-lookup"><span data-stu-id="7ca25-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ca25-127">注釈</span><span class="sxs-lookup"><span data-stu-id="7ca25-127">Remarks</span></span>

<span data-ttu-id="7ca25-128">新しい配列とそのデータは、1 つの割り当てで作成されたバッファー内に存在し [、ScRelocProps](screlocprops.md) 関数を使用して、個々の [SPropValue](spropvalue.md) 構造体のポインターを調整できます。</span><span class="sxs-lookup"><span data-stu-id="7ca25-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="7ca25-129">この調整の前に、ポインターは有効です。</span><span class="sxs-lookup"><span data-stu-id="7ca25-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="7ca25-130">**ScCopyProps は** 、コピーされたプロパティ配列の元のプロパティの順序を維持します。</span><span class="sxs-lookup"><span data-stu-id="7ca25-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="7ca25-131">_pcb パラメーター_ は省略可能です。NULL 以外の場合は _、pvDst_ パラメーターに格納されているバイト数に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7ca25-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ca25-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="7ca25-132">See also</span></span>



[<span data-ttu-id="7ca25-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="7ca25-133">ScDupPropset</span></span>](scduppropset.md)

