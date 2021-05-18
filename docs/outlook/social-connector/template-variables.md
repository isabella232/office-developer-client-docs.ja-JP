---
title: テンプレート変数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: テンプレート変数のインスタンス (templateVariable 要素で表されます) は、アクティビティ テンプレート内のアクティビティ フィード アイテムのデータを指定します。
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404373"
---
# <a name="template-variables"></a>テンプレート変数

テンプレート変数のインスタンス **(templateVariable** 要素で表されます) は、アクティビティ テンプレート内のアクティビティ フィード アイテムのデータを指定します。 
  
アクティビティ フィード XML の例については、「アクティビティ フィード [XML の例」を参照してください](activity-feed-xml-example.md)。

次の表に、サポートされているテンプレート変数の種類を示します。各変数は、対応する XML 列挙値で表されます。
  
|**テンプレート変数の種類**|**説明**|
|:-----|:-----|
|**entityVariable** <br/> |人、グループ、または物。  <br/> |
|**linkVariable** <br/> |リンク。  <br/> |
|**listVariable** <br/> |オブジェクトのグループ。  <br/> |
|**pictureVariable** <br/> |画像です。  <br/> |
|**publisherVariable** <br/> |アクティビティ フィード アイテムの発行元。  <br/> |
|**textVariable** <br/> |テキストのブロック。  <br/> |
   
テンプレート変数の各種類には、その変数に関するデータを指定するために必要な要素があります。 テンプレート変数は次のように指定されます。
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>リスト テンプレート変数

リスト内に含まれるテンプレート変数 **(listVariable** 要素と **listItems** 要素で区切られた) を次のように指定できます。 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
**listVariable 型のテンプレート変数は**、オブジェクトのコンテナーです。 コンマで区切られた項目 **(linkVariable** または **textVariable 型** ) またはピクチャ **(pictureVariable** 型の) を含めることができます。 リストには、最大 5 つのリンク アイテム、5 つのテキスト アイテム、または 5 つの画像を含めることができます。 
  
Outlook Social Connector (OSC) は、Windows システム ロケールに従ってリンクまたはテキスト リスト アイテムをローカライズします。
  
アクティビティ フィード アイテム内の画像を正しく解析して表示するには、画像をリストに含める必要があります。 すべての画像のサイズは、高さ 52 ピクセルに変更されます。 画像の幅はサイズ変更されません。
  
## <a name="template-variable-elements"></a>テンプレート変数要素

このセクションでは、テンプレート変数の種類ごとにサポートされる必須要素と省略可能な要素について説明します。
  
### <a name="entityvariable"></a>entityVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須です。  <br/> |
|**id** <br/> |ユーザーの一意の ID。 必須です。  <br/> |
|**nameHint** <br/> |フィード アイテムに表示する名前。 オプション。  <br/> |
|**profileUrl** <br/> |ユーザーの名前が存在する場合、フィード アイテム内のユーザー名のハイパーリンクとして使用されるユーザーのプロファイルの URL。 オプション。  <br/> |
|**emailAddress** <br/> |Outlook でこのユーザーの連絡先情報を更新するために使用される電子メール アドレス。 オプション。  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須です。  <br/> |
|**value** <br/> |このリンクの URL。 必須です。  <br/> |
|**text** <br/> |URL 自体の代わりに表示するリンク テキスト。 オプション。  <br/> |
   
### <a name="listvariable"></a>listVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須です。  <br/> |
|**listItems** <br/> |リスト内のアイテムのコンテナー。 必須です。  <br/> |
   
### <a name="picturevariable"></a>pictureVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須です。  <br/> |
|**value** <br/> |画像の URL。 必須です。  <br/> |
|**altText** <br/> |ユーザー補助のために、およびユーザーが画像の上にマウス ポインターを移動するときに表示する代替テキスト。 オプション。  <br/> |
|**href** <br/> |目的のターゲットが value 要素で指定されたピクチャ URL ではない場合、ユーザーが画像をクリックするときに使用する **ハイパーリンク** 。 オプション。  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須です。  <br/> |
|**id** <br/> |ユーザーの一意の ID。 必須です。  <br/> |
|**nameHint** <br/> |フィード アイテムに表示する名前。 オプション。  <br/> |
|**profileUrl** <br/> |ユーザーの名前が存在する場合、フィード アイテム内のユーザー名のハイパーリンクとして使用されるユーザーのプロファイルの URL。 オプション。  <br/> |
|**emailAddress** <br/> |Outlook でこのユーザーの連絡先情報を更新するために使用される電子メール アドレス。 オプション。  <br/> |
   
### <a name="textvariable"></a>textVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須です。  <br/> |
|**value** <br/> |表示するテキスト。 オプション。  <br/> |
   
## <a name="see-also"></a>関連項目

- [アクティビティ フィード アイテムの XML の概要](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails 要素](activitydetails-element.md)  
- [activityTemplateContainer 要素](activitytemplatecontainer-element.md)  
- [アクティビティを適切に表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)  
- [アクティビティの XML](xml-for-activities.md)  
- [Outlook ソーシャル コネクタ プロバイダー XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [OSC XML スキーマを使用したプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

