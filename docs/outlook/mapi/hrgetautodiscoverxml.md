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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: da466fc9add8cbc385014782f31749d3b6522da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800289"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="49f6a-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="49f6a-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="49f6a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49f6a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49f6a-105">Microsoft Exchange 2007 サーバーの自動検出サービスから取得した情報を表す拡張マークアップ言語 (XML) のストリームを返します。</span><span class="sxs-lookup"><span data-stu-id="49f6a-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="49f6a-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="49f6a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49f6a-107">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="49f6a-107">Exported by:</span></span>  <br/> |<span data-ttu-id="49f6a-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="49f6a-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="49f6a-109">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="49f6a-109">Called by:</span></span>  <br/> |<span data-ttu-id="49f6a-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="49f6a-110">Client</span></span>  <br/> |
|<span data-ttu-id="49f6a-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="49f6a-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="49f6a-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="49f6a-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="49f6a-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="49f6a-113">Parameters</span></span>

 <span data-ttu-id="49f6a-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="49f6a-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="49f6a-115">[in]Null で終わる簡易メール転送プロトコル (SMTP) メール アドレスの自動検出情報を取得するアカウントです。</span><span class="sxs-lookup"><span data-stu-id="49f6a-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="49f6a-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="49f6a-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="49f6a-117">[in]オプションの_pwzAddress_で指定されたアカウントのパスワードです。</span><span class="sxs-lookup"><span data-stu-id="49f6a-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="49f6a-118">任意のパスワードを渡す意味を持ちません_pwzAddress_によって指定されたアカウントにパスワードが必要ない場合に注意してください。</span><span class="sxs-lookup"><span data-stu-id="49f6a-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="49f6a-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="49f6a-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="49f6a-120">[in]設定されていない Win32 イベント ハンドルをオプションで、操作をキャンセルするために使用します。</span><span class="sxs-lookup"><span data-stu-id="49f6a-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="49f6a-121">操作をキャンセルするには、イベントを設定し、イベント ハンドルを渡すと_hCancelEvent_。操作をキャンセルしたくない場合は**null**を渡します。</span><span class="sxs-lookup"><span data-stu-id="49f6a-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="49f6a-122">メモがある値を渡すことはありません、イベント ハンドルは、影響を与えません、関数では無視されます。</span><span class="sxs-lookup"><span data-stu-id="49f6a-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="49f6a-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="49f6a-123">_ulFlags_</span></span>
  
> <span data-ttu-id="49f6a-124">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="49f6a-124">[in] This parameter is not used.</span></span> <span data-ttu-id="49f6a-125">0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f6a-125">It must be 0.</span></span>
    
 <span data-ttu-id="49f6a-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="49f6a-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="49f6a-127">[out]自動検出の XML を含む[IStream](http://msdn.microsoft.com/ja-jp/library/aa380034%28VS.85%29.aspx)オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="49f6a-127">[out] A pointer to an [IStream](http://msdn.microsoft.com/ja-jp/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="49f6a-128">自動検出が失敗した場合は**null**を返します。</span><span class="sxs-lookup"><span data-stu-id="49f6a-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="49f6a-129">操作を終了したら、 [IStream](http://msdn.microsoft.com/ja-jp/library/aa380034%28VS.85%29.aspx)オブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f6a-129">You must release the [IStream](http://msdn.microsoft.com/ja-jp/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="49f6a-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="49f6a-130">Return values</span></span>

<span data-ttu-id="49f6a-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="49f6a-131">S_OK</span></span> 
  
- <span data-ttu-id="49f6a-132">関数の呼び出しが成功します。</span><span class="sxs-lookup"><span data-stu-id="49f6a-132">The function call is successful.</span></span>
    
<span data-ttu-id="49f6a-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="49f6a-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="49f6a-134">_pwzAddress_が**null**か、有効な SMTP アドレスではありませんか_ppXmlStream_ [IStream](http://msdn.microsoft.com/ja-jp/library/aa380034%28VS.85%29.aspx)オブジェクトへの**null**ポインター。</span><span class="sxs-lookup"><span data-stu-id="49f6a-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](http://msdn.microsoft.com/ja-jp/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="49f6a-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="49f6a-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="49f6a-136">クライアント コンピューターがネットワークに接続されていない、Microsoft Exchange 2007 サーバーにクライアント コンピューターが接続されていない、 _pwzAddress_は、Exchange 2007 サーバー上のアカウントではありません、または_pwzAddress_は、Exchange でサポートされていないアカウント自動検出サービスです。</span><span class="sxs-lookup"><span data-stu-id="49f6a-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="49f6a-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="49f6a-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="49f6a-138">イベント ハンドルは、操作をキャンセルするのには_hCancelEvent_に渡されました。</span><span class="sxs-lookup"><span data-stu-id="49f6a-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="49f6a-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="49f6a-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="49f6a-140">_PwzAddress_または_pwzPassword_に渡される値が長すぎます、256 バイトのサイズの内部バッファーがオーバーフローしたことなどです。</span><span class="sxs-lookup"><span data-stu-id="49f6a-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

