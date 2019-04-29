---
title: i"alsessionalsessionlogonweb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: フォームベース認証を使用してソーシャルネットワークサイトにログオンします。
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430337"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="aa931-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="aa931-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="aa931-104">フォームベース認証を使用してソーシャルネットワークサイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="aa931-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="aa931-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aa931-105">Parameters</span></span>

<span data-ttu-id="aa931-106">_//_</span><span class="sxs-lookup"><span data-stu-id="aa931-106">_connectIn_</span></span>
  
> <span data-ttu-id="aa931-107">順番このメソッドが呼び出されたときのログオンプロセスのコンテキストに応じて、 **null**の文字列、web 上のログオンフォームへの URL、またはログオン資格情報を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="aa931-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="aa931-108">_connectout_</span><span class="sxs-lookup"><span data-stu-id="aa931-108">_connectOut_</span></span>
  
> <span data-ttu-id="aa931-109">読み上げログオン資格情報を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="aa931-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa931-110">注釈</span><span class="sxs-lookup"><span data-stu-id="aa931-110">Remarks</span></span>

<span data-ttu-id="aa931-111">Outlook Social Connector (.osc) は、プロバイダーがフォームベース認証をサポートしていることを示す場合にのみ、 **logonweb**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aa931-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="aa931-112">プロバイダーは、XML の**機能**に対して**uselogonwebauth**を**true**に設定することにより、フォームベース認証が必要であることを示します。</span><span class="sxs-lookup"><span data-stu-id="aa931-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="aa931-113">プロバイダーが**uselogonwebauth**を**false**として設定している場合、.osc は基本認証を使用して、 [iime alsession:: Logon](isocialsession-logon.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aa931-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="aa931-114">フォームベース認証を使用してソーシャルネットワークサイトにログオンするには、特定の順序で**logonweb**および[isocial alsession:: getlogonurl](isocialsession-getlogonurl.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa931-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="aa931-115">.osc は、最初に**logonweb**を呼び出し、 **null**を引数__ として指定します。</span><span class="sxs-lookup"><span data-stu-id="aa931-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="aa931-116">プロバイダーは、.osc に OSC_E_AUTH_ERROR エラーを発生させます。</span><span class="sxs-lookup"><span data-stu-id="aa931-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="aa931-117">.osc の次のメソッドは、 **getlogonurl**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aa931-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="aa931-118">プロバイダーは、 **getlogonurl**メソッドのログオンページに適切な URL を返します。</span><span class="sxs-lookup"><span data-stu-id="aa931-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="aa931-119">.osc は、 **getlogonurl**によって返される url を使用して、フォームベースのログオンページを表示します。</span><span class="sxs-lookup"><span data-stu-id="aa931-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="aa931-120">次に、.osc は**logonweb**をもう一度呼び出し、その URL を "/入力" __ パラメーターでログオンフォームに渡します。</span><span class="sxs-lookup"><span data-stu-id="aa931-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="aa931-121">認証が成功すると、プロバイダーは、 _connectout_パラメーターのログオン資格情報を .osc に返します。</span><span class="sxs-lookup"><span data-stu-id="aa931-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="aa931-122">認証が失敗した場合、プロバイダーは .osc に OSC_E_AUTH_ERROR エラーを発生させます。</span><span class="sxs-lookup"><span data-stu-id="aa931-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="aa931-123">.osc プロバイダーがキャッシュされた資格情報を使用したログ記録をサポートしている場合は、**機能**XML では**true**としてキャッシュされた**uselogoncached**指定します。</span><span class="sxs-lookup"><span data-stu-id="aa931-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="aa931-124">プロバイダーは、接続間に格納するために、プロバイダーが .osc を必要とする_connectout_文字列にログオン資格情報を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa931-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="aa931-125">.osc は、 _connectout_文字列を解釈しません。</span><span class="sxs-lookup"><span data-stu-id="aa931-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="aa931-126">.osc は、 **uselogoncached**が**true**であることを確認した後、セキュリティのために文字列を暗号化してから Windows レジストリに保存します。</span><span class="sxs-lookup"><span data-stu-id="aa931-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="aa931-127">.osc は、 [ISocialSession2:: logoncached](isocialsession2-logoncached.md)を呼び出すことによって、ソーシャルネットワークへの次回のログオン時に、この文字列を引数として渡されます。 __</span><span class="sxs-lookup"><span data-stu-id="aa931-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="aa931-128">エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa931-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa931-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa931-129">See also</span></span>

- [<span data-ttu-id="aa931-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa931-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="aa931-131">フォームベース認証</span><span class="sxs-lookup"><span data-stu-id="aa931-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

