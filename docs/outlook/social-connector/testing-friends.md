---
title: 友だちのテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: このトピックでは、プロバイダーがサポートする同期モードに応じて、Outlook Social Connector (.osc) プロバイダーが友人および友人以外のデータを適切に返すことを確認するテストとシナリオについて説明します。
ms.openlocfilehash: 1c97342fd5b219b15b1f58dbc065fc268f8e81d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433669"
---
# <a name="testing-friends"></a>友だちのテスト

このトピックでは、プロバイダーがサポートする同期モードに応じて、Outlook Social Connector (.osc) プロバイダーが友人および友人以外のデータを適切に返すことを確認するテストとシナリオについて説明します。

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>キャッシュされた同期

.osc プロバイダーは、 [isocialprovider:: getcapabilities](isocialprovider-getcapabilities.md)を実装します。この関数は、プロバイダーがフレンドのデータのキャッシュ同期をサポートしているかどうかを判断するために、.osc 呼び出しを行います。 [iGetFriendsAndColleagues alperson::](isocialperson-getfriendsandcolleagues.md)を呼び出すと、.osc は、ログオンユーザーの既定の Outlook ストアで、返されたフレンドのデータをソーシャルネットワーク固有の連絡先フォルダーに格納します。 また、次のようにして、各フレンドのプロファイル画像を取得するために、 [isocialsession:: getperson](isocialsession-getperson.md)および[iな alperson:: getperson](isocialperson-getpicture.md)を呼び出します。 
  
### <a name="initiate-synchronization"></a>同期を開始する

同期を開始するには、Microsoft Office Fluent ユーザーインターフェイスのリボンコンポーネントで [デバッグ] ボタンをオンにして、その**連絡先**を使用します。 [デバッグ] ボタンの詳細については、「[プロバイダーをデバッグする](debugging-a-provider.md)」を参照してください。 
  
### <a name="test-scenarios"></a>テスト シナリオ

次の項目をテストして、友人のデータが正しくキャッシュされていることを確認します。
  
|**テストするアイテム**|**予期される動作**|
|:-----|:-----|
|連絡先フォルダー  <br/> |ソーシャルネットワーク固有の連絡先フォルダーは、ユーザーの既定の Outlook ストアに存在します。  <br/> |
|iGetFriendsAndColleagues によって返されるフレンドのデータ **::** <br/> |各フレンドは、ネットワーク固有の連絡先フォルダー内の連絡先に対応します。  <br/> |
|Friends のデータ  <br/> |各フレンドの連絡先フィールドに適切なデータがあります。  <br/> |
|i入力されたユーザーによって返される友人のプロファイル画像 **:: getpicture** <br/> |各フレンドの連絡先アイテムには、プロフィール画像が含まれています。  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>オンデマンド同期

.osc プロバイダーは、 **isocialprovider:: getcapabilities**を実装します。この関数は、プロバイダーが友人および非友人のオンデマンド同期をサポートしているかどうかを判断するために、.osc を呼び出します。 [Outlook People] ウィンドウに表示される人物については、.osc は SMTP アドレスを取得してハッシュし、 [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)を呼び出し、これらのユーザーに対して返されるデータを (メモリ内に) 保存します。 
  
### <a name="determining-friends-and-non-friends"></a>友人と非友人を決定する

**GetPeopleDetails**に渡されるハッシュされた SMTP アドレスは、ユーザーがフレンドであるか友人であるかを判断するための鍵となります。 自分のソーシャルネットワークアカウントにその SMTP アドレスが含まれていない場合や、その人物がソーシャルネットワーク上の別の電子メールアドレスによって友人である場合でも、 **GetPeopleDetails**は、 **** **その人物に対して非フレンドをfriendStatus**は、_個人コレクション_のパラメーターです。 また、友人以外のユーザーがソーシャルネットワークアカウントで SMTP アドレスを指定している場合、返されるデータには、そのユーザーのプライバシー設定によって許可されている場合に、フレンド以外に対して使用可能なもののみが含まれます。 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>友人および非友人のテスト対象を作成する

友人のテスト件名を作成するには、そのアドレスをソーシャルネットワークアカウントに含めるユーザーの SMTP アドレスを識別し、そのネットワークでログオンしているユーザーのフレンド状態を持っているユーザーを特定します。 その SMTP アドレスを含む電子メールメッセージを作成します。 同様に、フレンド以外のテスト件名を作成するには、そのアドレスによってログオンしているユーザーのフレンドではないユーザーの SMTP アドレスを識別します。さらに、そのユーザーのプライバシー設定で指定されているユーザーが、自分のプライバシー設定で、そのユーザーのアクティビティをソーシャル networ で表示できないようにします。万. その SMTP アドレスを含む電子メールメッセージを作成します。 
  
Outlook エクスプローラーで、友達 (または友人以外) を含む電子メールメッセージを選択すると、[人] ウィンドウに受信者が表示されます。 [人] ウィンドウで友人 (または友人以外) を選択すると、プロバイダーがその人物に関する情報を提供しているかどうかをテストできます。
  
### <a name="test-scenarios"></a>テスト シナリオ

プロバイダーが友人や友人以外に関する情報を適切に提供しているかどうかを確認するには、次のシナリオをテストします。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|[人] ウィンドウで選択されたユーザーは、ソーシャルネットワーク上でログオンしているユーザーと友人になります。  <br/> |[人] ウィンドウには、ソーシャルネットワーク上のその人物の活動が表示されます。  <br/> |
|People ウィンドウで選択されたユーザーは、ソーシャルネットワーク上のログオンしているユーザーのフレンドではありませんが、自分のアクティビティを友人以外のユーザーに表示することが許可されています。  <br/> |[人] ウィンドウには、ソーシャルネットワーク上のその人物の活動が表示されます。  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>ハイブリッド同期

.osc プロバイダーが友人と友人以外のハイブリッド同期をサポートしている場合、.osc は次の処理を行います。 
  
- .osc は、ログオンしているユーザーのフレンドの情報をソーシャルネットワーク固有の連絡先フォルダーに格納します。
    
- .osc は、ソーシャルネットワークから非友人の情報を取得し、それをフォルダー内に格納するのではなく、メモリのみに格納します。
    
ハイブリッド同期をテストするには、友人のキャッシュされた[同期](#olosc_TestingFriends_CachedSync)セクションのテスト提案と、非友人の場合は「[オンデマンド同期](#olosc_TestingFriends_OnDemandSync)」セクションのテスト候補に従います。 
  
## <a name="see-also"></a>関連項目

- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md) 
- [Friends の XML](xml-for-friends.md)
- [.osc プロバイダーをリリースする準備をする](getting-ready-to-release-an-osc-provider.md)

