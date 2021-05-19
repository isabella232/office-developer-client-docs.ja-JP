---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347804"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="d85f7-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="d85f7-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="d85f7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d85f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d85f7-105">Microsoft Exchange 2007 サーバーの自動検出サービスから取得された情報を表す拡張可能マークアップ言語 (XML) ストリームを返します。</span><span class="sxs-lookup"><span data-stu-id="d85f7-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d85f7-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d85f7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d85f7-107">次の方法でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="d85f7-107">Exported by:</span></span>  <br/> |<span data-ttu-id="d85f7-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="d85f7-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="d85f7-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d85f7-109">Called by:</span></span>  <br/> |<span data-ttu-id="d85f7-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="d85f7-110">Client</span></span>  <br/> |
|<span data-ttu-id="d85f7-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="d85f7-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="d85f7-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="d85f7-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="d85f7-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d85f7-113">Parameters</span></span>

 <span data-ttu-id="d85f7-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="d85f7-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="d85f7-115">[in]自動検出情報を取得するアカウントの NULL 終端の簡易メール転送プロトコル (SMTP) 電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="d85f7-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="d85f7-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="d85f7-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="d85f7-117">[in]  _pwzAddress_ で指定されたアカウントのオプションのパスワードです。</span><span class="sxs-lookup"><span data-stu-id="d85f7-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="d85f7-118">_pwzAddress_ で指定されたアカウントにパスワードが必要ない場合、パスワードを渡しても効果はありません。</span><span class="sxs-lookup"><span data-stu-id="d85f7-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="d85f7-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="d85f7-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="d85f7-120">[in]オプションであり、操作をキャンセルするために使用できる、設定されていない Win32 イベント ハンドル。</span><span class="sxs-lookup"><span data-stu-id="d85f7-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="d85f7-121">操作をキャンセルするには、イベントを設定し、イベント ハンドルを  _hCancelEvent として渡します_。操作 **をキャンセル** しない場合は null を渡します。</span><span class="sxs-lookup"><span data-stu-id="d85f7-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="d85f7-122">イベント ハンドルを表す値を渡しても効果が無く、関数によって無視されます。</span><span class="sxs-lookup"><span data-stu-id="d85f7-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="d85f7-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d85f7-123">_ulFlags_</span></span>
  
> <span data-ttu-id="d85f7-124">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="d85f7-124">[in] This parameter is not used.</span></span> <span data-ttu-id="d85f7-125">0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d85f7-125">It must be 0.</span></span>
    
 <span data-ttu-id="d85f7-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="d85f7-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="d85f7-127">[out]自動検出 XML を含む [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d85f7-127">[out] A pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="d85f7-128">自動検出 **操作が失敗** した場合は null を返します。</span><span class="sxs-lookup"><span data-stu-id="d85f7-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="d85f7-129">[終了したら、IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d85f7-129">You must release the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d85f7-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="d85f7-130">Return values</span></span>

<span data-ttu-id="d85f7-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="d85f7-131">S_OK</span></span> 
  
- <span data-ttu-id="d85f7-132">関数呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="d85f7-132">The function call is successful.</span></span>
    
<span data-ttu-id="d85f7-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d85f7-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="d85f7-134">_pwzAddress は_ **null** か、有効な SMTP アドレスではないか _、ppXmlStream_ は [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトへの **null** ポインターです。</span><span class="sxs-lookup"><span data-stu-id="d85f7-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="d85f7-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d85f7-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="d85f7-136">クライアント コンピューターがネットワークに接続されていない、クライアント コンピューターが Microsoft Exchange 2007 サーバーに接続されていない _、pwzAddress_ が Exchange 2007 サーバー上のアカウントではない、または _pwzAddress_ が Exchange 自動検出サービスをサポートしていないアカウントです。</span><span class="sxs-lookup"><span data-stu-id="d85f7-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="d85f7-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d85f7-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="d85f7-138">操作を取り消すイベント ハンドルが  _hCancelEvent_ に渡されています。</span><span class="sxs-lookup"><span data-stu-id="d85f7-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="d85f7-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="d85f7-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="d85f7-140">_pwzAddress_ または _pwzPassword_ に渡される値が長すぎるので、サイズ 256 バイトの内部バッファーがオーバーフローします。</span><span class="sxs-lookup"><span data-stu-id="d85f7-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

