---
title: MAPI クライアント アプリケーションの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ad2e1f2d-57c3-4fb5-9e0f-db51640df84d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 12fb03ed5a165592113f49a202f777b0f301736d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568757"
---
# <a name="mapi-client-application-overview"></a><span data-ttu-id="45ec8-103">MAPI クライアント アプリケーションの概要</span><span class="sxs-lookup"><span data-stu-id="45ec8-103">MAPI Client Application Overview</span></span>

  
  
<span data-ttu-id="45ec8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45ec8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45ec8-105">MAPI クライアント アプリケーションは、MAPI プログラミング ・ インタ フェースを使用するアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="45ec8-105">A MAPI client application is any application that uses the MAPI programming interface.</span></span> <span data-ttu-id="45ec8-106">クライアント アプリケーションは、プライマリまたはセカンダリのフォーカスとしていずれかのメッセージのタスクを実装します。</span><span class="sxs-lookup"><span data-stu-id="45ec8-106">Client applications implement messaging tasks as either their primary or secondary focus.</span></span> <span data-ttu-id="45ec8-107">電子メールを送受信するアプリケーションなどのメッセージング クライアント アプリケーションでは、その主な目的としてメッセージングを実装します。</span><span class="sxs-lookup"><span data-stu-id="45ec8-107">Messaging client applications, such as applications that send and receive email, implement messaging as their primary focus.</span></span> <span data-ttu-id="45ec8-108">非メッセージング クライアントなどのアプリケーション インベントリまたはアプリケーションの構成では、メッセージングは、セカンダリ機能です。</span><span class="sxs-lookup"><span data-stu-id="45ec8-108">For non-messaging client applications, such as inventory or configuration applications, messaging is a secondary feature.</span></span>
  
<span data-ttu-id="45ec8-109">メッセージング アクティビティを含めることができます、たとえば、ワード プロセッシング アプリケーションのドキュメントを送信を有効にする**ファイル**] メニューの [Microsoft Office Outlook の電子メール、作業フロー オートメーション、プログラム、掲示板サービスにコマンドを**送信**します。</span><span class="sxs-lookup"><span data-stu-id="45ec8-109">Messaging activities can include, for example, a word processing application that has a **Send** command on its **File** menu to enable documents to be sent, Microsoft Office Outlook email, work flow automation programs, and bulletin board services.</span></span> 
  
<span data-ttu-id="45ec8-110">クライアント アプリケーションでは、ユーザーがインタラクティブな環境を作成するか、自動化された環境でのユーザー操作を含めることができますか。</span><span class="sxs-lookup"><span data-stu-id="45ec8-110">Client applications can either include the user to create an interactive environment or operate without a user in an automated environment.</span></span> <span data-ttu-id="45ec8-111">共通のダイアログ ボックスの標準的なユーザー ・ インタ フェースのセットを提供すると、MAPI クライアント アプリケーションをユーザー インターフェイスを提供する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="45ec8-111">Although MAPI supplies a set of common dialog boxes with its standard user interface, client applications are not required to present a user interface.</span></span> <span data-ttu-id="45ec8-112">実際、する場合は、すべての処理をアプリケーションでは、処理できます。</span><span class="sxs-lookup"><span data-stu-id="45ec8-112">In fact, all processing can be handled in the application, if you want.</span></span> <span data-ttu-id="45ec8-113">自動化されたクライアント アプリケーションの例は、定期的に標準の受信者を特定の種類のアイテムをルートするように設定された在庫管理アプリケーションになります。</span><span class="sxs-lookup"><span data-stu-id="45ec8-113">An example of an automated client application would be an inventory management application that is programmed to route items of a particular type to standard recipients on a regular basis.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="45ec8-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="45ec8-114">See also</span></span>



[<span data-ttu-id="45ec8-115">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="45ec8-115">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

