---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: クライアントが優先文字形式でアクセスできるオブジェクトを作成します。
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317606"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="ff1d8-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="ff1d8-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="ff1d8-104">クライアントが優先文字形式でアクセスできるオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ff1d8-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="ff1d8-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff1d8-106">次の方法でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-106">Exported by:</span></span>  <br/> |<span data-ttu-id="ff1d8-107">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="ff1d8-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="ff1d8-108">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ff1d8-108">Called by:</span></span>  <br/> |<span data-ttu-id="ff1d8-109">クライアント</span><span class="sxs-lookup"><span data-stu-id="ff1d8-109">Client</span></span>  <br/> |
|<span data-ttu-id="ff1d8-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="ff1d8-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff1d8-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="ff1d8-111">Outlook</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="ff1d8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ff1d8-112">Parameters</span></span>

<span data-ttu-id="ff1d8-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="ff1d8-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="ff1d8-114">[in]最初にラップされていないオブジェクトOutlookします。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="ff1d8-115">次のいずれかのインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="ff1d8-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ff1d8-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="ff1d8-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="ff1d8-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="ff1d8-118">[in]ラップされていない初期オブジェクトを特徴付けるフラグ。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="ff1d8-119">次の値の 1 つ以上を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="ff1d8-120">DDLWRAP_FLAG_ANSI- アンラップされたオブジェクトは ANSI です。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="ff1d8-121">DDLWRAP_FLAG_UNICODE- アンラップされたオブジェクトは UNICODE です。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="ff1d8-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="ff1d8-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="ff1d8-123">[in]優先文字形式のフラグ。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="ff1d8-124">次の値の 1 つ以上を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="ff1d8-125">DDLWRAP_FLAG_ANSI- ラップされたオブジェクトは ANSI として公開されます。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="ff1d8-126">DDLWRAP_FLAG_UNICODE- ラップされたオブジェクトは UNICODE として公開されます。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="ff1d8-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="ff1d8-127">_pIID_</span></span>
  
>  <span data-ttu-id="ff1d8-128">[in]ラップされていないオブジェクトでサポートされるインターフェイスの識別子。不明な場合は NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="ff1d8-129">_pulReserved_</span><span class="sxs-lookup"><span data-stu-id="ff1d8-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="ff1d8-130">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-130">[in] This parameter is not used.</span></span> <span data-ttu-id="ff1d8-131">NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-131">It must be NULL.</span></span> 
    
<span data-ttu-id="ff1d8-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="ff1d8-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="ff1d8-133">[in]_pvUnwrapped_**をラップ** する前に形式をチェックする必要がある場合は、このパラメーターを true に設定します。オブジェクトをチェック **せずにラップ** する場合は false に設定します。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="ff1d8-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="ff1d8-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="ff1d8-135">[out]要求された文字形式でラップされた、要求されたオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="ff1d8-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="ff1d8-136">Return values</span></span>

<span data-ttu-id="ff1d8-137">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff1d8-138">注釈</span><span class="sxs-lookup"><span data-stu-id="ff1d8-138">Remarks</span></span>

<span data-ttu-id="ff1d8-139">_fCheckWrap_ が true に設定されたラップされたオブジェクトを渡す **場合、ラップ** されていないオブジェクトになります。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="ff1d8-140">返されるオブジェクトがラップされるかどうかに関係なく、クライアントは返されたオブジェクトの参照を解放します。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="ff1d8-141">**GetProcAddress** を使用してこの関数のアドレスを検索する場合は **msmapi32.dllプロシージャHrCreateNewWrappedObject@28** として指定します。</span><span class="sxs-lookup"><span data-stu-id="ff1d8-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff1d8-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff1d8-142">See also</span></span>

- [<span data-ttu-id="ff1d8-143">データの劣化層 API について</span><span class="sxs-lookup"><span data-stu-id="ff1d8-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="ff1d8-144">定数 (データ低下層 API)</span><span class="sxs-lookup"><span data-stu-id="ff1d8-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

