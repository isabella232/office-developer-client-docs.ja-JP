---
title: Ndr を受信確認を一元化すること。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 16a150105211231af54ccfdc5d1565aeecea729e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579439"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="18def-103">Ndr を受信確認を一元化すること。</span><span class="sxs-lookup"><span data-stu-id="18def-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="18def-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18def-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18def-105">**配信不能レポート (Ndr) が到着したを中心に、クライアントの複数のインスタンスを同時に実行しているとき**</span><span class="sxs-lookup"><span data-stu-id="18def-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="18def-106">**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))、 **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) と**PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) を受信するアカウントに適切な値に設定します。レポートします。</span><span class="sxs-lookup"><span data-stu-id="18def-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="18def-107">必要な場合に[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)を呼び出すことによって、エントリの識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="18def-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="18def-108">アカウントをレポートの要求の発信者に送信するには、無視するためのメッセージング システムがあることを理解します。</span><span class="sxs-lookup"><span data-stu-id="18def-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="18def-109">レポートを移動する必要のある管理者に与える影響を減らします。</span><span class="sxs-lookup"><span data-stu-id="18def-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="18def-110">IPM などの個別のメッセージ クラスでは、元のメッセージを提供します。Note.MSNNews。</span><span class="sxs-lookup"><span data-stu-id="18def-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="18def-111">クラス Report.IPM.Note.MSNNews.NDR で受信したメッセージを検索し、それら付属するレポートを意図したアカウントに転送します。</span><span class="sxs-lookup"><span data-stu-id="18def-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="18def-112">同時に、 **PR_REPORT_ENTRYID**プロパティを受け入れる必要があることを通信するために、配信不能レポートのアカウントを無視するためのメッセージング システムに電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="18def-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="18def-113">**PR_REPORT_ENTRYID**を尊重しませんが、多くのメッセージング システムはこれを無視、MAPI メッセージ クラスの表記規則か。</span><span class="sxs-lookup"><span data-stu-id="18def-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="18def-114">したがって、メモのような結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="18def-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="18def-115">これは、入力が、変数のために対処するために少し困難になります。</span><span class="sxs-lookup"><span data-stu-id="18def-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="18def-116">件名を見るし、転送する場合は単語のリストから何かその意味を「配信不能」または何か、元の件名から。</span><span class="sxs-lookup"><span data-stu-id="18def-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="18def-117">時間の経過とともにこれらのリストを調整すること。</span><span class="sxs-lookup"><span data-stu-id="18def-117">Be prepared to tune these lists over time.</span></span> 
    

