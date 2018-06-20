---
title: 友人のテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: このトピックでは、テストおよび該当する場合、プロバイダーでサポートされている同期モードによって、Outlook ソーシャル コネクタ (OSC) プロバイダーがその友人や、友人以外のデータを適切に返すことを確認するシナリオについて説明します。
ms.openlocfilehash: 232977836833a9ef981ebef38c9ee243ea2dd2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804481"
---
# <a name="testing-friends"></a>友人のテスト

このトピックでは、テストおよび該当する場合、プロバイダーでサポートされている同期モードによって、Outlook ソーシャル コネクタ (OSC) プロバイダーがその友人や、友人以外のデータを適切に返すことを確認するシナリオについて説明します。

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>キャッシュの同期

OSC プロバイダーは、 [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)プロバイダーが友人のデータのキャッシュの同期をサポートしているかどうかを決定する、OSC を実装します。 [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)を呼び出すと、OSC は、ソーシャル ネットワークにログオンしているユーザーの既定の Outlook ストアに特定の連絡先フォルダーに返された友人のデータを格納します。 OSC は、各フレンドのプロフィールの画像を取得するには、 [ISocialSession::GetPerson](isocialsession-getperson.md)と[ISocialPerson::GetPicture](isocialperson-getpicture.md)にも呼び出されます。 
  
### <a name="initiate-synchronization"></a>同期を開始します。

同期を開始するを有効にして、デバッグ] をクリックして**連絡先を同期する**Microsoft Office Fluent ユーザー インターフェイスのリボンのコンポーネントで。 OSC デバッグ ボタンの詳細については[、プロバイダーをデバッグ](debugging-a-provider.md)」を参照してください。 
  
### <a name="test-scenarios"></a>シナリオをテストします。

友人のデータのキャッシュが正しくことを確認するのには、次の項目をテストします。
  
|**項目をテストするには**|**予想される動作**|
|:-----|:-----|
|[連絡先] フォルダー  <br/> |ソーシャル ネットワークの特定の連絡先フォルダーは、ユーザーの既定の Outlook ストアに存在します。  <br/> |
|友人のデータを**ISocialPerson::GetFriendsAndColleagues**によって返される <br/> |各友人は、特定のネットワークの連絡先フォルダーの連絡先に対応しています。  <br/> |
|友人のデータ  <br/> |各友人の連絡先のフィールドには、正しいデータが存在します。  <br/> |
|友人のプロフィールの画像が**ISocialPerson::GetPicture**によって返される <br/> |各友人の連絡先アイテムには、プロフィールの画像が含まれています。  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>オンデマンド同期

OSC プロバイダーは、 **ISocialProvider::GetCapabilities**プロバイダーがオンデマンドの同期や友人の友人ではないをサポートするかどうかを確認するのには、OSC の呼び出しを実装します。 Outlook 人物情報ウィンドウに表示されている方のため、OSC を取得、これらの方のために返されるハッシュの SMTP アドレスを[ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)を呼び出して、(メモリ) にデータを格納します。 
  
### <a name="determining-friends-and-non-friends"></a>友人と友人ではないを決定します。

ハッシュされた SMTP アドレスが**GetPeopleDetails**に渡されますが、人が友人や友人ではないかどうかを判断するキーです。 人に自分のソーシャル ネットワーク アカウントの SMTP アドレスが含まれていない場合、またはその人がソーシャル ネットワーク上の別の電子メール アドレスで友人の場合でも、 **GetPeopleDetails**も**nonfriend**その人のとして返します、 **friendStatus** 、 _personsCollection_パラメーターにします。 また、フレンドではありませんが、自分のソーシャル ネットワーク アカウントの SMTP アドレスを指定したユーザーでは、返されたデータが含まれています以外の友人にその人のプライバシーの設定で許可された使用可能なのみです。 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>友人と友人ではないテストの情報カテゴリを作成します。

友人のテストの対象を作成するには、自分のソーシャル ネットワーク アカウントでそのアドレスを含むユーザーと、そのネットワークにログオン中のユーザーとフレンドのステータスを持つユーザーの SMTP アドレスを識別します。 その SMTP アドレスを含む電子メール メッセージを作成します。 同様に、以外の友人のテストの対象を作成するには、ユーザーの SMTP アドレスを識別する人はそのアドレスでは、ログオン中のユーザーのフレンドではありませんし、まだ、ソーシャル ネットワーク上での活動を表示するのにはフレンド以外を使用するのには自分のプライバシーの設定で指定しました。k です。 その SMTP アドレスを含む電子メール メッセージを作成します。 
  
Outlook エクスプ ローラーで、友人 (または友人ではない) を含む電子メール メッセージを選択すると、人物情報ウィンドウは、受信者を表示します。 人物情報ウィンドウで、友人、友人ではない) を選択すると、テストするのにはプロバイダーが個人情報を提供することできます。
  
### <a name="test-scenarios"></a>シナリオをテストします。

プロバイダーが友人と友人ではないについての情報を適切に提供していることを確認するには、次のシナリオでテストします。
  
|**シナリオ**|**予想される動作**|
|:-----|:-----|
|人物情報ウィンドウで選択したユーザーは、ソーシャル ネットワークにログオン中のユーザーのフレンドです。  <br/> |人物情報ウィンドウには、ソーシャル ネットワーク上の人の活動が表示されます。  <br/> |
|人物情報ウィンドウで選択されている人は、ソーシャル ネットワークにログオン中のユーザーの非友人が、友人で非表示に自分の活動が可能に。  <br/> |人物情報ウィンドウには、ソーシャル ネットワーク上の人の活動が表示されます。  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>ハイブリッド同期

OSC プロバイダーでは、友人や友人ではないのハイブリッド同期をサポートする場合、OSC は、次を行います。 
  
- OSC では、ソーシャル ネットワークに固有の連絡先フォルダーにログオンしているユーザーの友人の情報を格納します。
    
- OSC では、ソーシャル ネットワークからオン ・ デマンドの友人ではないの情報を取得し、メモリ内のみではなくフォルダーに格納します。
    
ハイブリッド同期をテストするには、[キャッシュの同期](#olosc_TestingFriends_CachedSync)で、友人のテストの推奨事項とその友人ではないの[オンデマンド同期](#olosc_TestingFriends_OnDemandSync)のセクションに従います。 
  
## <a name="see-also"></a>関連項目

- [友人や活動を同期します。](synchronizing-friends-and-activities.md) 
- [友人の XML](xml-for-friends.md)
- [OSC プロバイダーをリリースする準備をします。](getting-ready-to-release-an-osc-provider.md)

