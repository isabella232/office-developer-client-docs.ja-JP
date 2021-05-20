---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439997"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="e4fb2-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="e4fb2-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="e4fb2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4fb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4fb2-105">[OpenIMsgOnIStg](openimsgonistg.md)関数によって指定された[IMessage](imessageimapiprop.md)オブジェクトのプロパティの属性を取得します。</span><span class="sxs-lookup"><span data-stu-id="e4fb2-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4fb2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e4fb2-106">Header file:</span></span>  <br/> |<span data-ttu-id="e4fb2-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="e4fb2-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="e4fb2-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="e4fb2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e4fb2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e4fb2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e4fb2-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e4fb2-110">Called by:</span></span>  <br/> |<span data-ttu-id="e4fb2-111">クライアント アプリケーションとメッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e4fb2-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="e4fb2-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e4fb2-112">Parameters</span></span>

 <span data-ttu-id="e4fb2-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="e4fb2-113">_lpObject_</span></span>
  
> <span data-ttu-id="e4fb2-114">[in][OpenIMsgOnIStg](openimsgonistg.md)関数から取得した **IMessage** オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e4fb2-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="e4fb2-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="e4fb2-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="e4fb2-116">[in]取得する属性のプロパティを示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e4fb2-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="e4fb2-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="e4fb2-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="e4fb2-118">[out]取得したプロパティ属性を含む [、返される SPropAttrArray](spropattrarray.md) 構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e4fb2-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e4fb2-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="e4fb2-119">Return value</span></span>

<span data-ttu-id="e4fb2-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="e4fb2-120">S_OK</span></span> 
  
> <span data-ttu-id="e4fb2-121">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e4fb2-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e4fb2-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="e4fb2-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="e4fb2-123">呼び出しは全体的に成功しましたが、1 つ以上のプロパティにアクセスする必要が生じ、プロパティの種類が変更されたPT_ERROR。</span><span class="sxs-lookup"><span data-stu-id="e4fb2-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e4fb2-124">注釈</span><span class="sxs-lookup"><span data-stu-id="e4fb2-124">Remarks</span></span>

<span data-ttu-id="e4fb2-125">プロパティ属性にアクセスできるのは、プロパティ オブジェクト、つまり [IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスを実装するオブジェクトのみです。</span><span class="sxs-lookup"><span data-stu-id="e4fb2-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="e4fb2-126">OLE 構造化ストレージ オブジェクトで MAPI プロパティを使用するために [、OpenIMsgOnIStg](openimsgonistg.md)は OLE **IStorage** オブジェクトの上に [IMessage : IMAPIProp](imessageimapiprop.md)オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="e4fb2-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="e4fb2-127">このようなオブジェクトのプロパティ属性は [、SetAttribIMsgOnIStg](setattribimsgonistg.md) を使用して設定または変更し **、GetAttribIMsgOnIStg** を使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="e4fb2-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e4fb2-128">**GetAttribIMsgOnIStg** および **SetAttribIMsgOnIStg** は、すべての **IMessage オブジェクトで動作しません** 。</span><span class="sxs-lookup"><span data-stu-id="e4fb2-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="e4fb2-129">これらは **、OpenIMsgOnIStg** によって返される **IMessage**-on- **IStorage** オブジェクトでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="e4fb2-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="e4fb2-130">_lppPropAttrArray_ パラメーター内の属性の数と位置は _、lpPropTagArray_ パラメーター内のプロパティ タグの数と位置に対応します。</span><span class="sxs-lookup"><span data-stu-id="e4fb2-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

