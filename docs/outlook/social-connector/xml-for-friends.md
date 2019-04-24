---
title: 友だち用 XML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: Microsoft Outlook Social Connector (.osc) プロバイダ XML スキーマのフレンド要素を使用すると、.osc プロバイダーは、ソーシャルネットワーク内の Outlook ユーザーに関連付けられた人物のリストに関する情報を指定できます。
ms.openlocfilehash: df3bf03c5fd1dcdac3096411bc60bcb1eeec661e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361160"
---
# <a name="xml-for-friends"></a>友だち用 XML

Microsoft Outlook Social Connector (.osc) プロバイダ XML スキーマの**フレンド**要素を使用すると、.osc プロバイダーは、ソーシャルネットワーク内の Outlook ユーザーに関連付けられた人物のリストに関する情報を指定できます。 .osc プロバイダーがキャッシュ同期をサポートしている場合、このユーザーの一覧には、ソーシャルネットワーク上の Outlook ユーザーのフレンドのみが含まれます。 .osc がオンデマンドまたはハイブリッド同期をサポートしている場合、このリストには、Outlook ユーザーの友人と友人以外の両方が含まれることがあります。 

リスト内の各ユーザーは、XML スキーマで**person**要素として表され、名、姓、電子メールアドレスなどの詳細をサポートします。 .osc プロバイダーは、ユーザーがソーシャルネットワークからフレンド情報を同期する方法にかかわらず、 **friends**要素と**person**要素を使用します。 **person**の子要素は、outlook 連絡先の一部のプロパティに似ているため、ソーシャルネットワークがキャッシュまたはハイブリッドをサポートしている場合は、ソーシャルネットワークに固有の outlook 連絡先フォルダーに友人を格納することが容易になります。Outlook の連絡先フォルダーへのフレンドの同期。 

## <a name="example-scenarios"></a>シナリオ例

次の例は、.osc プロバイダーが実装し、.osc がフレンド情報を取得するための、.osc プロバイダーの機能拡張 API 呼び出しを示しています。 情報は、.osc プロバイダ xml スキーマに準拠する xml 文字列で表されます。
  
friends xml の例については、「 [friends xml の例](friends-xml-example.md)」を参照してください。 フレンドの同期の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。

### <a name="scenario-1-get-a-list-of-friends"></a>シナリオ 1: 友人のリストを取得する

シナリオ 1-.osc 友人のリストと、各フレンドの[isocialperson](isocialpersoniunknown.md)オブジェクトおよび画像を取得します。 
    
1. ソーシャルネットワークサイトからのフレンドの表示をサポートし、.osc がフレンド情報をキャッシュできるようにする .osc プロバイダーは、 **getfriends**要素と**cacheFriends**要素を使用して、.osc に対して、その子要素**であるを示します。capabilities**要素。 
    
2. また、.osc プロバイダーは、 [iGetFriendsAndColleagues alprovider:: getcapabilities](isocialprovider-getcapabilities.md)、 [i alsession:: getcapabilities](isocialsession-getperson.md)、 [i alperson::](isocialperson-getfriendsandcolleagues.md)::: [getcapabilities](isocialperson-getpicture.md)メソッドを実装します。 
    
3. .osc は**icacheFriends alprovider:: getcapabilities**を呼び出して、次の要素の値を確認します。 **getcapabilities**は、.osc プロバイダーがソーシャルネットワークからの友人の表示をサポートしていることを確認し、 **** を実行してプロバイダーが機能していることを確認します。フレンドのキャッシュをサポートします。 
    
4. .osc は、 **iな alsession:: getperson**を呼び出して、Outlook ユーザーの**isocialsession**オブジェクトを取得します。 
    
5. .osc は**iGetFriendsAndColleagues alperson::** を呼び出して、_個人コレクション_のパラメーター文字列で返された Outlook ユーザーのフレンドリストを取得します。 _個人コレクション_文字列は、xml スキーマの**friends**要素の xml スキーマ定義に準拠しています。 
    
6. _個人コレクション_XML 文字列の各フレンドについて、.osc は、そのフレンドの**isocialsession**オブジェクトを取得するために、**次**のように、 **userID**要素の値を取得します。 
    
7. **個人コレクション**XML 文字列内の各フレンドについて、.osc は i指定された[alperson:: getpicture](isocialperson-getpicture.md)を呼び出して、そのフレンドの画像リソースを取得します。 
    
   .osc は、その友人のアクティビティと詳細 (たとえば、電子メールアドレス) を取得するために、 **iコード alperson**オブジェクトに対してさらに呼び出しを行うことができます。 
    
### <a name="scenario-2-synchronize-friends"></a>シナリオ 2: 友人を同期する 

シナリオ 2: .osc は、友人を動的に同期します。
    
1. 友人および友人以外のオンデマンド同期をサポートする .osc プロバイダーは、 **getfriends**要素と**dynamicContactsLookup**要素を使用して、.osc に対してを示します。 .osc プロバイダーは、 **hashfunction**要素も設定します。 3つすべての要素は、**機能**の子要素です。 
    
2. .osc プロバイダーは、 [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)メソッドも実装します。 
    
3. .osc は**idynamicContactsLookup alprovider:: getcapabilities**を呼び出して、.osc プロバイダーが友人や友人以外のフレンドとオンデマンドの同期をサポートしていることを確認するために、 **getcapabilities**および**** の値をチェックします。 また、.osc は、.osc プロバイダーがサポートする**hashfunction**の値をメモします。 
    
4. [人] ウィンドウに表示される各ユーザーについて、.osc は、ユーザーの電子メールアドレスを収集し、 **hashfunction**で指定されたハッシュ関数を使用してそれを暗号化します。 これにより、 **hashedAddresses**要素の xml スキーマ定義に準拠した xml 文字列が形成されます。 
    
5. .osc は**ISocialSession2:: GetPeopleDetails**を呼び出して、この XML 文字列を_個人住所_パラメーターとして提供します。これを使用すると、個人の更新された詳細を個人の_コレクション_パラメーターで動的に取得できます。 _個人コレクション_パラメータ文字列は、xml スキーマの**friends**要素の xml スキーマ定義に準拠しています。 

## <a name="parent-and-child-elements"></a>親要素と子要素

次に、**フレンド**スキーマの2つのトップレベル要素を示します。 
  
|**要素**|**説明**|
|:-----|:-----|
|**待ち** <br/> |**person**要素のリストのルート要素を表します。 **iGetFriendsAndColleagues**、 [i alsession:: findperson](isocialsession-findperson.md)、および**ISocialSession2:: GetPeopleDetails**は、**フレンド**要素のスキーマ定義に準拠した XML 文字列を返します。  <br/> |
|**人物** <br/> |**person**要素のリスト内の1人のユーザーを表します。 [i指定 alperson:: getdetails](isocialperson-getdetails.md)メソッドは、 **person**要素のスキーマ定義に準拠した XML 文字列を返します。  <br/> |
   
次の表では、.osc プロバイダ XML スキーマの**person**要素の各子要素について説明します。 
  
必要な要素やオプションの要素を含む、.osc プロバイダ XML スキーマの完全な定義については、「 [Outlook Social Connector プロバイダーの xml スキーマ](outlook-social-connector-provider-xml-schema.md)」を参照してください。
  
|**要素**|**説明**|
|:-----|:-----|
|**address** <br/> |個人の住所 (物理的な番地)。  <br/> |
|**記念** <br/> |その人物に対するイベントの記念日。  <br/> |
|**: askmeabout** <br/> |ユーザーの関心事項または専門知識。  <br/> |
|**birthday** <br/> |その人物の出生日。  <br/> |
|**businessAddress** <br/> |個人の職場の住所 (物理的な番地)。  <br/> |
|**businesscity** <br/> |ユーザーの職場の市区町村。  <br/> |
|**businessCountryOrRegion** <br/> |個人の職場の国または地域。  <br/> |
|**businessstate** <br/> |個人の職場の都道府県。  <br/> |
|**businesszip** <br/> |個人の職場の郵便番号。  <br/> |
|**セル** <br/> |個人の携帯電話番号。  <br/> |
|**市街** <br/> |個人の住所の市町村。  <br/> |
|**company** <br/> |個人に関連付けられている会社の名前。  <br/> |
|**countryOrRegion** <br/> |ユーザーの物理的な住所の国または地域。  <br/> |
|**creationTime** <br/> |ソーシャルネットワーク上の個人のプロファイルの作成日時。  <br/> |
|**emailAddress** <br/> |ユーザーのプライマリ電子メールアドレス。  <br/> |
|**emailAddress2** <br/> |個人の第2メールアドレス。  <br/> |
|**emailAddress3** <br/> |個人の第3の電子メールアドレス。  <br/> |
|**expirationTime** <br/> |ソーシャルネットワーク上のユーザーのプロファイルデータの有効期限が切れる時刻。  <br/> |
|**fileAs** <br/> |ユーザーが Outlook の連絡先ファイルの連絡先としてファイリングされる文字列。  <br/> |
|**firstName** <br/> |個人の名前または指定された名前。  <br/> |
|**friendStatus** <br/> |ソーシャルネットワークにログオンしているユーザーを持つこの人物のフレンド状態。 **friend**、 **nonfriend**、 **pending**、 **pendingin**、 **pendingin**のいずれかの値であることが必要です。  <br/> |
|**fullName** <br/> |個人の氏名。  <br/> |
|**女性** <br/> |人物の性別。 次のいずれかの値である必要があります。**男性**、**女性**、**未指定**。  <br/> |
|**homePhone** <br/> |個人の自宅の電話番号。  <br/> |
|**index** <br/> |**ISocialSession2:: GetPeopleDetails**メソッドの呼び出しに渡される個人のハッシュ化されたアドレスの場所を個人の_アドレス_文字列パラメーターで指定します。 また、 **GetPeopleDetails**によって**** 返される個人の_コレクション_文字列の個人 XML を示します。  <br/> |
|**あらゆる** <br/> |その人物が従事している業界。  <br/> |
|**interests** <br/> |個人の趣味または趣味。  <br/> |
|**lastModificationTime** <br/> |ユーザーのプロファイルがソーシャルネットワーク上で最後に変更された時刻。  <br/> |
|**lastName** <br/> |ユーザーの姓または姓。  <br/> |
|**location** <br/> |ユーザーの場所。  <br/> |
|**ニックネーム** <br/> |個人の短い名前または発明された名前。  <br/> |
|**otherAddress** <br/> |個人の代替住所。  <br/> |
|**othercity** <br/> |個人の代替住所の市区町村。  <br/> |
|**otherCountryOrRegion** <br/> |個人の代替住所の国または地域。  <br/> |
|**otherstate** <br/> |個人の代替住所の都道府県。  <br/> |
|**otherzip** <br/> |個人の代替住所の郵便番号。  <br/> |
|**代わり** <br/> |個人の主要な連絡先の電話番号。  <br/> |
|**pictureUrl** <br/> |個人のプロフィール画像の URL。  <br/> |
|**対** <br/> |この人物とログオンしているユーザーとの関係。  <br/> |
|**学校** <br/> |その人物が参加または移行した教育機関。  <br/> |
|**skills** <br/> |個人の個人スキル。  <br/> |
|**state** <br/> |個人の現物住所の都道府県。  <br/> |
|**title** <br/> |ユーザーの名前に追加された指定。  <br/> |
|**userID** <br/> |ソーシャルネットワーク上の人物を識別する ID。  <br/> |
|**webprofilepage** <br/> |個人のプロファイルを含む web ページアドレス。  <br/> |
|<b0><a1/&gt;</b0> <br/> |個人の web サイト。  <br/> |
|**workPhone** <br/> |個人の会社の電話番号。  <br/> |
|**国内** <br/> |個人の住所の郵便番号です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [Friends XML の例](friends-xml-example.md)  
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)  
- [機能の XML](xml-for-capabilities.md) 
- [アクティビティの XML](xml-for-activities.md)
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)

