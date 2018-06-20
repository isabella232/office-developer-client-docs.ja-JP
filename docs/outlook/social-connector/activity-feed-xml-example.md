---
title: アクティビティ フィードの XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: このトピックの例では XML では、アクティビティ フィードのソーシャル ネットワークの ISocialSession2::GetActivitiesEx メソッドが呼び出された後に、Outlook ソーシャル コネクタ (OSC) が返される XML 文字列です。
ms.openlocfilehash: ab27ddfad5044994a19bb32759994a0e98c39ae6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804324"
---
# <a name="activity-feed-xml-example"></a>アクティビティ フィードの XML の例

XML の例をこのトピックでは、アクティビティ フィードのソーシャル ネットワークの[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドが呼び出された後に、Outlook ソーシャル コネクタ (OSC) が返される XML 文字列です。 
  
**ActivityFeed**次の 4 つのアクティビティが含まれている XML の例は、表示目的で**activityDetails**要素で区切られたそれぞれのテンプレートに一致します。 
  
- Melissa Macbeth、ソーシャル ネットワーク上の**ownerID**が 4667647 では、プロフィールの画像を更新します。 このアクティビティでは、型**publisherVariable**、 **listVariable**、 **pictureVariable** (これは**listVariable**で囲まれている) の 3 つのテンプレート変数を指定します。 これらの変数は、アクティビティ フィードのアイテムとを使用して**pictureVariable**の子要素**の名前**、**値**、 **altText**、および**href** ) を更新する図の情報を公開したユーザーを指定します。
    
- マイケル ・ Affronti の 5015012 は、ソーシャル ネットワーク上の**ownerID**がプロフィールの画像を更新します。 最後のアクティビティと同様に、このアクティビティは、型**publisherVariable**、 **listVariable**、 **pictureVariable**の 3 つのテンプレート変数を指定します。 これらの変数は、アクティビティ フィードのアイテムを更新する図の情報を公開したユーザーを指定します。
    
- 同じの**ownerID** 5015012 の最後のアクティビティとして表示されている、マイケル ・ Affronti で状態を更新します。 このアクティビティでは、型の**publisherVariable**と**textVariable**の 2 つのテンプレート変数を指定します。 **publisherVariable**は、アクティビティ フィードのアイテムを発行した人物を指定し、 **textVariable**には、ステータス行の**値**が含まれています。`is hiking on Mount Rainier this weekend!`
    
- 同じの**ownerID** 5015012 の最後の 2 つの活動項目として表示されている、マイケル ・ Affronti でのブログ投稿です。 このアクティビティでは、型の**publisherVariable**と**linkVariable**の 2 つのテンプレート変数を指定します。 活動を公開したユーザーのフィードのアイテム、および**linkVariable**が含まれています詳細についてには ( **linkVariable**の**名前**、**テキスト**、および**値**の子要素で指定) を指定する**publisherVariable**に関するブログの投稿です。
    
それぞれの 4 つのアクティビティは、**テンプレート**要素で指定された 3 つのテンプレートのいずれかに一致する、**テンプレート Id**の値を指定します。 同じ**テンプレート Id**の値を持つアクティビティを表示するために使用される**テンプレート Id**値によって識別される、独自の**activityTemplateContainer**要素には、各テンプレート。 
  
この例で使用する XML 要素の詳細については、次のトピックを参照してください。 
  
- [フィード アイテムの活動項目の XML の概要](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails 要素](activitydetails-element.md)
    
- [activityTemplateContainer 要素](activitytemplatecontainer-element.md)
    
- [テンプレート変数](template-variables.md)
    
## <a name="xml-example"></a>XML の例

次の例では、 **activityFeed**の 4 つのアクティビティの XML: 2 つのプロファイル画像の更新、進捗状況の更新、およびブログの投稿です。 XML では、対応するアクティビティを表示するための 3 つのアクティビティの表示テンプレートを指定します。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <network>Contoso</network>
  <activities>
    <activityDetails>
      <ownerID>4667647</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a31</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-05T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>4667647</id>
          <nameHint>Melissa Macbeth</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a32</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-08T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a38</objectID>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <publishDate>2010-03-08T18:30:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com</profileUrl>
        </templateVariable>
        <templateVariable type="textVariable">
          <name>statusText</name>
          <value>is hiking on Mount Rainier this weekend!</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a39</objectID>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <publishDate>2010-03-04T15:00:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>http://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
  </activities>
  <templates>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <activityTemplate>
        <type>Photo</type>
        <title>{publisher:Publisher} has a new profile photo: </title>
        <data>{list:ProfilePhoto({picture:Photo})}</data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a>関連項目

- [OSC プロバイダーの XML の例](osc-provider-xml-examples.md)  
- [活動の XML](xml-for-activities.md) 
- [機能の XML の例](capabilities-xml-example.md)  
- [友人の XML の例](friends-xml-example.md)
- [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)

