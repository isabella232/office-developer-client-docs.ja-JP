---
title: 友人の XML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: Microsoft Outlook ・ ソーシャル コネクタ (OSC) プロバイダーの XML スキーマで友人の要素では、ソーシャル ネットワークでは、Outlook ユーザーに関連付けられている担当者の一覧についての情報を指定するのには、OSC プロバイダーを使用します。
ms.openlocfilehash: 07f1bb77e7912e3973fd2af8a70275642b72039c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804485"
---
# <a name="xml-for-friends"></a>友人の XML

Microsoft Outlook ・ ソーシャル コネクタ (OSC) プロバイダーの XML スキーマで**友人**の要素では、ソーシャル ネットワークでは、Outlook ユーザーに関連付けられている担当者の一覧についての情報を指定するのには、OSC プロバイダーを使用します。 OSC プロバイダーは、キャッシュの同期をサポートする場合、ソーシャル ネットワーク上の Outlook ユーザーのフレンドのみがこの人の一覧に含まれます。 OSC では、オン ・ デマンドまたはハイブリッドの同期をサポートする場合このリストは Outlook ユーザーの非友人や友人の両方を含む可能性があります。 

リストの各メンバーは、**人**名、姓、名、電子メール アドレスなどの詳細情報をサポートする XML スキーマで要素として表されます。 OSC プロバイダーでは、ソーシャル ネットワークからの友人の情報を同期するのには OSC、必要な方法に関係なく、**友人**や**人**の要素を使用します。 **人**の子要素は、ソーシャル ネットワークをサポートしていますがキャッシュされている場合は、ソーシャル ネットワークに特定の Outlook 連絡先フォルダー内のファイルを格納する友人を容易にする、Outlook の連絡先のプロパティ、またはハイブリッドのいくつかのようなことに注意してください。友人が Outlook の連絡先フォルダーに同期します。 

## <a name="example-scenarios"></a>シナリオの例

次の例のシナリオでは、機能拡張 API の呼び出し、OSC プロバイダーを実装し、OSC は友人の情報を取得するのには、OSC プロバイダーを表示します。 情報は、OSC プロバイダーの XML スキーマに準拠する XML 文字列で表されます。
  
友人 XML の例は、[友人の XML の例](friends-xml-example.md)を参照してください。 友人の情報を同期の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。

### <a name="scenario-1-get-a-list-of-friends"></a>シナリオ 1: 友人の一覧を取得します。

シナリオ 1: OSC は、各友人の友人、および[ISocialPerson](isocialpersoniunknown.md)オブジェクトや画像の一覧を取得します。 
    
1. OSC プロバイダーをサポートしているソーシャル ネットワーク サイトからのフレンドを表示させ、OSC フレンド情報をキャッシュすることを示します、OSC を**の子要素は、 **getFriends**と**cacheFriends**要素を使用して機能**要素です。 
    
2. OSC プロバイダーでは、 [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)、 [ISocialSession::GetPerson](isocialsession-getperson.md)、 [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)、および[ISocialPerson::GetPicture](isocialperson-getpicture.md)メソッドも実装します。 
    
3. OSC は、次の要素の値を確認するのには**ISocialProvider::GetCapabilities**を呼び出します: OSC プロバイダーはプロバイダーのことを確認するのには、ソーシャル ネットワーク、および**cacheFriends**からのフレンドを表示をサポートすることを確認するのには**getFriends**友人のキャッシュをサポートしています。 
    
4. OSC では、Outlook のユーザーの**ISocialPerson**オブジェクトを取得する**ISocialSession::GetPerson**を呼び出します。 
    
5. Outlook のユーザーを取得する**ISocialPerson::GetFriendsAndColleagues**を呼び出して、OSC の_personCollection_パラメーターの文字列にフレンド リストが返されます。 _PersonCollection_文字列は、XML スキーマ内の**フレンド**要素の XML スキーマ定義に準拠します。 
    
6. _PersonCollection_ XML 文字列内の各友人は、OSC は、その友人の**ISocialPerson**オブジェクトを取得する**ISocialSession::GetPerson**を呼び出すための**ユーザー Id**要素の値を取得します。 
    
7. OSC は**personCollection** XML 文字列内の各フレンドのフレンドの画像リソースを取得するのには[ISocialPerson::GetPicture](isocialperson-getpicture.md)を呼び出します。 
    
   OSC さらに加えることの活動と詳細情報 (電子メール アドレスなど) を取得する**ISocialPerson**オブジェクトでの呼び出しその友人。 
    
### <a name="scenario-2-synchronize-friends"></a>シナリオ 2: 同期の友人 

シナリオ 2: OSC は、友人を動的に同期します。
    
1. OSC プロバイダー以外の友人や友人のオン ・ デマンドの同期をサポートすることを示します、OSC を**getFriends**と**dynamicContactsLookup**の要素を使用しています。 OSC プロバイダーも**実装しています。** 要素を設定します。 3 つすべての要素は、**機能**の子要素です。 
    
2. OSC プロバイダーでは、 [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)メソッドも実装します。 
    
3. OSC では、 **getFriends**友人や、オンデマンドの同期の友人と友人ではない、OSC プロバイダーがサポートしていることを確認するのには**dynamicContactsLookup**の値を確認するのには**ISocialProvider::GetCapabilities**を呼び出します。 OSC は、**実装しています。** OSC プロバイダーでサポートされているの値をメモにもなります。 
    
4. 、人物情報ウィンドウに表示される各ユーザーの、OSC はユーザーの電子メール アドレスを収集し、それを**実装しています。** で指定されたハッシュ関数を使用して暗号化します。 これは、 **hashedAddresses**要素の XML スキーマ定義に準拠する XML 文字列を形成します。 
    
5. OSC では、 **ISocialSession2::GetPeopleDetails**、 _personAddresses_のパラメーターとして、ハッシュ化されたアドレスの場合は、この XML 文字列を提供する_personsCollection_パラメーターでは、担当者の更新の詳細情報を動的に取得するを呼び出します。 _PersonsCollection_パラメーターの文字列は、XML スキーマ内の**フレンド**要素の XML スキーマ定義に準拠します。 

## <a name="parent-and-child-elements"></a>親要素と子要素

**友人**スキーマの 2 つの最上位レベル要素を次に示します。 
  
|**要素**|**説明**|
|:-----|:-----|
|**友人** <br/> |**人**の要素の一覧のルート要素を表します。 **ISocialPerson::GetFriendsAndColleagues**、 [ISocialSession::FindPerson](isocialsession-findperson.md)、および**ISocialSession2::GetPeopleDetails**は、**友人**の要素のスキーマ定義に準拠する XML 文字列を返します。  <br/> |
|**人物** <br/> |**人**の要素の一覧で 1 人のユーザーを表します。 [ISocialPerson::GetDetails](isocialperson-getdetails.md)メソッドでは、**人**の要素のスキーマ定義に準拠する XML 文字列を返します。  <br/> |
   
OSC プロバイダーの XML スキーマ内の**ユーザー**要素の子要素を次の表に示します。 
  
のどの要素には、必須またはオプションを含む、OSC プロバイダーの XML スキーマの完全な定義は、 [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)を参照してください。
  
|**要素**|**説明**|
|:-----|:-----|
|**アドレス** <br/> |人の物理的な住所。  <br/> |
|**記念日** <br/> |イベント、個人の記念日。  <br/> |
|**askmeabout** <br/> |利息またはユーザーの専門知識のトピックを示します。  <br/> |
|**誕生日** <br/> |担当者の生年月日の日付です。  <br/> |
|**businessAddress** <br/> |人の職場の物理的な住所。  <br/> |
|**businessCity** <br/> |人の職場の市町村。  <br/> |
|**businessCountryOrRegion** <br/> |国または地域のワークプ レースです。  <br/> |
|**businessState** <br/> |人の職場の都道府県です。  <br/> |
|**businessZip** <br/> |郵便番号の人の職場です。  <br/> |
|**セル** <br/> |担当者の携帯電話番号です。  <br/> |
|**市区町村** <br/> |個人の住所の市町村。  <br/> |
|**会社** <br/> |ユーザーに関連付けられている会社の名前です。  <br/> |
|**countryOrRegion** <br/> |国または地域の人の住所です。  <br/> |
|**creationTime** <br/> |ソーシャル ネットワーク上のユーザーのプロファイルの作成時刻です。  <br/> |
|**emailAddress** <br/> |ユーザーのプライマリ電子メール アドレスです。  <br/> |
|**emailAddress2** <br/> |ユーザーのセカンダリ電子メール アドレスです。  <br/> |
|**emailAddress3** <br/> |人の 3 番目の電子メール アドレスです。  <br/> |
|**expirationTime** <br/> |ソーシャル ネットワークのユーザーのプロファイル データの有効期限時間。  <br/> |
|**表題** <br/> |人は、Outlook で連絡先ファイルを連絡先として登録する文字列です。  <br/> |
|**firstName** <br/> |名またはユーザーの名前を指定します。  <br/> |
|**friendStatus** <br/> |ソーシャル ネットワークにログオンしたユーザーがこのユーザーのフレンドの状態です。 次の値のいずれかである必要があります:**友人**、 **nonfriend**、**保留中**、 **pendingin**、 **pendingout**。  <br/> |
|**fullName** <br/> |ユーザーの完全名。  <br/> |
|**性別** <br/> |人の性別です。 次の値のいずれかである必要があります: **(オス)**、 **(メス)**、**指定されていません**。  <br/> |
|**homePhone** <br/> |ユーザーの自宅電話番号です。  <br/> |
|**index** <br/> |_PersonsAddresses_文字列パラメーターでのユーザーのハッシュ化されたアドレスの場所は、 **ISocialSession2::GetPeopleDetails**メソッドの呼び出しに渡されます。 人の**人**XML の**GetPeopleDetails**によって返される_personsCollection_の文字列を示します。  <br/> |
|**業界** <br/> |人が行っている業界です。  <br/> |
|**興味のあること** <br/> |興味や趣味の人です。  <br/> |
|**lastModificationTime** <br/> |ソーシャル ネットワークのユーザーのプロファイルが最後に変更された時刻です。  <br/> |
|**lastName** <br/> |最後の名前またはユーザーの姓です。  <br/> |
|**location** <br/> |人の場所です。  <br/> |
|**ニックネーム** <br/> |短い名前、またはユーザーの名前が作成されました。  <br/> |
|**かまいません** <br/> |人の代替住所です。  <br/> |
|**otherCity** <br/> |人の代替住所の市町村。  <br/> |
|**otherCountryOrRegion** <br/> |国または地域の代替住所です。  <br/> |
|**otherState** <br/> |人の代替住所の都道府県です。  <br/> |
|**otherZip** <br/> |Zip または人の代替住所の郵便番号です。  <br/> |
|**電話** <br/> |担当者の主な連絡先の電話番号です。  <br/> |
|**pictureUrl** <br/> |人のプロフィールの画像の URL です。  <br/> |
|**関係** <br/> |ログオン中のユーザーにこの人の関係です。  <br/> |
|**学校** <br/> |人またはにする学校です。  <br/> |
|**スキル** <br/> |人の個人のスキルです。  <br/> |
|**state** <br/> |人の住所の都道府県です。  <br/> |
|**title** <br/> |ユーザーの名前を追加指定します。  <br/> |
|**ユーザー Id** <br/> |ソーシャル ネットワーク上のユーザーを識別する ID です。  <br/> |
|**webProfilePage** <br/> |ユーザーのプロファイルを含む web ページのアドレスです。  <br/> |
|**web サイト** <br/> |個人の web サイトです。  <br/> |
|**workPhone** <br/> |人の会社の電話番号です。  <br/> |
|**zip** <br/> |Zip コードまたはユーザーの住所の郵便番号です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [友人の XML の例](friends-xml-example.md)  
- [友人や活動を同期します。](synchronizing-friends-and-activities.md)  
- [機能のための XML](xml-for-capabilities.md) 
- [活動の XML](xml-for-activities.md)
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

