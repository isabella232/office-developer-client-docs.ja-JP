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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347804"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="2773e-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="2773e-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="2773e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2773e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2773e-105">Microsoft Exchange 2007 サーバーの自動検出サービスから取得された情報を表す、拡張マークアップ言語 (XML) ストリームを返します。</span><span class="sxs-lookup"><span data-stu-id="2773e-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2773e-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2773e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2773e-107">エクスポート対象:</span><span class="sxs-lookup"><span data-stu-id="2773e-107">Exported by:</span></span>  <br/> |<span data-ttu-id="2773e-108">olmapi32</span><span class="sxs-lookup"><span data-stu-id="2773e-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="2773e-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="2773e-109">Called by:</span></span>  <br/> |<span data-ttu-id="2773e-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="2773e-110">Client</span></span>  <br/> |
|<span data-ttu-id="2773e-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="2773e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2773e-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="2773e-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="2773e-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2773e-113">Parameters</span></span>

 <span data-ttu-id="2773e-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="2773e-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="2773e-115">順番自動検出情報を取得するアカウントの、null で終了する簡易メール転送プロトコル (SMTP) 電子メールアドレス。</span><span class="sxs-lookup"><span data-stu-id="2773e-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="2773e-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="2773e-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="2773e-117">順番_pwzAddress_によって指定されたアカウントのパスワード (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="2773e-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="2773e-118">_pwzAddress_で指定されたアカウントがパスワードを必要としない場合、任意のパスワードを渡しても効果はありません。</span><span class="sxs-lookup"><span data-stu-id="2773e-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="2773e-119">_hcancelevent_</span><span class="sxs-lookup"><span data-stu-id="2773e-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="2773e-120">順番省略可能で、操作を取り消すために使用できる、未設定の Win32 イベントハンドル。</span><span class="sxs-lookup"><span data-stu-id="2773e-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="2773e-121">操作を取り消すには、イベントを設定し、イベントハンドルを_hcancelevent_として渡します。操作をキャンセルしない場合は、 **null**を渡します。</span><span class="sxs-lookup"><span data-stu-id="2773e-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="2773e-122">イベントハンドルを表さない値を渡すと、無効になり、関数は無視されます。</span><span class="sxs-lookup"><span data-stu-id="2773e-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="2773e-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2773e-123">_ulFlags_</span></span>
  
> <span data-ttu-id="2773e-124">順番このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="2773e-124">[in] This parameter is not used.</span></span> <span data-ttu-id="2773e-125">0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2773e-125">It must be 0.</span></span>
    
 <span data-ttu-id="2773e-126">_ppxmlstream_</span><span class="sxs-lookup"><span data-stu-id="2773e-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="2773e-127">読み上げautodiscovery XML を含む[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2773e-127">[out] A pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="2773e-128">autodiscovery 操作が失敗した場合は**null**を返します。</span><span class="sxs-lookup"><span data-stu-id="2773e-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="2773e-129">[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトの使用が終了したら解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2773e-129">You must release the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2773e-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="2773e-130">Return values</span></span>

<span data-ttu-id="2773e-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="2773e-131">S_OK</span></span> 
  
- <span data-ttu-id="2773e-132">関数呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="2773e-132">The function call is successful.</span></span>
    
<span data-ttu-id="2773e-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2773e-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="2773e-134">_pwzAddress_が**null**であるか、有効な SMTP アドレスではありません。または、 _ppxmlstream_は[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトへの**null**ポインターです。</span><span class="sxs-lookup"><span data-stu-id="2773e-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="2773e-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2773e-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="2773e-136">クライアントコンピューターがネットワークに接続されていない、クライアントコンピューターが Microsoft exchange 2007 サーバーに接続されていない、 _pwzAddress_が exchange 2007 サーバーのアカウントではない、または exchange をサポートしていないアカウントである_pwzAddress_自動検出サービス。</span><span class="sxs-lookup"><span data-stu-id="2773e-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="2773e-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="2773e-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="2773e-138">操作をキャンセルするため、 _hcancelevent_にイベントハンドルが渡されました。</span><span class="sxs-lookup"><span data-stu-id="2773e-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="2773e-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="2773e-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="2773e-140">_pwzAddress_または_pwzPassword_に渡された値が長すぎるため、サイズ256バイトの内部バッファーがオーバーフローしています。</span><span class="sxs-lookup"><span data-stu-id="2773e-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

