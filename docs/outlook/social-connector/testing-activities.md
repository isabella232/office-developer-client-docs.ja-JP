---
title: アクティビティをテストします。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: テストおよび以外の友人や友人の活動を適切に取得するのには Outlook ソーシャル コネクタ (OSC) プロバイダーがオンデマンドの同期を使用することを確認するシナリオについて説明します。
ms.openlocfilehash: 82d24b106e8d429d20a2d396eb60155cbb95f91f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804466"
---
# <a name="testing-activities"></a>アクティビティをテストします。

テストおよび以外の友人や友人の活動を適切に取得するのには Outlook ソーシャル コネクタ (OSC) プロバイダーがオンデマンドの同期を使用することを確認するシナリオについて説明します。

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>オンデマンド同期

OSC プロバイダーは、 **ISocialProvider::GetCapabilities**、プロバイダー以外の友人や友人の活動のオン ・ デマンドの同期をサポートしているかどうかを決定する、OSC を実装します。 Outlook 人物情報ウィンドウに表示されている方のため、OSC を取得、これらの方のために返されるハッシュの SMTP アドレスを[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)を呼び出して、(メモリ内) のアクティビティ データを格納します。 
  
### <a name="determining-activities-to-get"></a>取得するアクティビティを決定します。

ハッシュされた SMTP アドレスが**GetActivitiesEx**に渡されますが、OSC が友人の友人ではない活動を取得するかどうかを判断するキーです。 OSC では、人が自分のソーシャル ネットワーク アカウントの SMTP アドレスを指定する場合に、人の活動を取得します。 人には、自分のソーシャル ネットワーク アカウントでその SMTP アドレスは含まれませんか、 **GetActivitiesEx**がその人の活動を取得しませんその人が友人である場合は、ソーシャル ネットワーク上の別の電子メール アドレスで。 また、フレンドではありませんが、自分のソーシャル ネットワーク アカウントの SMTP アドレスを指定したユーザーでは、返されたデータが含まれています以外の友人にその人のプライバシーの設定で許可された使用可能なのみです。 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>友人と友人ではないテストの情報カテゴリを作成します。

友人のテストの対象を作成するには、自分のソーシャル ネットワーク アカウントでそのアドレスを含むユーザーと、そのネットワークにログオン中のユーザーとフレンドのステータスを持つユーザーの SMTP アドレスを識別します。 その SMTP アドレスを含む電子メール メッセージを作成します。 同様に、以外の友人のテストの対象を作成するには、ユーザーはそのアドレスでユーザーのログオンのフレンドではありませんし、ソーシャル ネットワーク上のプロファイルを表示するのにはフレンド以外を使用するのには自分のプライバシーの設定で指定したユーザーの SMTP アドレスを識別します。 その SMTP アドレスを含む電子メール メッセージを作成します。 
  
Outlook エクスプ ローラーで、友人 (または友人ではない) を含む電子メール メッセージを選択すると、人物情報ウィンドウは、受信者を表示します。 人物情報ウィンドウで、友人、友人ではない) を選択すると、テストするのにはプロバイダーが個人情報を提供することできます。
  
### <a name="test-scenarios"></a>シナリオをテストします。

友人と友人ではない適切な活動が発生していることを確認するには、次のシナリオをテストします。
  
|**シナリオ**|**予想される動作**|
|:-----|:-----|
|人物情報ウィンドウで選択したユーザーは、ソーシャル ネットワークにログオン中のユーザーのフレンドです。  <br/> |人物情報ウィンドウには、そのユーザーのプロファイルとソーシャル ネットワークに投稿すると、プロフィールの画像が表示されます。  <br/> |
|人物情報ウィンドウで選択されている人は、ソーシャル ネットワークにログオン中のユーザーの非友人が、友人で非表示に自分のプロファイルを許可するには。  <br/> |人物情報ウィンドウには、そのユーザーのプロファイルとソーシャル ネットワークに投稿すると、プロフィールの画像が表示されます。  <br/> |
   
## <a name="see-also"></a>関連項目

- [友人や活動を同期します。](synchronizing-friends-and-activities.md)  
- [活動の XML](xml-for-activities.md)
- [OSC プロバイダーをリリースする準備をします。](getting-ready-to-release-an-osc-provider.md)

