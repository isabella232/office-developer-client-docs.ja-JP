---
title: アクティビティ フィード XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: このトピックの XML 例は、ソーシャル ネットワークの ISocialSession2::GetActivitiesEx メソッドを呼び出した後、Outlook Social Connector (OSC) に返されるアクティビティ フィード XML 文字列です。
ms.openlocfilehash: bb8af45f25d8ee2897a3a01e2863466aeacec4e8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538327"
---
# <a name="activity-feed-xml-example"></a>アクティビティ フィード XML の例

このトピックの XML 例は、ソーシャル ネットワークの[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを呼び出した後、Outlook Social Connector (OSC) に返されるアクティビティ フィード XML 文字列です。 
  
この例では **、activityDetails** 要素で区切られた次の 4 つのアクティビティを含む **activityFeed** XML を示し、表示目的でテンプレートと一致します。 
  
- Melissa Macbeth によるプロファイル画像の更新。そのソーシャル ネットワーク上の **ownerID** は 4667647 です。 このアクティビティは **、publisherVariable、listVariable、****および** **pictureVariable (listVariable** で囲まれた) の 3 つのテンプレート変数 **を指定します**。 これらの変数は、アクティビティ フィード アイテムを公開したユーザーと、更新する図の情報を指定します **(pictureVariable** の名前、**値****、altText、****および href** 子要素を使用します)。 
    
- ソーシャル ネットワーク上の **ownerID** が 5015012 である Michael Affronti によるプロファイル画像の更新。 最後のアクティビティと同様に、このアクティビティは **publisherVariable、listVariable、pictureVariable** の 3 つのテンプレート変数 **を指定します**。  これらの変数は、アクティビティ フィード アイテムを公開したユーザーと、更新する画像の情報を指定します。
    
- Michael Affronti による状態の更新で、最後のアクティビティと同じ **ownerID** 5015012 が表示されます。 このアクティビティは、publisherVariable 型と **textVariable 型の 2** つの **テンプレート変数を指定します**。 **publisherVariable は** 、アクティビティ フィード アイテムを公開したユーザーを指定し **、textVariable には** 状態行 **の** 値が含まれます  `is hiking on Mount Rainier this weekend!`
    
- Michael Affronti のブログ投稿で、最後の 2 つのアクティビティと同じ **ownerID** 5015012 が表示されます。 このアクティビティは、publisherVariable 型と **linkVariable 型の 2** つの **テンプレート変数を指定します**。 **publisherVariable は**、アクティビティ フィード アイテムを公開したユーザーを指定し **、linkVariable** にはブログ投稿に関する詳細な情報 **(linkVariable** の名前、テキスト、および値の子要素で指定) が含まれます。 
    
4 つのアクティビティのそれぞれは **templateID** 値を指定します。これは templates 要素で指定された 3 つのテンプレートの 1 つと **一致** します。 各テンプレートは、独自の **activityTemplateContainer** 要素に含め、同じ **templateID** 値を持つアクティビティの表示にも使用される **templateID** 値で識別されます。 
  
この例で使用される XML 要素の詳細については、次のトピックを参照してください。 
  
- [アクティビティ フィード アイテムの XML の概要](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails 要素](activitydetails-element.md)
    
- [activityTemplateContainer 要素](activitytemplatecontainer-element.md)
    
- [テンプレート変数](template-variables.md)
    
## <a name="xml-example"></a>XML の例

次の例は **、2 つの** プロファイル画像の更新、状態の更新、およびブログ投稿の 4 つのアクティビティの activityFeed XML を示しています。 XML では、対応するアクティビティを表示するための 3 つのアクティビティ表示テンプレートも指定します。 
  
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
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
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
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
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
          <profileUrl>https://www.contoso.com</profileUrl>
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
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>https://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
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
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a>関連項目

- [OSC プロバイダー XML の例](osc-provider-xml-examples.md)  
- [アクティビティの XML](xml-for-activities.md) 
- [機能 XML の例](capabilities-xml-example.md)  
- [Friends XML の例](friends-xml-example.md)
- [Outlookソーシャル コネクタ プロバイダー XML スキーマ](outlook-social-connector-provider-xml-schema.md)

