---
title: テンプレート変数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: (TemplateVariable 要素によって表されます) のテンプレート変数のインスタンスでは、アクティビティ フィード項目のアクティビティ テンプレートでのデータを指定します。
ms.openlocfilehash: 99f4c2de586447fb0361e528bcd33d62b79e0fb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804483"
---
# <a name="template-variables"></a>テンプレート変数

( **TemplateVariable**要素によって表されます) のテンプレート変数のインスタンスでは、アクティビティ フィード項目のアクティビティ テンプレートでのデータを指定します。 
  
アクティビティの例については、フィードの XML、[アクティビティ フィードの XML の例](activity-feed-xml-example.md)を参照してください。

次の表は、XML の対応する列挙値によって表される各サポートされているテンプレートの変数の種類を示しています。
  
|**テンプレート変数の型**|**説明**|
|:-----|:-----|
|**entityVariable** <br/> |ユーザー、グループ、またはです。  <br/> |
|**linkVariable** <br/> |リンクです。  <br/> |
|**listVariable** <br/> |オブジェクトのグループです。  <br/> |
|**pictureVariable** <br/> |画像です。  <br/> |
|**publisherVariable** <br/> |活動の出版社では、アイテムをフィードします。  <br/> |
|**textVariable** <br/> |テキストのブロックです。  <br/> |
   
テンプレート変数の各タイプには、その変数に関するデータを指定する要素が必要でした。 テンプレート変数の指定は次のとおりです。
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>リストのテンプレート変数

リスト内で、( **listVariable**および**リスト項目**の要素で区切られた) 次のように格納されているテンプレートの変数を指定できます。 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
**ListVariable**型のテンプレート変数は、オブジェクトのコンテナーです。 これは、コンマで区切られた (の種類のアイテム、 **linkVariable**または**textVariable** ) または ( **pictureVariable**型) の画像を含めることができます。 リストは、5 つのリンク アイテム、5 つのテキスト、または 5 つの画像を含むことができます。 
  
Outlook ソーシャル コネクタ (OSC) は、Windows のシステム ロケール] ボックスの一覧項目をリンクまたはテキストをローカライズします。
  
正しく解析して、アクティビティ フィードのアイテムに画像を表示、リスト内の画像を含める必要があります。 すべての画像は、高さ 52 ピクセルにサイズ変更されます。 画像の幅のサイズは変更されません。
  
## <a name="template-variable-elements"></a>テンプレートの可変要素

このセクションでは、テンプレート変数の種類ごとにサポートされる必須および省略可能な要素について説明します。
  
### <a name="entityvariable"></a>entityVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前です。 必須。  <br/> |
|**id** <br/> |ユーザーの一意の ID です。 必須。  <br/> |
|**nameHint** <br/> |フィードの項目に表示される名前です。 省略可能。  <br/> |
|**profileUrl** <br/> |として使用するハイパーリンクでは、フィードの項目では、人の名前の人の名前が存在する場合、ユーザーのプロファイルの URL です。 省略可能。  <br/> |
|**emailAddress** <br/> |Outlook で、このユーザーの連絡先情報を更新するために使用される電子メール アドレスです。 省略可能。  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前です。 必須。  <br/> |
|**value** <br/> |このリンクの URL です。 必須。  <br/> |
|**text** <br/> |URL 自体の代わりに表示するリンク テキストです。 省略可能。  <br/> |
   
### <a name="listvariable"></a>listVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前です。 必須。  <br/> |
|**リスト項目** <br/> |リスト内の項目のコンテナーです。 必須。  <br/> |
   
### <a name="picturevariable"></a>pictureVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前です。 必須。  <br/> |
|**value** <br/> |画像の URL です。 必須。  <br/> |
|**altText** <br/> |ユーザー補助と、ユーザーが画像上でマウス ポインターを移動するとに表示する代替テキスト。 省略可能。  <br/> |
|**href** <br/> |目的のターゲット**値**の要素によって指定された画像の URL でない場合、画像をクリックするとを使用するハイパーリンク。 省略可能。  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前です。 必須。  <br/> |
|**id** <br/> |ユーザーの一意の ID です。 必須。  <br/> |
|**nameHint** <br/> |フィードの項目に表示される名前です。 省略可能。  <br/> |
|**profileUrl** <br/> |として使用するハイパーリンクでは、フィードの項目では、人の名前の人の名前が存在する場合、ユーザーのプロファイルの URL です。 省略可能。  <br/> |
|**emailAddress** <br/> |Outlook で、このユーザーの連絡先情報を更新するために使用される電子メール アドレスです。 省略可能。  <br/> |
   
### <a name="textvariable"></a>textVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前です。 必須。  <br/> |
|**value** <br/> |表示するテキスト。 省略可能。  <br/> |
   
## <a name="see-also"></a>関連項目

- [フィード アイテムの活動項目の XML の概要](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails 要素](activitydetails-element.md)  
- [activityTemplateContainer 要素](activitytemplatecontainer-element.md)  
- [アクティビティを正しく表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)  
- [活動の XML](xml-for-activities.md)  
- [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

