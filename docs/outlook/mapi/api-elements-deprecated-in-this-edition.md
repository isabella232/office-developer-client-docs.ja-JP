---
title: このエディションで廃止された API 要素
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318209"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="5fba5-103">このエディションで廃止された API 要素</span><span class="sxs-lookup"><span data-stu-id="5fba5-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="5fba5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fba5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fba5-105">次の API 要素は、Microsoft Outlook 2013 で廃止されました。</span><span class="sxs-lookup"><span data-stu-id="5fba5-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="5fba5-106">サポートされなくなったので、新しいプロジェクトで使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="5fba5-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="5fba5-107">メッセージと受信者のオプションの廃止</span><span class="sxs-lookup"><span data-stu-id="5fba5-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="5fba5-108">このリリースでは、次の API 要素が廃止されました。メッセージと受信者のオプションは、現在使用されていません。</span><span class="sxs-lookup"><span data-stu-id="5fba5-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="5fba5-109">**IXPLogon:: registeroptions**— MAPI サブシステムは、このメソッドを呼び出して、トランスポートプロバイダーのメッセージおよび受信者オプションの既定値を設定することはできなくなりました。</span><span class="sxs-lookup"><span data-stu-id="5fba5-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="5fba5-110">**optiondata**—メッセージおよび受信者オプションのプロパティをサポートするこのデータ構造は、現在は使用されていません。</span><span class="sxs-lookup"><span data-stu-id="5fba5-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="5fba5-111">MAPI サブシステムは、 **IXPLogon:: registeroptions**を呼び出して、トランスポートプロバイダーが特定のアドレスの種類に対してサポートしているメッセージまたは受信者オプションを取得することができなくなりました。</span><span class="sxs-lookup"><span data-stu-id="5fba5-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="5fba5-112">**optioncallback**-この関数プロトタイプは、コールバック関数を宣言するために使用され、さらに、プロバイダーのプロパティを解決するために使用される MAPI サブシステムは現在使われていません。</span><span class="sxs-lookup"><span data-stu-id="5fba5-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="5fba5-113">MAPI サブシステムは**IXPLogon:: registeroptions**を呼び出しません。または、トランスポートプロバイダーによって返されるコールバック関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="5fba5-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="5fba5-114">**imapisession:: messageoptions**-MAPI クライアントおよびサービスプロバイダーは、このメソッドを呼び出してプロパティを表示したり、特定のメッセージおよびアドレスの種類を制御するプロパティをユーザーが設定したりすることはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="5fba5-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="5fba5-115">メソッドは常に MAPI_E_NOT_FOUND を返します。これは、特定のメッセージにメッセージオプションがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5fba5-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="5fba5-116">**imapisession:: querydefaultmessageopt**— MAPI クライアントおよびサービスプロバイダーは、特定のアドレスの種類のメッセージオプションを制御するプロパティを取得するために、このメソッドを呼び出すことができなくなります。</span><span class="sxs-lookup"><span data-stu-id="5fba5-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="5fba5-117">メソッドによって、プロパティ値の配列へのポインターが返されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="5fba5-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="5fba5-118">**IAddrBook:: RecipOptions**— MAPI クライアントおよびサービスプロバイダーは、このメソッドを呼び出してプロパティを表示したり、特定のアドレスの種類の受信者の処理を制御するプロパティをユーザーに設定したりすることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="5fba5-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="5fba5-119">このメソッドは、常に MAPI_W_ERRORS_RETURNED を返します。この値は、特定の受信者に対して受信者のオプションが存在しないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5fba5-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="5fba5-120">**IAddrBook:: QueryDefaultRecipOpt**— MAPI クライアントおよびサービスプロバイダーは、特定のアドレスの種類の受信者オプションを制御するプロパティを取得するために、このメソッドを呼び出すことができなくなります。</span><span class="sxs-lookup"><span data-stu-id="5fba5-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="5fba5-121">メソッドによって、プロパティ値の配列へのポインターが返されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="5fba5-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5fba5-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="5fba5-122">See also</span></span>



[<span data-ttu-id="5fba5-123">Outlook MAPI リファレンスの概要</span><span class="sxs-lookup"><span data-stu-id="5fba5-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

