---
title: 省略可能なトランスポート プロバイダーの機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0bec2c17-b41c-4e46-8961-a55bde1f7326
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fd685e5bc67a3cb0785d9102e94c11ea921f07ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801693"
---
# <a name="optional-transport-provider-features"></a><span data-ttu-id="0c8b9-103">省略可能なトランスポート プロバイダーの機能</span><span class="sxs-lookup"><span data-stu-id="0c8b9-103">Optional Transport Provider Features</span></span>

  
  
<span data-ttu-id="0c8b9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c8b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c8b9-105">トランスポート プロバイダーを実装するオプションの機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0c8b9-105">Optional features transport providers can implement include:</span></span>
  
- <span data-ttu-id="0c8b9-106">メッセージおよびトランスポート プロバイダーを特定の受信者のオプションを登録しています。</span><span class="sxs-lookup"><span data-stu-id="0c8b9-106">Registering message and recipient options specific to the transport provider.</span></span>
    
- <span data-ttu-id="0c8b9-107">必要に応じて、構成情報およびメッセージング システムに資格情報を格納するプロファイルを維持します。</span><span class="sxs-lookup"><span data-stu-id="0c8b9-107">Maintaining a profile, if necessary, to store configuration information and credentials to the messaging system.</span></span>
    
- <span data-ttu-id="0c8b9-108">メッセージング システムに必要な資格情報の確認を実行しています。</span><span class="sxs-lookup"><span data-stu-id="0c8b9-108">Performing any verification of credentials required by the messaging system.</span></span>
    
- <span data-ttu-id="0c8b9-109">[IMAPISupport::Notify](imapisupport-notify.md)メソッドを使用して関心のあるクライアント アプリケーションのイベント通知をサポートします。</span><span class="sxs-lookup"><span data-stu-id="0c8b9-109">Supporting event notification for interested client applications with the [IMAPISupport::Notify](imapisupport-notify.md) method.</span></span> 
    
- <span data-ttu-id="0c8b9-110">構成のプロパティ シートと、トランスポート プロバイダーの設定を構成するユーザーを有効にするウィザードのダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="0c8b9-110">Displaying configuration property sheets and wizard dialog boxes to enable users to configure the transport provider's settings.</span></span>
    
- <span data-ttu-id="0c8b9-111">クライアント アプリケーションにメッセージの配信レポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="0c8b9-111">Providing message delivery reports to client applications.</span></span>
    

