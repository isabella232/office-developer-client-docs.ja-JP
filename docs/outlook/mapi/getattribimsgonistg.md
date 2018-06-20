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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ddb6d692a8e76a9c24affc3af9f612a6f1c0d769
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800155"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="1abf7-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="1abf7-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="1abf7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1abf7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1abf7-105">[OpenIMsgOnIStg](openimsgonistg.md)関数によって提供された[IMessage](imessageimapiprop.md)オブジェクトのプロパティの属性を取得します。</span><span class="sxs-lookup"><span data-stu-id="1abf7-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1abf7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1abf7-106">Header file:</span></span>  <br/> |<span data-ttu-id="1abf7-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="1abf7-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="1abf7-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="1abf7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1abf7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1abf7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1abf7-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1abf7-110">Called by:</span></span>  <br/> |<span data-ttu-id="1abf7-111">クライアント アプリケーション、およびメッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1abf7-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="1abf7-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="1abf7-112">Parameters</span></span>

 <span data-ttu-id="1abf7-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="1abf7-113">_lpObject_</span></span>
  
> <span data-ttu-id="1abf7-114">[in][OpenIMsgOnIStg](openimsgonistg.md)関数から取得した**IMessage**オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1abf7-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="1abf7-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="1abf7-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="1abf7-116">[in]取得する対象の属性は、プロパティを示すプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1abf7-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="1abf7-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="1abf7-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="1abf7-118">[out]取得したプロパティの属性を格納する返された[SPropAttrArray](spropattrarray.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1abf7-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1abf7-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1abf7-119">Return value</span></span>

<span data-ttu-id="1abf7-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="1abf7-120">S_OK</span></span> 
  
> <span data-ttu-id="1abf7-121">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="1abf7-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="1abf7-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="1abf7-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="1abf7-123">呼び出しは完了しましたが、1 つまたは複数のプロパティにアクセスできませんでしたし、PT_ERROR のプロパティの種類と返されました。</span><span class="sxs-lookup"><span data-stu-id="1abf7-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1abf7-124">備考</span><span class="sxs-lookup"><span data-stu-id="1abf7-124">Remarks</span></span>

<span data-ttu-id="1abf7-125">プロパティの属性は、プロパティ オブジェクト、つまり、オブジェクトを実装することでのみアクセスできます、 [IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="1abf7-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="1abf7-126">[OpenIMsgOnIStg](openimsgonistg.md)ビルドの MAPI プロパティを OLE 構造化ストレージ オブジェクトで使用できるようにするのには、 [IMessage: IMAPIProp](imessageimapiprop.md) OLE **IStorage**オブジェクト上にあるオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="1abf7-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="1abf7-127">このようなオブジェクトのプロパティの属性の設定または[SetAttribIMsgOnIStg](setattribimsgonistg.md)に変更し、 **GetAttribIMsgOnIStg**を取得します。</span><span class="sxs-lookup"><span data-stu-id="1abf7-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1abf7-128">**IMessage**オブジェクトのすべては、 **GetAttribIMsgOnIStg**と**SetAttribIMsgOnIStg**は動作しません。</span><span class="sxs-lookup"><span data-stu-id="1abf7-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="1abf7-129">-点灯 - **OpenIMsgOnIStg**によって返される**IStorage**オブジェクトは、 **IMessage**に対して有効であるだけです。</span><span class="sxs-lookup"><span data-stu-id="1abf7-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="1abf7-130">数と、 _lppPropAttrArray_パラメーター内の属性の位置の数と、 _lpPropTagArray_パラメーター内のプロパティ タグの位置に対応します。</span><span class="sxs-lookup"><span data-stu-id="1abf7-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

