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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e8a0daa2afe2397f39b7f37a31ef718ba65a3350
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803890"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="6026f-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="6026f-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="6026f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6026f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6026f-105">[OpenIMsgOnIStg](openimsgonistg.md)関数によって提供された[IMessage](imessageimapiprop.md)オブジェクトのプロパティの属性を変更または設定します。</span><span class="sxs-lookup"><span data-stu-id="6026f-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6026f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6026f-106">Header file:</span></span>  <br/> |<span data-ttu-id="6026f-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="6026f-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="6026f-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6026f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6026f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6026f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6026f-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6026f-110">Called by:</span></span>  <br/> |<span data-ttu-id="6026f-111">クライアント アプリケーション、およびメッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6026f-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="6026f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="6026f-112">Parameters</span></span>

 <span data-ttu-id="6026f-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="6026f-113">_lpObject_</span></span>
  
> <span data-ttu-id="6026f-114">[in]属性が設定されているプロパティのオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6026f-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="6026f-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="6026f-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="6026f-116">[in]属性が設定されているプロパティのプロパティを示すプロパティ タグの配列を格納する[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6026f-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="6026f-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="6026f-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="6026f-118">[in]設定するプロパティの属性を一覧表示する[SPropAttrArray](spropattrarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6026f-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="6026f-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="6026f-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="6026f-120">[out]返された[SPropProblemArray](spropproblemarray.md)構造体のプロパティの問題のセットが含まれているへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6026f-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="6026f-121">この構造体は、 **SetAttribIMsgOnIStg**は、すべてではなく、一部のプロパティを設定することをされている場合に発生する問題を識別します。</span><span class="sxs-lookup"><span data-stu-id="6026f-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="6026f-122">_LppPropProblems_パラメーターに null ポインターが渡されると場合、は、いくつかのプロパティが設定されていない場合でもにプロパティの問題の配列が返されません。</span><span class="sxs-lookup"><span data-stu-id="6026f-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6026f-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6026f-123">Return value</span></span>

<span data-ttu-id="6026f-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="6026f-124">S_OK</span></span> 
  
> <span data-ttu-id="6026f-125">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="6026f-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6026f-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="6026f-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="6026f-127">呼び出しは完了しましたが、1 つまたは複数のプロパティにアクセスできませんでしたし、PT_ERROR のプロパティの種類と返されました。</span><span class="sxs-lookup"><span data-stu-id="6026f-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6026f-128">備考</span><span class="sxs-lookup"><span data-stu-id="6026f-128">Remarks</span></span>

<span data-ttu-id="6026f-129">プロパティの属性は、プロパティ オブジェクト、つまり、オブジェクトを実装することでのみアクセスできます、 [IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="6026f-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="6026f-130">[OpenIMsgOnIStg](openimsgonistg.md)ビルドの MAPI プロパティを OLE 構造化ストレージ オブジェクトで使用できるようにするのには、 [IMessage: IMAPIProp](imessageimapiprop.md) OLE **IStorage**オブジェクト上にあるオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="6026f-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="6026f-131">このようなオブジェクトのプロパティの属性の設定または**SetAttribIMsgOnIStg**に変更し、 [GetAttribIMsgOnIStg](getattribimsgonistg.md)を取得します。</span><span class="sxs-lookup"><span data-stu-id="6026f-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="6026f-132">**メモ****IMessage**オブジェクトのすべては、 **GetAttribIMsgOnIStg**と**SetAttribIMsgOnIStg**は動作しません。</span><span class="sxs-lookup"><span data-stu-id="6026f-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="6026f-133">-点灯 - **OpenIMsgOnIStg**によって返される**IStorage**オブジェクトは、 **IMessage**に対して有効であるだけです。</span><span class="sxs-lookup"><span data-stu-id="6026f-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="6026f-134">_LpPropAttrs_パラメーターに番号と、属性の位置は数と、 _lpPropTags_パラメーターで渡されたプロパティ タグの位置が可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6026f-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="6026f-135">**SetAttribIMsgOnIStg**関数を使用して、メッセージのプロパティを**IMessage**スキーマで必要なときは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="6026f-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="6026f-136">サンプル メッセージ ストア プロバイダーは、この目的で使用します。</span><span class="sxs-lookup"><span data-stu-id="6026f-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="6026f-137">詳細については、[メッセージ](mapi-messages.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6026f-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

