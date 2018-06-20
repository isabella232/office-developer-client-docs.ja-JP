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
# <a name="activity-feed-xml-example"></a><span data-ttu-id="b12cb-103">アクティビティ フィードの XML の例</span><span class="sxs-lookup"><span data-stu-id="b12cb-103">Activity Feed XML Example</span></span>

<span data-ttu-id="b12cb-104">XML の例をこのトピックでは、アクティビティ フィードのソーシャル ネットワークの[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドが呼び出された後に、Outlook ソーシャル コネクタ (OSC) が返される XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="b12cb-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="b12cb-105">**ActivityFeed**次の 4 つのアクティビティが含まれている XML の例は、表示目的で**activityDetails**要素で区切られたそれぞれのテンプレートに一致します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="b12cb-106">Melissa Macbeth、ソーシャル ネットワーク上の**ownerID**が 4667647 では、プロフィールの画像を更新します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="b12cb-107">このアクティビティでは、型**publisherVariable**、 **listVariable**、 **pictureVariable** (これは**listVariable**で囲まれている) の 3 つのテンプレート変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="b12cb-108">これらの変数は、アクティビティ フィードのアイテムとを使用して**pictureVariable**の子要素**の名前**、**値**、 **altText**、および**href** ) を更新する図の情報を公開したユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="b12cb-109">マイケル ・ Affronti の 5015012 は、ソーシャル ネットワーク上の**ownerID**がプロフィールの画像を更新します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="b12cb-110">最後のアクティビティと同様に、このアクティビティは、型**publisherVariable**、 **listVariable**、 **pictureVariable**の 3 つのテンプレート変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="b12cb-111">これらの変数は、アクティビティ フィードのアイテムを更新する図の情報を公開したユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="b12cb-112">同じの**ownerID** 5015012 の最後のアクティビティとして表示されている、マイケル ・ Affronti で状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="b12cb-113">このアクティビティでは、型の**publisherVariable**と**textVariable**の 2 つのテンプレート変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="b12cb-114">**publisherVariable**は、アクティビティ フィードのアイテムを発行した人物を指定し、 **textVariable**には、ステータス行の**値**が含まれています。`is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="b12cb-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="b12cb-115">同じの**ownerID** 5015012 の最後の 2 つの活動項目として表示されている、マイケル ・ Affronti でのブログ投稿です。</span><span class="sxs-lookup"><span data-stu-id="b12cb-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="b12cb-116">このアクティビティでは、型の**publisherVariable**と**linkVariable**の 2 つのテンプレート変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="b12cb-117">活動を公開したユーザーのフィードのアイテム、および**linkVariable**が含まれています詳細についてには ( **linkVariable**の**名前**、**テキスト**、および**値**の子要素で指定) を指定する**publisherVariable**に関するブログの投稿です。</span><span class="sxs-lookup"><span data-stu-id="b12cb-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="b12cb-118">それぞれの 4 つのアクティビティは、**テンプレート**要素で指定された 3 つのテンプレートのいずれかに一致する、**テンプレート Id**の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="b12cb-119">同じ**テンプレート Id**の値を持つアクティビティを表示するために使用される**テンプレート Id**値によって識別される、独自の**activityTemplateContainer**要素には、各テンプレート。</span><span class="sxs-lookup"><span data-stu-id="b12cb-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="b12cb-120">この例で使用する XML 要素の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b12cb-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="b12cb-121">フィード アイテムの活動項目の XML の概要</span><span class="sxs-lookup"><span data-stu-id="b12cb-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="b12cb-122">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="b12cb-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="b12cb-123">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="b12cb-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="b12cb-124">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="b12cb-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="b12cb-125">XML の例</span><span class="sxs-lookup"><span data-stu-id="b12cb-125">XML example</span></span>

<span data-ttu-id="b12cb-126">次の例では、 **activityFeed**の 4 つのアクティビティの XML: 2 つのプロファイル画像の更新、進捗状況の更新、およびブログの投稿です。</span><span class="sxs-lookup"><span data-stu-id="b12cb-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="b12cb-127">XML では、対応するアクティビティを表示するための 3 つのアクティビティの表示テンプレートを指定します。</span><span class="sxs-lookup"><span data-stu-id="b12cb-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="b12cb-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b12cb-128">See also</span></span>

- [<span data-ttu-id="b12cb-129">OSC プロバイダーの XML の例</span><span class="sxs-lookup"><span data-stu-id="b12cb-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="b12cb-130">活動の XML</span><span class="sxs-lookup"><span data-stu-id="b12cb-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="b12cb-131">機能の XML の例</span><span class="sxs-lookup"><span data-stu-id="b12cb-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="b12cb-132">友人の XML の例</span><span class="sxs-lookup"><span data-stu-id="b12cb-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="b12cb-133">Outlook ソーシャル コネクタ プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="b12cb-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

