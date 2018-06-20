---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: キャッシュされた資格情報を使用して、ソーシャル ネットワーク サイトにログオンします。
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804379"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="030de-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="030de-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="030de-104">キャッシュされた資格情報を使用して、ソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="030de-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="030de-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="030de-105">Parameters</span></span>

<span data-ttu-id="030de-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="030de-106">_connectIn_</span></span>
  
> <span data-ttu-id="030de-107">[in]空の場合し、OSC が**LogonCached**を呼び出し、コンテキストによって、ログオンの資格情報を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="030de-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="030de-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="030de-108">_userName_</span></span>
  
> <span data-ttu-id="030de-109">[in]ユーザー名を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="030de-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="030de-110">_password_</span><span class="sxs-lookup"><span data-stu-id="030de-110">_password_</span></span>
  
> <span data-ttu-id="030de-111">[in]ユーザーのパスワードを含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="030de-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="030de-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="030de-112">_connectOut_</span></span>
  
> <span data-ttu-id="030de-113">[out]資格情報が含まれている不透明な文字列です。</span><span class="sxs-lookup"><span data-stu-id="030de-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="030de-114">備考</span><span class="sxs-lookup"><span data-stu-id="030de-114">Remarks</span></span>

<span data-ttu-id="030de-115">**機能** [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)から返された XML の**場合は true**として**useLogonCached**が設定されている場合にのみ、認証にこのメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="030de-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="030de-116">Outlook ソーシャル コネクタ (OSC) では、 **LogonCached**を呼び出し、 _connectIn_に空の文字列と空以外の_ユーザー名_と_パスワード_の文字列を渡します。</span><span class="sxs-lookup"><span data-stu-id="030de-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="030de-117">プロバイダーでは、ソーシャル ネットワークにログオンする_ユーザー名_と_パスワード_を使用して、認証が成功した場合は、OSC に不透明な_connectOut_パラメーターを返します。</span><span class="sxs-lookup"><span data-stu-id="030de-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="030de-118">認証が失敗した場合、プロバイダーは、OSC に OSC_E_LOGON_FAILURE エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="030de-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="030de-119">_ConnectOut_パラメーターでは、OSC に不透明な文字列し、は、パラメーターに渡される、 _connectIn_回目以降のソーシャル ネットワークにログオンするための OSC で。</span><span class="sxs-lookup"><span data-stu-id="030de-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="030de-120">プロバイダーは、プロバイダーが接続間にわたって格納 OSC _connectOut_文字列の任意の資格情報を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="030de-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="030de-121">OSC では、 _connectOut_、内の文字列を解釈しません。 し、Windows レジストリに格納する前にセキュリティ上の目的の文字列を暗号化します。</span><span class="sxs-lookup"><span data-stu-id="030de-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="030de-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="030de-122">See also</span></span>

- [<span data-ttu-id="030de-123">ISocialSession2: IUnknown</span><span class="sxs-lookup"><span data-stu-id="030de-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

