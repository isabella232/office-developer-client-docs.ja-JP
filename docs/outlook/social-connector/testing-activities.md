---
title: アクティビティのテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: このトピックでは、Outlook Social Connector (.osc) プロバイダーが、オンデマンド同期を使用して友人や非友人の活動を適切に返すことを確認するテストとシナリオについて説明します。
ms.openlocfilehash: 0a40dca84681a9e758c2f17d2647c339ded70462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329205"
---
# <a name="testing-activities"></a>アクティビティのテスト

このトピックでは、Outlook Social Connector (.osc) プロバイダーが、オンデマンド同期を使用して友人や非友人の活動を適切に返すことを確認するテストとシナリオについて説明します。

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>オンデマンド同期

.osc プロバイダーは、 **isocialprovider:: getcapabilities**を実装します。この関数は、プロバイダーが友人および非友人のアクティビティのオンデマンド同期をサポートしているかどうかを判断するために、.osc を呼び出します。 [Outlook People] ウィンドウに表示される人物については、.osc は SMTP アドレスを取得してハッシュし、 [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)を呼び出します。また、これらのユーザーに対して返されるアクティビティデータをメモリ内に格納します。 
  
### <a name="determining-activities-to-get"></a>取得するアクティビティの決定

**GetActivitiesEx**に渡されるハッシュされた SMTP アドレスは、.osc がフレンドまたはフレンド以外のアクティビティを取得するかどうかを判断するための鍵となります。 .osc は、ユーザーがソーシャルネットワークアカウントでその SMTP アドレスを指定した場合に、そのユーザーのアクティビティを取得します。 その SMTP アドレスが自分のソーシャルネットワークアカウントに含まれていない場合、またはそのユーザーがソーシャルネットワーク上の他の電子メールアドレスで友人である場合、 **GetActivitiesEx**はその人物のアクティビティを取得しません。 また、友人以外のユーザーがソーシャルネットワークアカウントの SMTP アドレスを指定している場合、返されるデータには、そのユーザーのプライバシー設定によって許可されている場合に、フレンド以外に対して使用可能なもののみが含まれます。 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>友人および非友人のテスト対象を作成する

友人のテスト件名を作成するには、そのアドレスをソーシャルネットワークアカウントに含めるユーザーの SMTP アドレスを識別し、そのネットワークでログオンしているユーザーのフレンド状態を持っているユーザーを特定します。 その SMTP アドレスを含む電子メールメッセージを作成します。 同様に、フレンド以外のテスト件名を作成するには、そのアドレスによってログオンしているユーザーのフレンドではないユーザーの SMTP アドレスを識別し、自分のプライバシー設定で指定したユーザーがソーシャルネットワークで自分のプロファイルを表示できないようにします。 その SMTP アドレスを含む電子メールメッセージを作成します。 
  
Outlook エクスプローラーで、友達 (または友人以外) を含む電子メールメッセージを選択すると、[人] ウィンドウに受信者が表示されます。 [人] ウィンドウで友人 (または友人以外) を選択すると、プロバイダーがその人物に関する情報を提供しているかどうかをテストできます。
  
### <a name="test-scenarios"></a>テスト シナリオ

友人や友人以外の適切な活動を取得していることを確認するには、次のシナリオをテストします。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|[人] ウィンドウで選択されたユーザーは、ソーシャルネットワーク上でログオンしているユーザーと友人になります。  <br/> |[人] ウィンドウには、ソーシャルネットワークに投稿されたユーザーのプロファイルとプロファイル画像が表示されます。  <br/> |
|People ウィンドウで選択されたユーザーは、ソーシャルネットワーク上のログオンしているユーザーのフレンドではありませんが、自分のプロファイルを友人以外に表示することが許可されています。  <br/> |[人] ウィンドウには、ソーシャルネットワークに投稿されたユーザーのプロファイルとプロファイル画像が表示されます。  <br/> |
   
## <a name="see-also"></a>関連項目

- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)  
- [アクティビティの XML](xml-for-activities.md)
- [.osc プロバイダーをリリースする準備をする](getting-ready-to-release-an-osc-provider.md)

