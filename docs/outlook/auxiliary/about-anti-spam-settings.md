---
title: 迷惑メール対策の設定について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook では、ユーザーがアカウントをスパムから保護できるように、各アカウントの設定を指定することができます。 このようなスパム対策の設定は、ユーザーのプロファイルでそのアカウントに指定されたセクションに格納されます。
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316962"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="5fdba-104">迷惑メール対策の設定について</span><span class="sxs-lookup"><span data-stu-id="5fdba-104">About anti-spam settings</span></span>

<span data-ttu-id="5fdba-105">Outlook では、ユーザーがアカウントをスパムから保護できるように、各アカウントの設定を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="5fdba-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="5fdba-106">このようなスパム対策の設定は、ユーザーのプロファイルでそのアカウントに指定されたセクションに格納されます。</span><span class="sxs-lookup"><span data-stu-id="5fdba-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="5fdba-107">[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md)プロパティを使用して、このアカウントのユーザー設定を格納するプロファイルのセクションの一意の ID (UID) を取得します。これには、スパム対策の設定も含まれます。</span><span class="sxs-lookup"><span data-stu-id="5fdba-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="5fdba-108">次のプロパティを使用して、アカウントのスパム対策設定を取得します。</span><span class="sxs-lookup"><span data-stu-id="5fdba-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="5fdba-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—ユーザーがアカウントの受信拒否リストとして指定した電子メールアドレスとドメインのセミコロンで区切られた一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="5fdba-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="5fdba-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—ユーザーがアカウントに対して指定したスパムフィルターのレベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="5fdba-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="5fdba-111">次の表に、サポートされている値を示します。</span><span class="sxs-lookup"><span data-stu-id="5fdba-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="5fdba-112">サポートされる値</span><span class="sxs-lookup"><span data-stu-id="5fdba-112">Supported value</span></span> |<span data-ttu-id="5fdba-113">Definition</span><span class="sxs-lookup"><span data-stu-id="5fdba-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="5fdba-114">なし</span><span class="sxs-lookup"><span data-stu-id="5fdba-114">None</span></span>  <br/> |<span data-ttu-id="5fdba-115">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="5fdba-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="5fdba-116">低</span><span class="sxs-lookup"><span data-stu-id="5fdba-116">Low</span></span>  <br/> |<span data-ttu-id="5fdba-117">0x00000006</span><span class="sxs-lookup"><span data-stu-id="5fdba-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="5fdba-118">中</span><span class="sxs-lookup"><span data-stu-id="5fdba-118">Medium</span></span>  <br/> |<span data-ttu-id="5fdba-119">0x00000005</span><span class="sxs-lookup"><span data-stu-id="5fdba-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="5fdba-120">高</span><span class="sxs-lookup"><span data-stu-id="5fdba-120">High</span></span>  <br/> |<span data-ttu-id="5fdba-121">0x00000003</span><span class="sxs-lookup"><span data-stu-id="5fdba-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="5fdba-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—ユーザーがアカウントの信頼できる受信者として指定した電子メールアドレスとドメインのセミコロンで区切られたリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="5fdba-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="5fdba-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—ユーザーがアカウントの信頼できる差出人として指定した電子メールアドレスとドメインのセミコロンで区切られたリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="5fdba-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5fdba-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="5fdba-124">See also</span></span>

- [<span data-ttu-id="5fdba-125">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="5fdba-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="5fdba-126">迷惑メールフィルターリストに名前を追加する</span><span class="sxs-lookup"><span data-stu-id="5fdba-126">Add names to the Junk Email Filter lists</span></span>](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

