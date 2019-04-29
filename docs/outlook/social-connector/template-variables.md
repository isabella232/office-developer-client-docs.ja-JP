---
title: テンプレート変数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: テンプレート変数のインスタンス (templateVariable 要素で表されます) は、アクティビティテンプレート内のアクティビティフィードアイテムのデータを指定します。
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404373"
---
# <a name="template-variables"></a>テンプレート変数

テンプレート変数のインスタンス ( **templateVariable**要素で表されます) は、アクティビティテンプレート内のアクティビティフィードアイテムのデータを指定します。 
  
アクティビティフィード xml の例については、「[アクティビティフィード xml の例](activity-feed-xml-example.md)」を参照してください。

次の表に、対応する XML 列挙値で表される、サポートされるテンプレート変数の種類を示します。
  
|**テンプレート変数の種類**|**説明**|
|:-----|:-----|
|**entityvariable** <br/> |個人、グループ、または事柄。  <br/> |
|**linkvariable** <br/> |リンク。  <br/> |
|**listvariable** <br/> |オブジェクトのグループ。  <br/> |
|**ピクチャ変数** <br/> |画像です。  <br/> |
|**publisherVariable** <br/> |アクティビティフィードアイテムの発行元。  <br/> |
|**textvariable** <br/> |テキストのブロック。  <br/> |
   
各種類のテンプレート変数には、その変数に関するデータを指定するために必要な要素があります。 テンプレート変数は次のように指定されます。
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>リストテンプレート変数

リスト内に含まれるテンプレート変数 ( **listvariable**および**listItems**要素で区切られたもの) を次のように指定できます。 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
**listvariable**型のテンプレート変数は、オブジェクトのコンテナーです。 このオブジェクトには、( **linkvariable**または**textvariable**型の) (または、図の**変数**型の) コンマ区切りのアイテムを含めることができます。 リストには最大5つのリンク項目、5つのテキスト項目、または5つの画像を含めることができます。 
  
Outlook Social Connector (.osc) は、Windows システムロケールに従って、リンクまたはテキストリストアイテムをローカライズします。
  
アクティビティフィードアイテムで画像を正しく解析して表示するには、画像をリストに含める必要があります。 すべての図の高さを52ピクセルに変更します。 図の幅は変更されません。
  
## <a name="template-variable-elements"></a>テンプレート変数要素

このセクションでは、テンプレート変数の種類ごとに、必要な要素とオプションの要素について説明します。
  
### <a name="entityvariable"></a>entityvariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須。  <br/> |
|**id** <br/> |ユーザーの一意の ID。 必須。  <br/> |
|**namehint** <br/> |フィードアイテムに表示する名前を指定します。 省略可能です。  <br/> |
|**profileurl** <br/> |ユーザーの名前が存在する場合に、フィードアイテムでのユーザー名のハイパーリンクとして使用される個人のプロファイルの URL。 省略可能です。  <br/> |
|**emailAddress** <br/> |このユーザーの連絡先情報を Outlook で更新するために使用される電子メールアドレス。 省略可能です。  <br/> |
   
### <a name="linkvariable"></a>linkvariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須。  <br/> |
|**value** <br/> |このリンクの URL。 必須。  <br/> |
|**text** <br/> |URL 自体の代わりに表示するリンクテキスト。 省略可能です。  <br/> |
   
### <a name="listvariable"></a>listvariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須。  <br/> |
|**listItems** <br/> |リスト内のアイテムのコンテナー。 必須。  <br/> |
   
### <a name="picturevariable"></a>ピクチャ変数

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須。  <br/> |
|**value** <br/> |図の URL を示します。 必須。  <br/> |
|**alttext** <br/> |ユーザー補助のために表示する代替テキスト、およびユーザーがマウスポインターを画像の上に移動したとき。 省略可能です。  <br/> |
|**href** <br/> |目的のターゲットが**value**要素で指定された画像の URL ではない場合に、ユーザーがピクチャをクリックしたときに使用するハイパーリンク。 省略可能です。  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須。  <br/> |
|**id** <br/> |ユーザーの一意の ID。 必須。  <br/> |
|**namehint** <br/> |フィードアイテムに表示する名前を指定します。 省略可能です。  <br/> |
|**profileurl** <br/> |ユーザーの名前が存在する場合に、フィードアイテムでのユーザー名のハイパーリンクとして使用される個人のプロファイルの URL。 省略可能です。  <br/> |
|**emailAddress** <br/> |このユーザーの連絡先情報を Outlook で更新するために使用される電子メールアドレス。 省略可能です。  <br/> |
   
### <a name="textvariable"></a>textvariable

|**要素**|**説明**|
|:-----|:-----|
|**name** <br/> |変数の名前。 必須。  <br/> |
|**value** <br/> |表示するテキストを入力します。 省略可能です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [アクティビティフィードアイテムの XML の概要](overview-of-xml-for-an-activity-feed-item.md)  
- [activitydetails 要素](activitydetails-element.md)  
- [activitytemplatecontainer 要素](activitytemplatecontainer-element.md)  
- [アクティビティを適切に表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)  
- [アクティビティの XML](xml-for-activities.md)  
- [Outlook Social Connector プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)

