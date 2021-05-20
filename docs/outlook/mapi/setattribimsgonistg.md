---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428831"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="789c7-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="789c7-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="789c7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="789c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="789c7-105">[OpenIMsgOnIStg](openimsgonistg.md)関数によって提供される[IMessage](imessageimapiprop.md)オブジェクトのプロパティの属性を設定または変更します。</span><span class="sxs-lookup"><span data-stu-id="789c7-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="789c7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="789c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="789c7-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="789c7-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="789c7-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="789c7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="789c7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="789c7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="789c7-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="789c7-110">Called by:</span></span>  <br/> |<span data-ttu-id="789c7-111">クライアント アプリケーションとメッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="789c7-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="789c7-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="789c7-112">Parameters</span></span>

 <span data-ttu-id="789c7-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="789c7-113">_lpObject_</span></span>
  
> <span data-ttu-id="789c7-114">[in]プロパティ属性が設定されているオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="789c7-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="789c7-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="789c7-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="789c7-116">[in]プロパティ属性が設定されているプロパティを示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="789c7-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="789c7-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="789c7-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="789c7-118">[in]設定する [プロパティ属性を示す SPropAttrArray](spropattrarray.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="789c7-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="789c7-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="789c7-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="789c7-120">[out]プロパティの問題のセットを含む、返される [SPropProblemArray](spropproblemarray.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="789c7-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="789c7-121">この構造は **、SetAttribIMsgOnIStg** が一部のプロパティを設定できたが、すべてではない場合に発生する問題を識別します。</span><span class="sxs-lookup"><span data-stu-id="789c7-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="789c7-122">_lppPropProblems_ パラメーターに NULL へのポインターが渡された場合、一部のプロパティが設定されていない場合でも、プロパティの問題配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="789c7-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="789c7-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="789c7-123">Return value</span></span>

<span data-ttu-id="789c7-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="789c7-124">S_OK</span></span> 
  
> <span data-ttu-id="789c7-125">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="789c7-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="789c7-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="789c7-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="789c7-127">呼び出しは全体的に成功しましたが、1 つ以上のプロパティにアクセスする必要が生じ、プロパティの種類が変更されたPT_ERROR。</span><span class="sxs-lookup"><span data-stu-id="789c7-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="789c7-128">注釈</span><span class="sxs-lookup"><span data-stu-id="789c7-128">Remarks</span></span>

<span data-ttu-id="789c7-129">プロパティ属性にアクセスできるのは、プロパティ オブジェクト、つまり [IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスを実装するオブジェクトのみです。</span><span class="sxs-lookup"><span data-stu-id="789c7-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="789c7-130">OLE 構造化ストレージ オブジェクトで MAPI プロパティを使用するために [、OpenIMsgOnIStg](openimsgonistg.md)は OLE **IStorage** オブジェクトの上に [IMessage : IMAPIProp](imessageimapiprop.md)オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="789c7-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="789c7-131">このようなオブジェクトのプロパティ属性は **、SetAttribIMsgOnIStg** を使用して設定または変更し [、GetAttribIMsgOnIStg](getattribimsgonistg.md)を使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="789c7-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="789c7-132">**メモ\*\*\*\*GetAttribIMsgOnIStg** および **SetAttribIMsgOnIStg** は、すべての **IMessage オブジェクトで動作しません**。</span><span class="sxs-lookup"><span data-stu-id="789c7-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="789c7-133">これらは **、OpenIMsgOnIStg** によって返される **IMessage**-on- **IStorage** オブジェクトでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="789c7-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="789c7-134">_lpPropAttrs_ パラメーターでは、属性の数と位置が _lpPropTags_ パラメーターで渡されるプロパティ タグの数と位置と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="789c7-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="789c7-135">**SetAttribIMsgOnIStg** 関数は、IMessage スキーマで必要なときにメッセージ プロパティを読み取り **専用にするために使用** されます。</span><span class="sxs-lookup"><span data-stu-id="789c7-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="789c7-136">サンプル メッセージ ストア プロバイダーは、この目的のためにそれを使用します。</span><span class="sxs-lookup"><span data-stu-id="789c7-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="789c7-137">詳細については、「Messages」を [参照してください](mapi-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="789c7-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

