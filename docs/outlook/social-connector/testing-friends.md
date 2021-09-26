---
title: 友だちのテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: このトピックでは、Outlook Social Connector (OSC) プロバイダーが、プロバイダーがサポートする同期モードに応じて、該当する場合は友人や友人以外のデータを適切に返すのを確認するテストとシナリオについて説明します。
ms.openlocfilehash: f882a2003675840d4096660a397f9b032a9a1e7c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608803"
---
# <a name="testing-friends"></a>友だちのテスト

このトピックでは、Outlook Social Connector (OSC) プロバイダーが、プロバイダーがサポートする同期モードに応じて、該当する場合は友人や友人以外のデータを適切に返すのを確認するテストとシナリオについて説明します。

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>キャッシュされた同期

OSC プロバイダーは [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)を実装します。これは、プロバイダーが友人のデータのキャッシュ同期をサポートするかどうかを判断するために OSC が呼び出します。 [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)を呼び出した後、OSC は、返されたフレンドのデータを、ログオンしているユーザーの既定の Outlook ストアのソーシャル ネットワークに固有の連絡先フォルダーに格納します。 また、OSC は [ISocialSession::GetPerson](isocialsession-getperson.md) と [ISocialPerson::GetPicture](isocialperson-getpicture.md) を呼び出して、各フレンドのプロファイル画像を取得します。 
  
### <a name="initiate-synchronization"></a>同期の開始

同期を開始するには、ユーザー インターフェイスのリボン コンポーネントでデバッグ ボタン [連絡先の同期] をオンMicrosoft Office Fluentできます。 OSC デバッグ ボタンの詳細については [、「Debuging a Provider 」を参照してください](debugging-a-provider.md)。 
  
### <a name="test-scenarios"></a>テスト シナリオ

次の項目をテストして、フレンドのデータが正しくキャッシュされていることを確認します。
  
|**テストするアイテム**|**予期される動作**|
|:-----|:-----|
|連絡先フォルダー  <br/> |ソーシャル ネットワーク固有の連絡先フォルダーは、ユーザーの既定の連絡先ストアにOutlookされます。  <br/> |
|ISocialPerson によって返されるフレンドのデータ **::GetFriendsAndColleagues** <br/> |各フレンドは、ネットワーク固有の連絡先フォルダー内の連絡先に対応します。  <br/> |
|フレンドのデータ  <br/> |各フレンドの連絡先フィールドに正しいデータがあります。  <br/> |
|ISocialPerson によって返されるフレンドのプロフィール **写真::GetPicture** <br/> |各フレンドの連絡先アイテムには、プロファイル画像が含まれる。  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>オンデマンド同期

OSC プロバイダーは **ISocialProvider::GetCapabilities** を実装します。これは、プロバイダーが友人と友人以外のオンデマンド同期をサポートするかどうかを判断するために OSC が呼び出します。 Outlook People Pane に表示されるユーザーの場合、OSC は SMTP アドレスを取得してハッシュし[、ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)を呼び出し、これらのユーザーに返されるデータを (メモリ内に) 格納します。 
  
### <a name="determining-friends-and-non-friends"></a>フレンドと非フレンドを決定する

**GetPeopleDetails** に渡されるハッシュ化された SMTP アドレスは、人が友人か非友人かを判断するキーです。 ユーザーが自分のソーシャル ネットワーク アカウントに SMTP アドレスを含めない場合、またはそのユーザーがソーシャル ネットワーク上の別の電子メール アドレスの友人である場合でも **、GetPeopleDetails** は _personsCollection_ パラメーターの **friendStatus** としてそのユーザーの非フレンドを返します。  また、友人ではないが、自分のソーシャル ネットワーク アカウントで SMTP アドレスを指定している人の場合、返されるデータには、そのユーザーのプライバシー設定で許可されているフレンド以外のユーザーが使用できるデータだけが含まれます。 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>友人や友人以外のテスト 対象を作成する

フレンドのテスト 対象を作成するには、そのアドレスを自分のソーシャル ネットワーク アカウントに含め、そのネットワーク上のログオンユーザーとのフレンドステータスを持つユーザーの SMTP アドレスを特定します。 その SMTP アドレスを含む電子メール メッセージを作成します。 同様に、フレンド以外のテスト 対象を作成するには、ログオンしているユーザーの友人ではないユーザーの SMTP アドレスをそのアドレスで特定し、まだ友人以外のユーザーがソーシャル ネットワーク上で自分のアクティビティを表示するためのプライバシー設定を指定しているユーザーを識別します。 その SMTP アドレスを含む電子メール メッセージを作成します。 
  
ユーザー エクスプローラー Outlook、友人 (または非フレンド) を含む電子メール メッセージを選択すると、受信者が [ユーザー ウィンドウ] に表示されます。 [ユーザー] ウィンドウでフレンド (またはフレンド以外) を選択すると、プロバイダーがユーザーに関する情報を提供しているのをテストできます。
  
### <a name="test-scenarios"></a>テスト シナリオ

プロバイダーが友人や友人以外の情報を適切に提供しているか確認するには、次のシナリオをテストします。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|[ユーザー] ウィンドウで選択されたユーザーは、ソーシャル ネットワーク上のログオンユーザーとのフレンドです。  <br/> |[ユーザー] ウィンドウには、そのユーザーのソーシャル ネットワーク上のアクティビティが表示されます。  <br/> |
|[ユーザー] ウィンドウで選択されたユーザーは、ソーシャル ネットワーク上のログオンしているユーザーの非フレンドですが、自分のアクティビティを友人以外のユーザーが表示できます。  <br/> |[ユーザー] ウィンドウには、そのユーザーのソーシャル ネットワーク上のアクティビティが表示されます。  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>ハイブリッド同期

OSC プロバイダーが友人と友人以外のハイブリッド同期をサポートしている場合、OSC は次の処理を実行します。 
  
- OSC は、ログオンしているユーザーの友人の情報をソーシャル ネットワーク固有の連絡先フォルダーに格納します。
    
- OSC は、フレンド以外のオンデマンドの情報をソーシャル ネットワークから取得し、メモリにのみ格納しますが、フォルダーには格納できません。
    
ハイブリッド同期をテストするには、友人の [キャッシュされた[](#olosc_TestingFriends_CachedSync)同期] セクションのテストの提案に従い[](#olosc_TestingFriends_OnDemandSync)、友人以外の場合は [オンデマンド同期] セクションのテストの提案に従います。 
  
## <a name="see-also"></a>関連項目

- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md) 
- [友人のための XML](xml-for-friends.md)
- [OSC プロバイダーをリリースする準備](getting-ready-to-release-an-osc-provider.md)

