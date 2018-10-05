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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400720"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="79c12-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="79c12-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="79c12-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79c12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79c12-105">Microsoft Exchange 2007 サーバーの自動検出サービスから取得した情報を表す拡張マークアップ言語 (XML) のストリームを返します。</span><span class="sxs-lookup"><span data-stu-id="79c12-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="79c12-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="79c12-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79c12-107">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="79c12-107">Exported by:</span></span>  <br/> |<span data-ttu-id="79c12-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="79c12-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="79c12-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="79c12-109">Called by:</span></span>  <br/> |<span data-ttu-id="79c12-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="79c12-110">Client</span></span>  <br/> |
|<span data-ttu-id="79c12-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="79c12-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="79c12-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="79c12-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="79c12-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="79c12-113">Parameters</span></span>

 <span data-ttu-id="79c12-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="79c12-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="79c12-115">[in]Null で終わる簡易メール転送プロトコル (SMTP) メール アドレスの自動検出情報を取得するアカウントです。</span><span class="sxs-lookup"><span data-stu-id="79c12-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="79c12-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="79c12-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="79c12-117">[in]オプションの_pwzAddress_で指定されたアカウントのパスワードです。</span><span class="sxs-lookup"><span data-stu-id="79c12-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="79c12-118">任意のパスワードを渡す意味を持ちません_pwzAddress_によって指定されたアカウントにパスワードが必要ない場合に注意してください。</span><span class="sxs-lookup"><span data-stu-id="79c12-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="79c12-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="79c12-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="79c12-120">[in]設定されていない Win32 イベント ハンドルをオプションで、操作をキャンセルするために使用します。</span><span class="sxs-lookup"><span data-stu-id="79c12-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="79c12-121">操作をキャンセルするには、イベントを設定し、イベント ハンドルを渡すと_hCancelEvent_。操作をキャンセルしたくない場合は**null**を渡します。</span><span class="sxs-lookup"><span data-stu-id="79c12-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="79c12-122">メモがある値を渡すことはありません、イベント ハンドルは、影響を与えません、関数では無視されます。</span><span class="sxs-lookup"><span data-stu-id="79c12-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="79c12-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="79c12-123">_ulFlags_</span></span>
  
> <span data-ttu-id="79c12-124">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="79c12-124">[in] This parameter is not used.</span></span> <span data-ttu-id="79c12-125">0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="79c12-125">It must be 0.</span></span>
    
 <span data-ttu-id="79c12-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="79c12-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="79c12-127">[out]自動検出の XML を含む[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="79c12-127">[out] A pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="79c12-128">自動検出が失敗した場合は**null**を返します。</span><span class="sxs-lookup"><span data-stu-id="79c12-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="79c12-129">操作を終了したら、 [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79c12-129">You must release the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="79c12-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="79c12-130">Return values</span></span>

<span data-ttu-id="79c12-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="79c12-131">S_OK</span></span> 
  
- <span data-ttu-id="79c12-132">関数の呼び出しが成功します。</span><span class="sxs-lookup"><span data-stu-id="79c12-132">The function call is successful.</span></span>
    
<span data-ttu-id="79c12-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="79c12-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="79c12-134">_pwzAddress_が**null**か、有効な SMTP アドレスではありませんか_ppXmlStream_ [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトへの**null**ポインター。</span><span class="sxs-lookup"><span data-stu-id="79c12-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="79c12-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="79c12-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="79c12-136">クライアント コンピューターがネットワークに接続されていない、Microsoft Exchange 2007 サーバーにクライアント コンピューターが接続されていない、 _pwzAddress_は、Exchange 2007 サーバー上のアカウントではありません、または_pwzAddress_は、Exchange でサポートされていないアカウント自動検出サービスです。</span><span class="sxs-lookup"><span data-stu-id="79c12-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="79c12-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="79c12-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="79c12-138">イベント ハンドルは、操作をキャンセルするのには_hCancelEvent_に渡されました。</span><span class="sxs-lookup"><span data-stu-id="79c12-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="79c12-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="79c12-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="79c12-140">_PwzAddress_または_pwzPassword_に渡される値が長すぎます、256 バイトのサイズの内部バッファーがオーバーフローしたことなどです。</span><span class="sxs-lookup"><span data-stu-id="79c12-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

