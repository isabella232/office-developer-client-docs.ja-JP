---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: 優先される文字の形式では、クライアントがアクセスできるオブジェクトを作成します。
ms.openlocfilehash: 187bcbce8fd1170e05f57c5c9147a8962669fea4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799319"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="46f42-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="46f42-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="46f42-104">優先される文字の形式では、クライアントがアクセスできるオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="46f42-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="46f42-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="46f42-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46f42-106">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="46f42-106">Exported by:</span></span>  <br/> |<span data-ttu-id="46f42-107">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="46f42-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="46f42-108">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46f42-108">Called by:</span></span>  <br/> |<span data-ttu-id="46f42-109">クライアント</span><span class="sxs-lookup"><span data-stu-id="46f42-109">Client</span></span>  <br/> |
|<span data-ttu-id="46f42-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="46f42-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="46f42-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="46f42-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a><span data-ttu-id="46f42-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="46f42-112">Parameters</span></span>

<span data-ttu-id="46f42-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="46f42-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="46f42-114">[in]最初のラップが解除された Outlook オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="46f42-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="46f42-115">次のインタ フェースのいずれかを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46f42-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="46f42-116">[IMailUser: IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx)、 [IMAPIFolder: IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx)、 [IMessage: IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx)、 [IMsgStore: IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx)、 [IMSLogon: IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)、または[IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="46f42-116">[IMailUser : IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="46f42-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="46f42-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="46f42-118">[in]ラップの最初のオブジェクトの特性を示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="46f42-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="46f42-119">次の値の 1 つ以上にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="46f42-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="46f42-120">DDLWRAP_FLAG_ANSI-Unwrapped オブジェクトは、ANSI です。</span><span class="sxs-lookup"><span data-stu-id="46f42-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="46f42-121">DDLWRAP_FLAG_UNICODE-Unwrapped オブジェクトには、UNICODE です。</span><span class="sxs-lookup"><span data-stu-id="46f42-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="46f42-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="46f42-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="46f42-123">[in]優先文字形式のフラグ。</span><span class="sxs-lookup"><span data-stu-id="46f42-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="46f42-124">次の値の 1 つ以上にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="46f42-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="46f42-125">DDLWRAP_FLAG_ANSI-Wrapped オブジェクトは、ANSI として公開されます。</span><span class="sxs-lookup"><span data-stu-id="46f42-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="46f42-126">DDLWRAP_FLAG_UNICODE-Wrapped オブジェクトを UNICODE として公開されます。</span><span class="sxs-lookup"><span data-stu-id="46f42-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="46f42-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="46f42-127">_pIID_</span></span>
  
>  <span data-ttu-id="46f42-128">[in]ラップが解除されたオブジェクトでサポートされているインターフェイスの識別子これが不明な場合は、NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="46f42-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="46f42-129">_pulReserved_</span><span class="sxs-lookup"><span data-stu-id="46f42-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="46f42-130">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="46f42-130">[in] This parameter is not used.</span></span> <span data-ttu-id="46f42-131">NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="46f42-131">It must be NULL.</span></span> 
    
<span data-ttu-id="46f42-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="46f42-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="46f42-133">[in]テキストを折り返すには、その形式の_pvUnwrapped_をチェックする必要がある場合、このパラメーターを**true**に設定します。オブジェクトをチェックすることがなく折り返す必要がある場合は、 **false**に設定します。</span><span class="sxs-lookup"><span data-stu-id="46f42-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="46f42-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="46f42-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="46f42-135">[out]要求された文字の形式で、要求されたオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="46f42-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="46f42-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="46f42-136">Return values</span></span>

<span data-ttu-id="46f42-137">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="46f42-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46f42-138">解釈</span><span class="sxs-lookup"><span data-stu-id="46f42-138">Remarks</span></span>

<span data-ttu-id="46f42-139">_FCheckWrap_を**true**に設定すると、ラップされたオブジェクトを渡すことは、ラップが解除されたオブジェクトになります。</span><span class="sxs-lookup"><span data-stu-id="46f42-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="46f42-140">、返されたオブジェクトをラップするかどうかに関係なくクライアントでは、返されるオブジェクトの参照を解放する必要が。</span><span class="sxs-lookup"><span data-stu-id="46f42-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="46f42-141">Msmapi32.dll のこの関数のアドレスを検索するには、 **GetProcAddress**を使用して、プロシージャ名として**HrCreateNewWrappedObject@28**を指定します。</span><span class="sxs-lookup"><span data-stu-id="46f42-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46f42-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="46f42-142">See also</span></span>

- [<span data-ttu-id="46f42-143">データの劣化層 API について</span><span class="sxs-lookup"><span data-stu-id="46f42-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="46f42-144">定数 (データの劣化層 API)</span><span class="sxs-lookup"><span data-stu-id="46f42-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

