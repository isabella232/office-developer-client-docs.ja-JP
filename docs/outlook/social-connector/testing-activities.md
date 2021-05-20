---
title: アクティビティのテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: このトピックでは、Outlook Social Connector (OSC) プロバイダーがオンデマンド同期を使用して友人や友人以外のアクティビティを適切に返すのを確認するテストとシナリオについて説明します。
ms.openlocfilehash: 0a40dca84681a9e758c2f17d2647c339ded70462
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436301"
---
# <a name="testing-activities"></a>アクティビティのテスト

このトピックでは、Outlook Social Connector (OSC) プロバイダーがオンデマンド同期を使用して友人や友人以外のアクティビティを適切に返すのを確認するテストとシナリオについて説明します。

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>オンデマンド同期

OSC プロバイダーは **、ISocialProvider::GetCapabilities** を実装します。これは、プロバイダーが友人や友人以外のアクティビティのオンデマンド同期をサポートするかどうかを判断するために OSC が呼び出します。 Outlook People Pane に表示されるユーザーの場合、OSC は SMTP アドレスを取得してハッシュし[、ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)を呼び出し、これらのユーザーに返されるアクティビティ データを (メモリ内に) 格納します。 
  
### <a name="determining-activities-to-get"></a>取得するアクティビティの決定

**GetActivitiesEx** に渡されるハッシュ化された SMTP アドレスは、OSC がフレンドまたは非フレンドのアクティビティを取得するかどうかを決定するキーです。 ユーザーが自分のソーシャル ネットワーク アカウントで SMTP アドレスを指定した場合、OSC はユーザーのアクティビティを取得します。 そのユーザーが自分のソーシャル ネットワーク アカウントに SMTP アドレスを含めない場合、またはそのユーザーが友人で、ソーシャル ネットワーク上の別の電子メール アドレスである場合 **、GetActivitiesEx** は、そのユーザーのアクティビティを取得できません。 また、友人ではないが、自分のソーシャル ネットワーク アカウントで SMTP アドレスを指定している人の場合、返されるデータには、そのユーザーのプライバシー設定で許可されているフレンド以外のユーザーが使用できるデータだけが含まれます。 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>友人や友人以外のテスト 対象を作成する

フレンドのテスト 対象を作成するには、そのアドレスを自分のソーシャル ネットワーク アカウントに含め、そのネットワーク上のログオンユーザーとのフレンドステータスを持つユーザーの SMTP アドレスを特定します。 その SMTP アドレスを含む電子メール メッセージを作成します。 同様に、フレンド以外のテスト 対象を作成するには、そのアドレスでログオンしているユーザーの友人ではないユーザーの SMTP アドレスを特定し、友人以外のユーザーがソーシャル ネットワーク上で自分のプロファイルを表示するためのプライバシー設定で指定したユーザーの SMTP アドレスを特定します。 その SMTP アドレスを含む電子メール メッセージを作成します。 
  
ユーザー エクスプローラー Outlook、友人 (または非フレンド) を含む電子メール メッセージを選択すると、受信者が [ユーザー ウィンドウ] に表示されます。 [ユーザー] ウィンドウでフレンド (またはフレンド以外) を選択すると、プロバイダーがユーザーに関する情報を提供しているのをテストできます。
  
### <a name="test-scenarios"></a>テスト シナリオ

友人や友人以外のユーザーに適切なアクティビティを取得しているか確認するには、次のシナリオをテストします。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|[ユーザー] ウィンドウで選択されたユーザーは、ソーシャル ネットワーク上のログオンユーザーとのフレンドです。  <br/> |[ユーザー] ウィンドウには、ソーシャル ネットワークに投稿されたユーザーのプロファイルとプロファイル画像が表示されます。  <br/> |
|[ユーザー] ウィンドウで選択されたユーザーは、ソーシャル ネットワーク上のログオンしているユーザーの非フレンドですが、自分のプロファイルを友人以外のユーザーが表示できます。  <br/> |[ユーザー] ウィンドウには、ソーシャル ネットワークに投稿されたユーザーのプロファイルとプロファイル画像が表示されます。  <br/> |
   
## <a name="see-also"></a>関連項目

- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)  
- [アクティビティの XML](xml-for-activities.md)
- [OSC プロバイダーをリリースする準備](getting-ready-to-release-an-osc-provider.md)

