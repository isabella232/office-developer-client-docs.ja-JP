---
title: アクティビティフィード XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: 'このトピックの XML の例は、ソーシャルネットワークに対して ISocialSession2:: GetActivitiesEx メソッドを呼び出した後、Outlook Social Connector (.OSC) に返されるアクティビティフィード XML 文字列です。'
ms.openlocfilehash: bb8af45f25d8ee2897a3a01e2863466aeacec4e8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538327"
---
# <a name="activity-feed-xml-example"></a>アクティビティフィード XML の例

このトピックの XML の例は、ソーシャルネットワークに対して[ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを呼び出した後、Outlook Social CONNECTOR (.osc) に返されるアクティビティフィード XML 文字列です。 
  
この例は、次の4つのアクティビティを含む**Activityfeed** XML を示しています。各アクティビティは、 **activityfeed**要素で区切られ、表示用のテンプレートと一致します。 
  
- Melissa Macbeth によって、ソーシャルネットワーク上の**ownerID**が4667647であるプロファイル画像の更新。 このアクティビティでは、 **publisherVariable**、 **Listvariable**、および**ピクチャ変数**( **listvariable**で囲まれています) の3つのテンプレート変数を指定します。 これらの変数は、アクティビティフィードアイテムを発行したユーザー、および変更される画像の情報を指定します (picture**変数**の**name**、 **value**、 **alttext**、および**href**の子要素を使用)。
    
- Michael Affronti によって、ソーシャルネットワーク上の**ownerID**が5015012であるプロファイル画像の更新。 このアクティビティは、最後のアクティビティと同様に、 **publisherVariable**、 **listvariable**、および**ピクチャ変数**型の3つのテンプレート変数を指定します。 これらの変数は、アクティビティフィードアイテムを発行したユーザーと、更新する画像の情報を指定します。
    
- Affronti によって進捗の更新が行われ、最後のアクティビティとして5015012の同じ**ownerID**が表示されます。 このアクティビティは、type **publisherVariable**および**textvariable**の2つのテンプレート変数を指定します。 **publisherVariable**は、アクティビティフィードアイテムを発行したユーザーを指定し、 **textvariable**にはステータス行の**値**が含まれています。`is hiking on Mount Rainier this weekend!`
    
- マイケル Affronti によるブログ投稿。最後の2つのアクティビティと同じ**ownerID**が5015012に表示されます。 このアクティビティは、 **publisherVariable**および**linkvariable**型の2つのテンプレート変数を指定します。 **publisherVariable**は、アクティビティフィードアイテムを発行したユーザーを指定します。 **linkvariable**には、追加情報 ( **linkvariable**の**name**、 **text**、 **value**子要素で指定される) が含まれています。ブログ投稿について
    
4つの各アクティビティは、 **templates**要素で指定された3つのテンプレートのいずれかに一致する**templateID**値を指定します。 各テンプレートは独自の**Activitytemplatecontainer**要素に含まれています。これは、同じ**templateID**値を持つアクティビティを表示するためにも使用される**templateID**値で識別されます。 
  
この例で使用されている XML 要素の詳細な説明については、以下のトピックを参照してください。 
  
- [アクティビティフィードアイテムの XML の概要](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails 要素](activitydetails-element.md)
    
- [activityTemplateContainer 要素](activitytemplatecontainer-element.md)
    
- [テンプレート変数](template-variables.md)
    
## <a name="xml-example"></a>XML の例

次の例は、2つのプロファイル画像の更新、状態の更新、およびブログ投稿の4つのアクティビティの**Activityfeed** XML を示しています。 また、XML は、対応するアクティビティを表示するための3つのアクティビティ表示テンプレートも指定します。 
  
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

- [.OSC プロバイダーの XML の例](osc-provider-xml-examples.md)  
- [アクティビティの XML](xml-for-activities.md) 
- [機能 XML の例](capabilities-xml-example.md)  
- [Friends XML の例](friends-xml-example.md)
- [Outlook Social Connector プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)

