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
# <a name="setattribimsgonistg"></a><span data-ttu-id="4c22b-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="4c22b-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="4c22b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c22b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c22b-105">[OpenIMsgOnIStg](openimsgonistg.md)関数によって指定された[IMessage](imessageimapiprop.md)オブジェクトのプロパティの属性を設定または変更します。</span><span class="sxs-lookup"><span data-stu-id="4c22b-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c22b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4c22b-106">Header file:</span></span>  <br/> |<span data-ttu-id="4c22b-107">Imessage</span><span class="sxs-lookup"><span data-stu-id="4c22b-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="4c22b-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="4c22b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4c22b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4c22b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4c22b-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="4c22b-110">Called by:</span></span>  <br/> |<span data-ttu-id="4c22b-111">クライアントアプリケーションとメッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="4c22b-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="4c22b-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4c22b-112">Parameters</span></span>

 <span data-ttu-id="4c22b-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="4c22b-113">_lpObject_</span></span>
  
> <span data-ttu-id="4c22b-114">順番プロパティ属性が設定されているオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4c22b-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="4c22b-115">_lpproptags_</span><span class="sxs-lookup"><span data-stu-id="4c22b-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="4c22b-116">順番プロパティタグの配列が含まれている[SPropTagArray](sproptagarray.md)構造体へのポインター。プロパティの属性が設定されているプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="4c22b-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="4c22b-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="4c22b-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="4c22b-118">順番設定するプロパティ属性を一覧表示する[sproな trarray](spropattrarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4c22b-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="4c22b-119">_lpppropproblems 問題_</span><span class="sxs-lookup"><span data-stu-id="4c22b-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="4c22b-120">読み上げプロパティの問題のセットを含む、返された[sprop問題の配列](spropproblemarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4c22b-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="4c22b-121">この構造体は、 **SetAttribIMsgOnIStg**が一部のプロパティを設定できた場合に発生する問題を特定します。ただし、すべてではありません。</span><span class="sxs-lookup"><span data-stu-id="4c22b-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="4c22b-122">_lpppropproblems_パラメーターに NULL へのポインターが渡された場合、一部のプロパティが設定されていない場合でも、プロパティ問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="4c22b-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4c22b-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="4c22b-123">Return value</span></span>

<span data-ttu-id="4c22b-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c22b-124">S_OK</span></span> 
  
> <span data-ttu-id="4c22b-125">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="4c22b-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4c22b-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="4c22b-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="4c22b-127">呼び出しは全体的に成功しましたが、1つ以上のプロパティがアクセスできず、PT_ERROR のプロパティの種類で返されました。</span><span class="sxs-lookup"><span data-stu-id="4c22b-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c22b-128">注釈</span><span class="sxs-lookup"><span data-stu-id="4c22b-128">Remarks</span></span>

<span data-ttu-id="4c22b-129">property 属性は、プロパティオブジェクト (つまり、 [imapiprop: IUnknown](imapipropiunknown.md)インターフェイスを実装するオブジェクト) にのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4c22b-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="4c22b-130">ole 構造化ストレージオブジェクトで MAPI プロパティを使用できるようにするために、 [OpenIMsgOnIStg](openimsgonistg.md)は、ole **IStorage**オブジェクトの先頭に[IMessage: imapiprop](imessageimapiprop.md)オブジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="4c22b-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="4c22b-131">このようなオブジェクトのプロパティ属性は、 **SetAttribIMsgOnIStg**を使用して設定または変更したり、 [GetAttribIMsgOnIStg](getattribimsgonistg.md)で取得したりできます。</span><span class="sxs-lookup"><span data-stu-id="4c22b-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="4c22b-132">**メモ\*\*\*\*GetAttribIMsgOnIStg**および**SetAttribIMsgOnIStg**は、すべての**IMessage**オブジェクトでは動作しません。</span><span class="sxs-lookup"><span data-stu-id="4c22b-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="4c22b-133">これらは、 **OpenIMsgOnIStg**によって返される\*\*\*\* **IMessage**オブジェクトに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="4c22b-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="4c22b-134">_lpPropAttrs_パラメーターでは、属性の数と位置が、 _lpproptags_パラメーターで渡されるプロパティタグの数と位置に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c22b-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="4c22b-135">**SetAttribIMsgOnIStg**関数は、 **IMessage**スキーマで必要な場合にメッセージプロパティを読み取り専用にするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4c22b-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="4c22b-136">サンプルメッセージストアプロバイダーは、これを目的として使用します。</span><span class="sxs-lookup"><span data-stu-id="4c22b-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="4c22b-137">詳細については、「[メッセージ](mapi-messages.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c22b-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

