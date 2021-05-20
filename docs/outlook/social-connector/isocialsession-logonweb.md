---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: フォーム ベース認証を使用してソーシャル ネットワーク サイトにログオンします。
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430337"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="d622e-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="d622e-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="d622e-104">フォーム ベース認証を使用してソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="d622e-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="d622e-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d622e-105">Parameters</span></span>

<span data-ttu-id="d622e-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="d622e-106">_connectIn_</span></span>
  
> <span data-ttu-id="d622e-107">[in]null の文字列、Web 上のログオン フォームへの URL、またはこのメソッドが呼び出された場合のログオン プロセスのコンテキストに応じて、ログオン資格情報を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d622e-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="d622e-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="d622e-108">_connectOut_</span></span>
  
> <span data-ttu-id="d622e-109">[out]ログオン資格情報を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d622e-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d622e-110">注釈</span><span class="sxs-lookup"><span data-stu-id="d622e-110">Remarks</span></span>

<span data-ttu-id="d622e-111">このOutlookソーシャル コネクタ (OSC) は、プロバイダーがフォーム ベース認証をサポートすると示している場合にのみ **LogonWeb** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d622e-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="d622e-112">プロバイダーは、機能の XML で **useLogonWebAuth** を **true** に設定して、フォーム ベースの認証を必要と **します**。</span><span class="sxs-lookup"><span data-stu-id="d622e-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="d622e-113">プロバイダーが **useLogonWebAuth** を **false** に設定すると、OSC は基本認証を使用し [、ISocialSession::Logon メソッドを呼び出](isocialsession-logon.md) します。</span><span class="sxs-lookup"><span data-stu-id="d622e-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="d622e-114">フォーム ベース認証を使用してソーシャル ネットワーク サイトにログオンするには **、LogonWeb** メソッドと [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) メソッドを特定の順序で呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d622e-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="d622e-115">OSC は **LogonWeb を初めて** 呼び出し **、connectIn** パラメーターに null  _を渡_ します。</span><span class="sxs-lookup"><span data-stu-id="d622e-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="d622e-116">プロバイダーは、OSC OSC_E_AUTH_ERRORエラーを発生します。</span><span class="sxs-lookup"><span data-stu-id="d622e-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="d622e-117">OSC は次に **GetLogonUrl を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="d622e-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="d622e-118">プロバイダーは **、GetLogonUrl** メソッドのログオン ページに適切な URL を返します。</span><span class="sxs-lookup"><span data-stu-id="d622e-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="d622e-119">OSC は **、GetLogonUrl** によって返される URL を使用して、フォーム ベースのログオン ページを表示します。</span><span class="sxs-lookup"><span data-stu-id="d622e-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="d622e-120">その後、OSC は LogonWeb を **2** 回目に呼び出し  _、connectIn_ パラメーターのログオン フォームに URL を渡します。</span><span class="sxs-lookup"><span data-stu-id="d622e-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="d622e-121">認証が成功した場合、プロバイダーは  _connectOut_ パラメーターのログオン資格情報を OSC に返します。</span><span class="sxs-lookup"><span data-stu-id="d622e-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="d622e-122">認証に失敗した場合、プロバイダーは OSC OSC_E_AUTH_ERRORエラーを発生します。</span><span class="sxs-lookup"><span data-stu-id="d622e-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="d622e-123">OSC プロバイダーがキャッシュされた資格情報の使用によるログオンをサポートしている場合は、機能 XML で **useLogonCached** を **true** **として指定** します。</span><span class="sxs-lookup"><span data-stu-id="d622e-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="d622e-124">プロバイダーは、OSC が接続間で格納する必要がある  _connectOut_ 文字列にログオン資格情報を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d622e-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="d622e-125">OSC は  _connectOut 文字列を解釈_ しない。</span><span class="sxs-lookup"><span data-stu-id="d622e-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="d622e-126">OSC が **useLogonCached** がtrue であるのを確認した後、OSC はセキュリティのために文字列を暗号化してから、その文字列をレジストリWindowsします。</span><span class="sxs-lookup"><span data-stu-id="d622e-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="d622e-127">OSC は [、ISocialSession2::LogonCached](isocialsession2-logoncached.md)を呼び出してソーシャル ネットワークにログオンしようとして、この文字列を _connectIn_ パラメーターに渡します。</span><span class="sxs-lookup"><span data-stu-id="d622e-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="d622e-128">エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d622e-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d622e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="d622e-129">See also</span></span>

- [<span data-ttu-id="d622e-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d622e-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="d622e-131">フォーム ベース認証</span><span class="sxs-lookup"><span data-stu-id="d622e-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

