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
# <a name="activity-feed-xml-example"></a><span data-ttu-id="62dbe-103">アクティビティフィード XML の例</span><span class="sxs-lookup"><span data-stu-id="62dbe-103">Activity Feed XML Example</span></span>

<span data-ttu-id="62dbe-104">このトピックの XML の例は、ソーシャルネットワークに対して[ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを呼び出した後、Outlook Social CONNECTOR (.osc) に返されるアクティビティフィード XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="62dbe-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="62dbe-105">この例は、次の4つのアクティビティを含む**Activityfeed** XML を示しています。各アクティビティは、 **activityfeed**要素で区切られ、表示用のテンプレートと一致します。</span><span class="sxs-lookup"><span data-stu-id="62dbe-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="62dbe-106">Melissa Macbeth によって、ソーシャルネットワーク上の**ownerID**が4667647であるプロファイル画像の更新。</span><span class="sxs-lookup"><span data-stu-id="62dbe-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="62dbe-107">このアクティビティでは、 **publisherVariable**、 **Listvariable**、および**ピクチャ変数**( **listvariable**で囲まれています) の3つのテンプレート変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="62dbe-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="62dbe-108">これらの変数は、アクティビティフィードアイテムを発行したユーザー、および変更される画像の情報を指定します (picture**変数**の**name**、 **value**、 **alttext**、および**href**の子要素を使用)。</span><span class="sxs-lookup"><span data-stu-id="62dbe-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="62dbe-109">Michael Affronti によって、ソーシャルネットワーク上の**ownerID**が5015012であるプロファイル画像の更新。</span><span class="sxs-lookup"><span data-stu-id="62dbe-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="62dbe-110">このアクティビティは、最後のアクティビティと同様に、 **publisherVariable**、 **listvariable**、および**ピクチャ変数**型の3つのテンプレート変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="62dbe-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="62dbe-111">これらの変数は、アクティビティフィードアイテムを発行したユーザーと、更新する画像の情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="62dbe-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="62dbe-112">Affronti によって進捗の更新が行われ、最後のアクティビティとして5015012の同じ**ownerID**が表示されます。</span><span class="sxs-lookup"><span data-stu-id="62dbe-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="62dbe-113">このアクティビティは、type **publisherVariable**および**textvariable**の2つのテンプレート変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="62dbe-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="62dbe-114">**publisherVariable**は、アクティビティフィードアイテムを発行したユーザーを指定し、 **textvariable**にはステータス行の**値**が含まれています。`is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="62dbe-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="62dbe-115">マイケル Affronti によるブログ投稿。最後の2つのアクティビティと同じ**ownerID**が5015012に表示されます。</span><span class="sxs-lookup"><span data-stu-id="62dbe-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="62dbe-116">このアクティビティは、 **publisherVariable**および**linkvariable**型の2つのテンプレート変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="62dbe-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="62dbe-117">**publisherVariable**は、アクティビティフィードアイテムを発行したユーザーを指定します。 **linkvariable**には、追加情報 ( **linkvariable**の**name**、 **text**、 **value**子要素で指定される) が含まれています。ブログ投稿について</span><span class="sxs-lookup"><span data-stu-id="62dbe-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="62dbe-118">4つの各アクティビティは、 **templates**要素で指定された3つのテンプレートのいずれかに一致する**templateID**値を指定します。</span><span class="sxs-lookup"><span data-stu-id="62dbe-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="62dbe-119">各テンプレートは独自の**Activitytemplatecontainer**要素に含まれています。これは、同じ**templateID**値を持つアクティビティを表示するためにも使用される**templateID**値で識別されます。</span><span class="sxs-lookup"><span data-stu-id="62dbe-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="62dbe-120">この例で使用されている XML 要素の詳細な説明については、以下のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="62dbe-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="62dbe-121">アクティビティフィードアイテムの XML の概要</span><span class="sxs-lookup"><span data-stu-id="62dbe-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="62dbe-122">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="62dbe-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="62dbe-123">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="62dbe-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="62dbe-124">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="62dbe-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="62dbe-125">XML の例</span><span class="sxs-lookup"><span data-stu-id="62dbe-125">XML example</span></span>

<span data-ttu-id="62dbe-126">次の例は、2つのプロファイル画像の更新、状態の更新、およびブログ投稿の4つのアクティビティの**Activityfeed** XML を示しています。</span><span class="sxs-lookup"><span data-stu-id="62dbe-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="62dbe-127">また、XML は、対応するアクティビティを表示するための3つのアクティビティ表示テンプレートも指定します。</span><span class="sxs-lookup"><span data-stu-id="62dbe-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="62dbe-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="62dbe-128">See also</span></span>

- [<span data-ttu-id="62dbe-129">.OSC プロバイダーの XML の例</span><span class="sxs-lookup"><span data-stu-id="62dbe-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="62dbe-130">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="62dbe-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="62dbe-131">機能 XML の例</span><span class="sxs-lookup"><span data-stu-id="62dbe-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="62dbe-132">Friends XML の例</span><span class="sxs-lookup"><span data-stu-id="62dbe-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="62dbe-133">Outlook Social Connector プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="62dbe-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

