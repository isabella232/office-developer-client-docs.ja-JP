---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: フォーム ベース認証を使用して、ソーシャル ネットワーク サイトにログオンします。
ms.openlocfilehash: 4af0301d5b619ce7f9ff54b97f54b4b00408a564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804372"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="9cbb8-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="9cbb8-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="9cbb8-104">フォーム ベース認証を使用して、ソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="9cbb8-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="9cbb8-105">Parameters</span></span>

<span data-ttu-id="9cbb8-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="9cbb8-106">_connectIn_</span></span>
  
> <span data-ttu-id="9cbb8-107">[in]**Null**では、ログオン フォーム、またはこのメソッドが呼び出されたときに、ログオン プロセスのコンテキストによって、ログオンの資格情報を含む文字列を URL 文字列です。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="9cbb8-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="9cbb8-108">_connectOut_</span></span>
  
> <span data-ttu-id="9cbb8-109">[out]ログオン資格情報を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9cbb8-110">備考</span><span class="sxs-lookup"><span data-stu-id="9cbb8-110">Remarks</span></span>

<span data-ttu-id="9cbb8-111">Outlook ソーシャル コネクタ (OSC) は、プロバイダーでは、フォーム ベース認証をサポートしていることを示している場合にのみ、 **LogonWeb**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="9cbb8-112">プロバイダーでは、**該当****機能**の XML ファイルで**useLogonWebAuth**を設定することでフォーム ベースの認証が必要なことを示します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="9cbb8-113">プロバイダーでは、 **useLogonWebAuth**が**false**に設定、OSC は基本認証を使用し、 [ISocialSession::Logon](isocialsession-logon.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="9cbb8-114">フォーム ベース認証を使用して、ソーシャル ネットワーク サイトへのログオンでは、特定の順序で、 **LogonWeb**メソッドと[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="9cbb8-115">OSC は、最初に**LogonWeb**を呼び出す_connectIn_パラメーターに**null**を渡します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="9cbb8-116">プロバイダーは、OSC のように、OSC_E_AUTH_ERROR エラーを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="9cbb8-117">OSC は、次に**GetLogonUrl**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="9cbb8-118">プロバイダーは、 **GetLogonUrl**メソッドでは、ログオン ページに適切な URL を返します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="9cbb8-119">OSC では、 **GetLogonUrl**によって返される URL を使用して、フォーム ベースのログオン ページが表示します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="9cbb8-120">OSC を呼び出して**LogonWeb** 2 回目、 _connectIn_パラメーターでのログオン フォームに URL を渡します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="9cbb8-121">認証が成功すると、プロバイダーは、OSC を_connectOut_パラメーターにログオン資格情報を返します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="9cbb8-122">認証が失敗した場合、プロバイダーは、OSC のように、OSC_E_AUTH_ERROR エラーを発生させます。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="9cbb8-123">OSC プロバイダーは、キャッシュされた資格情報を使用してログオンをサポートする場合は、XML の**機能**で**は** **useLogonCached**を指定します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="9cbb8-124">プロバイダーは、プロバイダーは、接続での格納に OSC をしようとしている_connectOut_の文字列に、ログオン資格情報を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="9cbb8-125">OSC では、 _connectOut_の文字列は解釈されません。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="9cbb8-126">OSC では、その**useLogonCached**が**true**を確認した後、OSC は、Windows レジストリに格納する前にセキュリティのための文字列を暗号化します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="9cbb8-127">OSC は、 [ISocialSession2::LogonCached](isocialsession2-logoncached.md)を呼び出すことによって、ソーシャル ネットワークへのログオンに 2 回目以降に、 _connectIn_パラメーターにこの文字列を渡します。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="9cbb8-128">エラー コードの詳細については、 [Outlook ソーシャル コネクタ プロバイダーのエラー コード](outlook-social-connector-provider-error-codes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9cbb8-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9cbb8-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="9cbb8-129">See also</span></span>

- [<span data-ttu-id="9cbb8-130">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9cbb8-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="9cbb8-131">フォーム ベースの認証</span><span class="sxs-lookup"><span data-stu-id="9cbb8-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

