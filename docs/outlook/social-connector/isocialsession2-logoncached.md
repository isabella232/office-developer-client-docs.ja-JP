---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: キャッシュされた資格情報を使用してソーシャルネットワークサイトにログオンします。
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336506"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="10d16-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="10d16-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="10d16-104">キャッシュされた資格情報を使用してソーシャルネットワークサイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="10d16-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="10d16-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="10d16-105">Parameters</span></span>

<span data-ttu-id="10d16-106">_//_</span><span class="sxs-lookup"><span data-stu-id="10d16-106">_connectIn_</span></span>
  
> <span data-ttu-id="10d16-107">順番この文字列は、.osc が**logoncached**を呼び出しているコンテキストに応じて、空の場合と、ログオン資格情報が含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="10d16-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="10d16-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="10d16-108">_userName_</span></span>
  
> <span data-ttu-id="10d16-109">順番ユーザー名を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="10d16-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="10d16-110">_password_</span><span class="sxs-lookup"><span data-stu-id="10d16-110">_password_</span></span>
  
> <span data-ttu-id="10d16-111">順番ユーザーのパスワードを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="10d16-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="10d16-112">_connectout_</span><span class="sxs-lookup"><span data-stu-id="10d16-112">_connectOut_</span></span>
  
> <span data-ttu-id="10d16-113">読み上げ資格情報を含む符号化文字列。</span><span class="sxs-lookup"><span data-stu-id="10d16-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10d16-114">解説</span><span class="sxs-lookup"><span data-stu-id="10d16-114">Remarks</span></span>

<span data-ttu-id="10d16-115">このメソッドは、 [iime alprovider:: getcapabilities](isocialprovider-getcapabilities.md)によって返される**機能**XML で**uselogoncached**が**true**に設定されている場合にのみ、認証のために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="10d16-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="10d16-116">Outlook Social Connector (.osc) は、 **logoncached**を呼び出し、空の文字列を__ 指定します。ユーザー名とパスワードは空ではない_ユーザー名_と_パスワード_文字列を渡します。</span><span class="sxs-lookup"><span data-stu-id="10d16-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="10d16-117">プロバイダーは、ソーシャルネットワークにログオンするために_ユーザー名_と_パスワード_を使用し、認証が成功した場合は、不透明な_connectout_パラメーターを .osc に返します。</span><span class="sxs-lookup"><span data-stu-id="10d16-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="10d16-118">認証が失敗した場合、プロバイダーは、OSC_E_LOGON_FAILURE エラーを .osc に返します。</span><span class="sxs-lookup"><span data-stu-id="10d16-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="10d16-119">_connectout_パラメーターは、.osc に対する不透明な文字列であり、.osc によっ__ てソーシャルネットワークにログオンするために、次に試行されたときに、このパラメーターに渡されます。</span><span class="sxs-lookup"><span data-stu-id="10d16-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="10d16-120">プロバイダーは、接続間に格納するために、プロバイダーが .osc を必要とするすべての資格情報を_connectout_文字列に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10d16-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="10d16-121">.osc は、 _connectout_の文字列を解釈しないで、セキュリティ上の理由で文字列を暗号化してから、Windows レジストリに保存します。</span><span class="sxs-lookup"><span data-stu-id="10d16-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="10d16-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="10d16-122">See also</span></span>

- [<span data-ttu-id="10d16-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="10d16-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

