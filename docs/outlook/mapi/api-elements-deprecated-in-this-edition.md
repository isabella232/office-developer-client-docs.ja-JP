---
title: このエディションで非推奨の API 要素
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: c70e89efba585183d2019bbda49102ecd14b9e20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799676"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="769ca-103">このエディションで非推奨の API 要素</span><span class="sxs-lookup"><span data-stu-id="769ca-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="769ca-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="769ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="769ca-105">Microsoft Outlook 2013 では、次の API 要素は推奨されていません。</span><span class="sxs-lookup"><span data-stu-id="769ca-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="769ca-106">サポートされていませんし、新しいプロジェクトで使用する必要がありません。</span><span class="sxs-lookup"><span data-stu-id="769ca-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="769ca-107">メッセージと受信者のオプションの廃止</span><span class="sxs-lookup"><span data-stu-id="769ca-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="769ca-108">次の API 要素は古いメッセージと受信者のオプションこのリリースでは使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="769ca-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="769ca-109">**IXPLogon::RegisterOptions**など、MAPI サブシステムが不要になったトランスポート プロバイダーのメッセージと受信者のオプションの既定値を確立するためには、このメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="769ca-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="769ca-110">**OPTIONDATA**- と受信者のメッセージのオプションのプロパティがサポートされているこのデータ構造体は使用されていません。</span><span class="sxs-lookup"><span data-stu-id="769ca-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="769ca-111">MAPI サブシステムには、不要になった任意のメッセージまたはトランスポート プロバイダーは、特定のアドレスの種類をサポートしている受信者のオプションを取得するのには**IXPLogon::RegisterOptions**が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="769ca-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="769ca-112">**OPTIONCALLBACK**: この関数のプロトタイプ、トランスポート プロバイダーを使用して、コールバック関数をさらに、宣言、プロバイダーのプロパティを解決するのには使用する MAPI サブシステムが古くなった。</span><span class="sxs-lookup"><span data-stu-id="769ca-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="769ca-113">**IXPLogon::RegisterOptions**やトランスポート プロバイダーによって返されるすべてのコールバック関数を使用して、MAPI サブシステムが不要になった。</span><span class="sxs-lookup"><span data-stu-id="769ca-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="769ca-114">**IMAPISession::MessageOptions**: MAPI クライアントとサービスのプロバイダーは、プロパティの表示または特定のメッセージとアドレスの種類を制御するプロパティを設定できるようにするには、このメソッドを呼び出す必要がありますできなくします。</span><span class="sxs-lookup"><span data-stu-id="769ca-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="769ca-115">メソッドは、常に、特定のメッセージのメッセージのオプションがないことを示す MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="769ca-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="769ca-116">**IMAPISession::QueryDefaultMessageOpt**: MAPI クライアントとサービスのプロバイダーは、特定のアドレスの種類をメッセージのオプションを制御するプロパティを取得するには、このメソッドを呼び出す必要がありますできなくします。</span><span class="sxs-lookup"><span data-stu-id="769ca-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="769ca-117">不要になったプロパティの値の配列へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="769ca-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="769ca-118">**IAddrBook::RecipOptions**: MAPI クライアントとサービスのプロバイダーは、プロパティの表示、またはユーザーがそのコントロールの処理を特定のアドレスの種類の受信者のプロパティを設定できるようにするには、このメソッドを呼び出す必要がありますできなくします。</span><span class="sxs-lookup"><span data-stu-id="769ca-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="769ca-119">メソッドは、特定の宛先の受信者のオプションがないことを示す、MAPI_W_ERRORS_RETURNED を常に返します。</span><span class="sxs-lookup"><span data-stu-id="769ca-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="769ca-120">**IAddrBook::QueryDefaultRecipOpt**: MAPI クライアントとサービスのプロバイダーは、特定のアドレスの種類の受信者のオプションを制御するプロパティを取得するには、このメソッドを呼び出す必要がありますできなくします。</span><span class="sxs-lookup"><span data-stu-id="769ca-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="769ca-121">不要になったプロパティの値の配列へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="769ca-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="769ca-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="769ca-122">See also</span></span>



[<span data-ttu-id="769ca-123">Outlook MAPI リファレンスの概要</span><span class="sxs-lookup"><span data-stu-id="769ca-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

