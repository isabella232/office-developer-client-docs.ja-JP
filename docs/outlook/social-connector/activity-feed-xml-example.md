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
# <a name="activity-feed-xml-example"></a><span data-ttu-id="e051c-103">アクティビティ フィード XML の例</span><span class="sxs-lookup"><span data-stu-id="e051c-103">Activity Feed XML Example</span></span>

<span data-ttu-id="e051c-104">このトピックの XML 例は、ソーシャル ネットワークの[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを呼び出した後、Outlook Social Connector (OSC) に返されるアクティビティ フィード XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="e051c-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="e051c-105">この例では **、activityDetails** 要素で区切られた次の 4 つのアクティビティを含む **activityFeed** XML を示し、表示目的でテンプレートと一致します。</span><span class="sxs-lookup"><span data-stu-id="e051c-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="e051c-106">Melissa Macbeth によるプロファイル画像の更新。そのソーシャル ネットワーク上の **ownerID** は 4667647 です。</span><span class="sxs-lookup"><span data-stu-id="e051c-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="e051c-107">このアクティビティは **、publisherVariable、listVariable、\*\*\*\*および** **pictureVariable (listVariable** で囲まれた) の 3 つのテンプレート変数 **を指定します**。</span><span class="sxs-lookup"><span data-stu-id="e051c-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="e051c-108">これらの変数は、アクティビティ フィード アイテムを公開したユーザーと、更新する図の情報を指定します **(pictureVariable** の名前、**値\*\*\*\*、altText、\*\*\*\*および href** 子要素を使用します)。 </span><span class="sxs-lookup"><span data-stu-id="e051c-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="e051c-109">ソーシャル ネットワーク上の **ownerID** が 5015012 である Michael Affronti によるプロファイル画像の更新。</span><span class="sxs-lookup"><span data-stu-id="e051c-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="e051c-110">最後のアクティビティと同様に、このアクティビティは **publisherVariable、listVariable、pictureVariable** の 3 つのテンプレート変数 **を指定します**。 </span><span class="sxs-lookup"><span data-stu-id="e051c-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="e051c-111">これらの変数は、アクティビティ フィード アイテムを公開したユーザーと、更新する画像の情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="e051c-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="e051c-112">Michael Affronti による状態の更新で、最後のアクティビティと同じ **ownerID** 5015012 が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e051c-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="e051c-113">このアクティビティは、publisherVariable 型と **textVariable 型の 2** つの **テンプレート変数を指定します**。</span><span class="sxs-lookup"><span data-stu-id="e051c-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="e051c-114">**publisherVariable は** 、アクティビティ フィード アイテムを公開したユーザーを指定し **、textVariable には** 状態行 **の** 値が含まれます  `is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="e051c-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="e051c-115">Michael Affronti のブログ投稿で、最後の 2 つのアクティビティと同じ **ownerID** 5015012 が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e051c-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="e051c-116">このアクティビティは、publisherVariable 型と **linkVariable 型の 2** つの **テンプレート変数を指定します**。</span><span class="sxs-lookup"><span data-stu-id="e051c-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="e051c-117">**publisherVariable は**、アクティビティ フィード アイテムを公開したユーザーを指定し **、linkVariable** にはブログ投稿に関する詳細な情報 **(linkVariable** の名前、テキスト、および値の子要素で指定) が含まれます。 </span><span class="sxs-lookup"><span data-stu-id="e051c-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="e051c-118">4 つのアクティビティのそれぞれは **templateID** 値を指定します。これは templates 要素で指定された 3 つのテンプレートの 1 つと **一致** します。</span><span class="sxs-lookup"><span data-stu-id="e051c-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="e051c-119">各テンプレートは、独自の **activityTemplateContainer** 要素に含め、同じ **templateID** 値を持つアクティビティの表示にも使用される **templateID** 値で識別されます。</span><span class="sxs-lookup"><span data-stu-id="e051c-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="e051c-120">この例で使用される XML 要素の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e051c-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="e051c-121">アクティビティ フィード アイテムの XML の概要</span><span class="sxs-lookup"><span data-stu-id="e051c-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="e051c-122">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="e051c-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="e051c-123">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="e051c-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="e051c-124">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="e051c-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="e051c-125">XML の例</span><span class="sxs-lookup"><span data-stu-id="e051c-125">XML example</span></span>

<span data-ttu-id="e051c-126">次の例は **、2 つの** プロファイル画像の更新、状態の更新、およびブログ投稿の 4 つのアクティビティの activityFeed XML を示しています。</span><span class="sxs-lookup"><span data-stu-id="e051c-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="e051c-127">XML では、対応するアクティビティを表示するための 3 つのアクティビティ表示テンプレートも指定します。</span><span class="sxs-lookup"><span data-stu-id="e051c-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="e051c-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e051c-128">See also</span></span>

- [<span data-ttu-id="e051c-129">OSC プロバイダー XML の例</span><span class="sxs-lookup"><span data-stu-id="e051c-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="e051c-130">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="e051c-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="e051c-131">機能 XML の例</span><span class="sxs-lookup"><span data-stu-id="e051c-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="e051c-132">Friends XML の例</span><span class="sxs-lookup"><span data-stu-id="e051c-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="e051c-133">Outlookソーシャル コネクタ プロバイダー XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="e051c-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

