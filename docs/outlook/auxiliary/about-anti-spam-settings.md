---
title: 迷惑メール対策の設定について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook では、迷惑メールからアカウントを保護するために各アカウントの設定を指定することができます。 このような迷惑メール対策設定は、ユーザーのプロファイルで、そのアカウント用に指定されたセクションに格納されます。
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390381"
---
# <a name="about-anti-spam-settings"></a>迷惑メール対策の設定について

Outlook では、迷惑メールからアカウントを保護するために各アカウントの設定を指定することができます。 このような迷惑メール対策設定は、ユーザーのプロファイルで、そのアカウント用に指定されたセクションに格納されます。 [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md)プロパティを使用すると、スパム対策の設定を含む、このアカウントのユーザーの環境設定が格納されているプロファイルのセクションの固有 ID (UID) を取得します。 
  
アカウントのスパム対策の設定を取得するのにには、次のプロパティを使用します。
  
- [PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)-アカウントの禁止された送信者としてユーザーが指定した電子メール アドレスとドメインのセミコロン区切りのリストを指定します。
    
- [PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)-アカウントのユーザーが指定するスパムのフィルタ リングのレベルを指定します。 次の表は、サポートされている値を示します。
    
|サポートされている値 |Definition |
|:-----|:-----|
|なし  <br/> |0 xffffffff  <br/> |
|低  <br/> |0x00000006  <br/> |
|中  <br/> |0x00000005  <br/> |
|高  <br/> |0x00000003  <br/> |
   
- [PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)-ユーザー アカウントの信頼された受信者として指定する電子メール アドレスとドメインのセミコロン区切りのリストを指定します。
    
- [PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)-アカウントの信頼された送信者としてユーザーが指定した電子メール アドレスとドメインのセミコロン区切りのリストを指定します。
    
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)
- [迷惑メール フィルター リストに名前を追加します。](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

