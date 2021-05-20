---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: キャッシュされた資格情報を使用してソーシャル ネットワーク サイトにログオンします。
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436623"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="37ad6-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="37ad6-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="37ad6-104">キャッシュされた資格情報を使用してソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="37ad6-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="37ad6-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37ad6-105">Parameters</span></span>

<span data-ttu-id="37ad6-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="37ad6-106">_connectIn_</span></span>
  
> <span data-ttu-id="37ad6-107">[in]OSC が **LogonCached** を呼び出しているコンテキストに応じて、空またはログオン資格情報を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="37ad6-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="37ad6-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="37ad6-108">_userName_</span></span>
  
> <span data-ttu-id="37ad6-109">[in]ユーザー名を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="37ad6-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="37ad6-110">_password_</span><span class="sxs-lookup"><span data-stu-id="37ad6-110">_password_</span></span>
  
> <span data-ttu-id="37ad6-111">[in]ユーザーのパスワードを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="37ad6-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="37ad6-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="37ad6-112">_connectOut_</span></span>
  
> <span data-ttu-id="37ad6-113">[out]資格情報を含む不透明な文字列。</span><span class="sxs-lookup"><span data-stu-id="37ad6-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37ad6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="37ad6-114">Remarks</span></span>

<span data-ttu-id="37ad6-115">このメソッドは [、ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)によって返される機能 **XML** で **useLogonCached** が **true** に設定されている場合にのみ、認証のために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="37ad6-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="37ad6-116">このOutlookソーシャル コネクタ (OSC) は **LogonCached** を呼び出し _、connectIn_ および空でない _userName_ 文字列とパスワード文字列に空の文字列を _渡_ します。</span><span class="sxs-lookup"><span data-stu-id="37ad6-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="37ad6-117">プロバイダーは  _userName_  _とパスワード_ を使用してソーシャル ネットワークにログオンし、認証が成功した場合は不透明な  _connectOut_ パラメーターを OSC に返します。</span><span class="sxs-lookup"><span data-stu-id="37ad6-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="37ad6-118">認証に失敗した場合、プロバイダーは OSC にOSC_E_LOGON_FAILUREエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="37ad6-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="37ad6-119">_connectOut パラメーター_ は、OSC に対して不透明な文字列であり、OSC がソーシャル ネットワークにログオンしようとして以降に _connectIn_ パラメーターに渡されます。</span><span class="sxs-lookup"><span data-stu-id="37ad6-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="37ad6-120">プロバイダーは、OSC が接続間で格納する必要がある  _connectOut_ 文字列に資格情報を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37ad6-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="37ad6-121">OSC は _connectOut_ 内の文字列を解釈しません。また、セキュリティ上の目的で文字列を暗号化してから、Windowsします。</span><span class="sxs-lookup"><span data-stu-id="37ad6-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37ad6-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="37ad6-122">See also</span></span>

- [<span data-ttu-id="37ad6-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="37ad6-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

