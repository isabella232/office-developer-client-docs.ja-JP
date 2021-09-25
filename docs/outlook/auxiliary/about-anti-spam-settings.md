---
title: 迷惑メール対策の設定について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlookユーザーは、スパムからアカウントを保護するために、各アカウントの設定を指定できます。 このようなスパム対策設定は、ユーザーのプロファイル内のそのアカウントに指定されたセクションに保存されます。
ms.openlocfilehash: d316df2cfc94f3dbb23dcaea68dd9a20e0b282a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625799"
---
# <a name="about-anti-spam-settings"></a>迷惑メール対策の設定について

Outlookユーザーは、スパムからアカウントを保護するために、各アカウントの設定を指定できます。 このようなスパム対策設定は、ユーザーのプロファイル内のそのアカウントに指定されたセクションに保存されます。 [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md)プロパティを使用して、このアカウントのユーザー設定 (スパム対策設定を含む) を格納するプロファイル内のセクションの一意の ID (UID) を取得します。 
  
アカウントのスパム対策設定を取得するには、次のプロパティを使用します。
  
- [PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—ユーザーがアカウントの受信拒否送信者として指定した電子メール アドレスとドメインのセミコロンで区切られたリストを指定します。
    
- [PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—ユーザーがアカウントに指定したスパム フィルターのレベルを指定します。 次の表に、サポートされている値を示します。
    
|サポートされている値 |Definition |
|:-----|:-----|
|なし  <br/> |0xFFFFFFFF  <br/> |
|低い  <br/> |0x00000006  <br/> |
|中  <br/> |0x00000005  <br/> |
|高  <br/> |0x00000003  <br/> |
   
- [PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—ユーザーがアカウントの信頼できる受信者として指定した電子メール アドレスとドメインのセミコロンで区切られたリストを指定します。
    
- [PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—ユーザーがアカウントの信頼できる送信者として指定した電子メール アドレスとドメインのセミコロンで区切られたリストを指定します。
    
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)
- [迷惑メール フィルター リストに名前を追加する](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

