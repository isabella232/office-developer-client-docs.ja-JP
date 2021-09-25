---
title: 友だち用 XML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: Microsoft Outlook Social Connector (OSC) プロバイダー XML スキーマの friends 要素を使用すると、OSC プロバイダーは、ソーシャル ネットワーク内の Outlook ユーザーに関連付けられたユーザーの一覧に関する情報を指定できます。
ms.openlocfilehash: a6d8dbe78e40f94ea5fe30e7361b37ef05c46a02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590346"
---
# <a name="xml-for-friends"></a>友だち用 XML

Microsoft  Outlook Social Connector (OSC) プロバイダー XML スキーマの friends 要素を使用すると、OSC プロバイダーは、ソーシャル ネットワーク内の Outlook ユーザーに関連付けられているユーザーの一覧に関する情報を指定できます。 OSC プロバイダーがキャッシュ同期をサポートしている場合、このユーザーの一覧には、ソーシャル ネットワーク上のユーザー Outlookのフレンドだけが含まれる。 OSC がオンデマンド同期またはハイブリッド同期をサポートしている場合、このリストには、ユーザーのフレンドとフレンド以外のOutlookがあります。 

リスト内の各ユーザーは、名、名、電子メール アドレスなどの詳細をサポートする XML スキーマの person 要素として表されます。 OSC プロバイダーは、OSCがソーシャル ネットワークからフレンド情報を同期する方法に関係なく、フレンド要素と人物要素を使用します。  ソーシャル ネットワークが Outlook連絡先フォルダーへの友人のキャッシュまたはハイブリッド同期をサポートしている場合、人の子要素は Outlook 連絡先のプロパティの一部に似ています。これは、ソーシャル ネットワークに固有の Outlook 連絡先フォルダーに友人を保存する際に便利です。 

## <a name="example-scenarios"></a>シナリオ例

次のシナリオ例は、OSC プロバイダーが実装する OSC プロバイダー拡張 API 呼び出しと、OSC がフレンド情報を取得するために行う呼び出しを示しています。 情報は、OSC プロバイダー XML スキーマに準拠した XML 文字列で表されます。
  
フレンド XML の例については、「Friends [XML の例」を参照してください](friends-xml-example.md)。 友人の情報の同期の詳細については、「友人とアクティビティの同期 [」を参照してください](synchronizing-friends-and-activities.md)。

### <a name="scenario-1-get-a-list-of-friends"></a>シナリオ 1: フレンドのリストを取得する

シナリオ 1: OSC はフレンドのリストと [、ISocialPerson](isocialpersoniunknown.md) オブジェクトと各フレンドの画像を取得します。 
    
1. ソーシャル ネットワーク サイトからフレンドを表示し、OSC がフレンド情報をキャッシュすることをサポートする OSC プロバイダーは **、getFriends** 要素と **cacheFriends** 要素 **(capabilities** 要素の子要素) を使用して OSC に対してそれを示します。 
    
2. OSC プロバイダーは[、ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) [、ISocialSession::GetPerson、ISocialPerson::GetFriendsAndColleagues、](isocialsession-getperson.md)および[ISocialPerson::GetPicture](isocialperson-getpicture.md)メソッドも実装します。 [](isocialperson-getfriendsandcolleagues.md) 
    
3. OSC は **ISocialProvider::GetCapabilities** を呼び出して、次の要素の値を確認します **。getFriends** は、OSC プロバイダーがソーシャル ネットワークからのフレンドの表示をサポートし **、cacheFriends** を使用してプロバイダーが友人のキャッシュをサポートしているのを確認します。 
    
4. OSC は **ISocialSession::GetPerson** を呼び出して、ユーザーの **ISocialPerson** オブジェクトOutlookします。 
    
5. OSC は **ISocialPerson::GetFriendsAndColleagues** を呼び出して _、personCollection_ パラメーター文字列で返される Outlook ユーザーのフレンド リストを取得します。 _personCollection 文字列_ は、XML スキーマの **friends** 要素の XML スキーマ定義に準拠しています。 
    
6. _personCollection_ XML 文字列内のフレンドごとに、OSC は **userID** 要素の値を取得して **ISocialSession::GetPerson** を呼び出して、そのフレンドの **ISocialPerson** オブジェクトを取得します。 
    
7. **personCollection** XML 文字列内の各フレンドについて、OSC は [ISocialPerson::GetPicture](isocialperson-getpicture.md)を呼び出して、そのフレンドの画像リソースを取得します。 
    
   OSC は **、ISocialPerson** オブジェクトをさらに呼び出して、そのフレンドのアクティビティと詳細 (電子メール アドレスなど) を取得できます。 
    
### <a name="scenario-2-synchronize-friends"></a>シナリオ 2: 友人の同期 

シナリオ 2:OSC はフレンドを動的に同期します。
    
1. フレンドとフレンド以外のオンデマンド同期をサポートする OSC プロバイダーは **、getFriends** 要素と **dynamicContactsLookup** 要素を使用して OSC に対してそれを示します。 OSC プロバイダーは **、hashFunction 要素も設定** します。 3 つの要素はすべて、機能の子 **要素です**。 
    
2. OSC プロバイダーは [、ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) メソッドも実装します。 
    
3. OSC は **ISocialProvider::GetCapabilities** を呼び出して **getFriends** と **dynamicContactsLookup** の値を確認し、OSC プロバイダーが友人と友人以外のフレンドとオンデマンド同期をサポートしているか確認します。 OSC は、OSC プロバイダーがサポートする **hashFunction** の値もメモします。 
    
4. ユーザー ウィンドウに表示されるユーザーごとに、OSC はユーザーの電子メール アドレスを収集し **、hashFunction** で指定されたハッシュ関数を使用して暗号化します。 これは、hashedAddresses 要素の XML スキーマ定義に準拠する **XML 文字列を形成** します。 
    
5. OSC は **ISocialSession2::GetPeopleDetails** を呼び出し  _、personAddresses_ パラメーターとしてハッシュされたアドレスのこの XML 文字列を提供し  _、personsCollection_ パラメーターのユーザーの更新された詳細を動的に取得します。 _personsCollection_ パラメーター文字列は、XML スキーマの **friends** 要素の XML スキーマ定義に準拠しています。 

## <a name="parent-and-child-elements"></a>親要素と子要素

フレンド スキーマの 2 つのトップ レベル要素を **次に示** します。 
  
|**Element**|**説明**|
|:-----|:-----|
|**フレンド** <br/> |ユーザー要素のリストのルート要素を **表** します。 **ISocialPerson::GetFriendsAndColleagues** [、ISocialSession::FindPerson、](isocialsession-findperson.md)**および ISocialSession2::GetPeopleDetails** は **、friends** 要素のスキーマ定義に準拠する XML 文字列を返します。  <br/> |
|**人** <br/> |ユーザー要素のリスト内の 1 人のユーザー **を表** します。 [ISocialPerson::GetDetails](isocialperson-getdetails.md)メソッドは、person 要素のスキーマ定義に準拠する XML 文字列を **返** します。  <br/> |
   
次の表では、OSC プロバイダー XML スキーマ内の **person** 要素の各子要素について説明します。 
  
OSC プロバイダー XML スキーマの完全な定義 (必須または省略可能な要素を含む) については、「ソーシャル コネクタ プロバイダー XML スキーマOutlook[を参照してください](outlook-social-connector-provider-xml-schema.md)。
  
|**Element**|**説明**|
|:-----|:-----|
|**address** <br/> |人物の物理的な住所。  <br/> |
|**記念日** <br/> |ユーザーのイベントの記念日。  <br/> |
|**askmeabout** <br/> |人物の関心や専門知識に関するトピック。  <br/> |
|**birthday** <br/> |その人の生年月日。  <br/> |
|**businessAddress** <br/> |ユーザーの職場の物理的な住所。  <br/> |
|**businessCity** <br/> |ユーザーの職場の市区町場。  <br/> |
|**businessCountryOrRegion** <br/> |ユーザーの職場の国または地域。  <br/> |
|**businessState** <br/> |ユーザーの職場の州または州。  <br/> |
|**businessZip** <br/> |ユーザーの職場の郵便番号または郵便番号。  <br/> |
|**セル** <br/> |ユーザーの携帯電話番号。  <br/> |
|**city** <br/> |ユーザーの物理アドレスの都市。  <br/> |
|**company** <br/> |ユーザーに関連付けられている会社の名前。  <br/> |
|**countryOrRegion** <br/> |ユーザーの物理アドレスの国または地域。  <br/> |
|**creationTime** <br/> |ソーシャル ネットワーク上のユーザーのプロファイルの作成時間。  <br/> |
|**emailAddress** <br/> |ユーザーのプライマリ 電子メール アドレス。  <br/> |
|**emailAddress2** <br/> |ユーザーのセカンダリ メール アドレス。  <br/> |
|**emailAddress3** <br/> |ユーザーの第 3 の電子メール アドレス。  <br/> |
|**expirationTime** <br/> |ユーザーのプロファイル データがソーシャル ネットワークで期限切れになる時間。  <br/> |
|**fileAs** <br/> |ユーザーが連絡先ファイル内の連絡先としてファイルされる文字列Outlook指定します。  <br/> |
|**firstName** <br/> |ユーザーの名または名前を指定します。  <br/> |
|**friendStatus** <br/> |ソーシャル ネットワーク上のログオンユーザーを持つこのユーザーのフレンド状態。 friend 、 **nonfriend**、 **pending**、 **pendingin**、 **pendingout** の値のいずれかを指定 **する必要があります**。  <br/> |
|**fullName** <br/> |ユーザーの完全な名前。  <br/> |
|**性別** <br/> |人の性別。 次のいずれかの値を指定する必要 **があります****。**   <br/> |
|**homePhone** <br/> |ユーザーの自宅の電話番号。  <br/> |
|**index** <br/> |**ISocialSession2::GetPeopleDetails** メソッドの呼び出しに渡される _personsAddresses_ 文字列パラメーター内の人物のハッシュされたアドレスの場所。 また **、GetPeopleDetails** によって返される _personsCollection_ 文字列内の人物 XML も示します。   <br/> |
|**業界** <br/> |その人が従事している業界。  <br/> |
|**interests** <br/> |その人の興味や趣味。  <br/> |
|**lastModificationTime** <br/> |ソーシャル ネットワークでユーザーのプロファイルが最後に変更された時刻。  <br/> |
|**lastName** <br/> |ユーザーの姓または姓。  <br/> |
|**location** <br/> |ユーザーの場所。  <br/> |
|**ニックネーム** <br/> |人物の短い名前または発明された名前。  <br/> |
|**otherAddress** <br/> |ユーザーの代替の住所。  <br/> |
|**otherCity** <br/> |ユーザーの代替住所の都市。  <br/> |
|**otherCountryOrRegion** <br/> |ユーザーの代替住所の国または地域。  <br/> |
|**otherState** <br/> |ユーザーの代替住所の州または州。  <br/> |
|**otherZip** <br/> |ユーザーの代替住所の郵便番号または郵便番号。  <br/> |
|**電話** <br/> |ユーザーのプライマリ連絡先電話番号。  <br/> |
|**pictureUrl** <br/> |ユーザーのプロファイル画像の URL。  <br/> |
|**リレーションシップ** <br/> |このユーザーとログオンしているユーザーとの関係。  <br/> |
|**schools** <br/> |その人が行く、または行った学校。  <br/> |
|**skills** <br/> |個人のスキル。  <br/> |
|**state** <br/> |ユーザーの物理的な住所の状態または州。  <br/> |
|**title** <br/> |ユーザーの名前に追加された指定。  <br/> |
|**userID** <br/> |ソーシャル ネットワーク上のユーザーを識別するための ID。  <br/> |
|**webProfilePage** <br/> |ユーザーのプロファイルを含む Web ページ アドレス。  <br/> |
|**Web サイト** <br/> |ユーザーの Web サイト。  <br/> |
|**workPhone** <br/> |ユーザーのビジネス電話番号。  <br/> |
|**zip** <br/> |人の物理的な住所の郵便番号または郵便番号。  <br/> |
   
## <a name="see-also"></a>関連項目

- [Friends XML の例](friends-xml-example.md)  
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)  
- [機能の XML](xml-for-capabilities.md) 
- [アクティビティの XML](xml-for-activities.md)
- [OSC XML スキーマを使用したプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

