---
title: 既定のメッセージ ストア
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576912"
---
# <a name="default-message-stores"></a><span data-ttu-id="2ca6b-103">既定のメッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="2ca6b-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="2ca6b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ca6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ca6b-105">既定のメッセージ ストアは、クライアント アプリケーションが汎用メッセージング タスクに使用できるものです。</span><span class="sxs-lookup"><span data-stu-id="2ca6b-105">A default message store is one that client applications can use for general purpose messaging tasks.</span></span> <span data-ttu-id="2ca6b-106">既定のメッセージ ストアとしてメッセージ ストア プロバイダーを使用する場合に、メッセージ ストア プロバイダーにとって必要となるいくつかのオプション機能があります。</span><span class="sxs-lookup"><span data-stu-id="2ca6b-106">There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store.</span></span> <span data-ttu-id="2ca6b-107">それらは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2ca6b-107">These are as follows:</span></span>
  
- <span data-ttu-id="2ca6b-108">受信トレイ、送信トレイ、および検索結果フォルダーといった特別なフォルダーを実装します。</span><span class="sxs-lookup"><span data-stu-id="2ca6b-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="2ca6b-109">開封済みレポートと未読レポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="2ca6b-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="2ca6b-110">受信メッセージと送信メッセージの送信を許可します。</span><span class="sxs-lookup"><span data-stu-id="2ca6b-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="2ca6b-111">任意のメッセージ クラスのメッセージの作成を許可します。</span><span class="sxs-lookup"><span data-stu-id="2ca6b-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="2ca6b-112">名前付きプロパティと複数値プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2ca6b-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="2ca6b-113">メッセージ ストア プロバイダーがトランスポート プロバイダーと密接に結合している場合でも、[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2ca6b-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="2ca6b-p102">関連するコンテンツ テーブルをサポートします。詳細については、[コンテンツ テーブル](contents-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ca6b-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="2ca6b-116">送信メッセージ キューにメッセージがある場合に、 MAPI スプーラーの通知をサポートします。</span><span class="sxs-lookup"><span data-stu-id="2ca6b-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ca6b-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ca6b-117">See also</span></span>



[<span data-ttu-id="2ca6b-118">MAPI メッセージ ストア プロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="2ca6b-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

