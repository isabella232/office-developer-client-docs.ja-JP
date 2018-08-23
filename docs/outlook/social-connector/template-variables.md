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
# <a name="template-variables"></a><span data-ttu-id="a914b-103">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="a914b-103">Template variables</span></span>

<span data-ttu-id="a914b-104">( **TemplateVariable**要素によって表されます) のテンプレート変数のインスタンスでは、アクティビティ フィード項目のアクティビティ テンプレートでのデータを指定します。</span><span class="sxs-lookup"><span data-stu-id="a914b-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="a914b-105">アクティビティの例については、フィードの XML、[アクティビティ フィードの XML の例](activity-feed-xml-example.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a914b-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="a914b-106">次の表は、XML の対応する列挙値によって表される各サポートされているテンプレートの変数の種類を示しています。</span><span class="sxs-lookup"><span data-stu-id="a914b-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="a914b-107">**テンプレート変数の型**</span><span class="sxs-lookup"><span data-stu-id="a914b-107">**Type of template variable**</span></span>|<span data-ttu-id="a914b-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="a914b-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a914b-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="a914b-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="a914b-110">ユーザー、グループ、またはです。</span><span class="sxs-lookup"><span data-stu-id="a914b-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="a914b-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="a914b-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="a914b-112">リンクです。</span><span class="sxs-lookup"><span data-stu-id="a914b-112">A link.</span></span>  <br/> |
|<span data-ttu-id="a914b-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="a914b-113">**listVariable**</span></span> <br/> |<span data-ttu-id="a914b-114">オブジェクトのグループです。</span><span class="sxs-lookup"><span data-stu-id="a914b-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="a914b-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="a914b-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="a914b-116">画像です。</span><span class="sxs-lookup"><span data-stu-id="a914b-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="a914b-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="a914b-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="a914b-118">活動の出版社では、アイテムをフィードします。</span><span class="sxs-lookup"><span data-stu-id="a914b-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="a914b-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="a914b-119">**textVariable**</span></span> <br/> |<span data-ttu-id="a914b-120">テキストのブロックです。</span><span class="sxs-lookup"><span data-stu-id="a914b-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="a914b-121">テンプレート変数の各タイプには、その変数に関するデータを指定する要素が必要でした。</span><span class="sxs-lookup"><span data-stu-id="a914b-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="a914b-122">テンプレート変数の指定は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a914b-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="a914b-123">リストのテンプレート変数</span><span class="sxs-lookup"><span data-stu-id="a914b-123">List template variable</span></span>

<span data-ttu-id="a914b-124">リスト内で、( **listVariable**および**リスト項目**の要素で区切られた) 次のように格納されているテンプレートの変数を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a914b-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="a914b-125">**ListVariable**型のテンプレート変数は、オブジェクトのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="a914b-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="a914b-126">これは、コンマで区切られた (の種類のアイテム、 **linkVariable**または**textVariable** ) または ( **pictureVariable**型) の画像を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a914b-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="a914b-127">リストは、5 つのリンク アイテム、5 つのテキスト、または 5 つの画像を含むことができます。</span><span class="sxs-lookup"><span data-stu-id="a914b-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="a914b-128">Outlook ソーシャル コネクタ (OSC) は、Windows のシステム ロケール] ボックスの一覧項目をリンクまたはテキストをローカライズします。</span><span class="sxs-lookup"><span data-stu-id="a914b-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="a914b-129">正しく解析して、アクティビティ フィードのアイテムに画像を表示、リスト内の画像を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a914b-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="a914b-130">すべての画像は、高さ 52 ピクセルにサイズ変更されます。</span><span class="sxs-lookup"><span data-stu-id="a914b-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="a914b-131">画像の幅のサイズは変更されません。</span><span class="sxs-lookup"><span data-stu-id="a914b-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="a914b-132">テンプレートの可変要素</span><span class="sxs-lookup"><span data-stu-id="a914b-132">Template variable elements</span></span>

<span data-ttu-id="a914b-133">このセクションでは、テンプレート変数の種類ごとにサポートされる必須および省略可能な要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="a914b-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="a914b-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="a914b-134">entityVariable</span></span>

|<span data-ttu-id="a914b-135">**要素**</span><span class="sxs-lookup"><span data-stu-id="a914b-135">**Element**</span></span>|<span data-ttu-id="a914b-136">**説明**</span><span class="sxs-lookup"><span data-stu-id="a914b-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a914b-137">**name**</span><span class="sxs-lookup"><span data-stu-id="a914b-137">**name**</span></span> <br/> |<span data-ttu-id="a914b-138">変数の名前です。</span><span class="sxs-lookup"><span data-stu-id="a914b-138">The name of the variable.</span></span> <span data-ttu-id="a914b-139">必須。</span><span class="sxs-lookup"><span data-stu-id="a914b-139">Required.</span></span>  <br/> |
|<span data-ttu-id="a914b-140">**id**</span><span class="sxs-lookup"><span data-stu-id="a914b-140">**id**</span></span> <br/> |<span data-ttu-id="a914b-141">ユーザーの一意の ID です。</span><span class="sxs-lookup"><span data-stu-id="a914b-141">The unique ID of the user.</span></span> <span data-ttu-id="a914b-142">必須。</span><span class="sxs-lookup"><span data-stu-id="a914b-142">Required.</span></span>  <br/> |
|<span data-ttu-id="a914b-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="a914b-143">**nameHint**</span></span> <br/> |<span data-ttu-id="a914b-144">フィードの項目に表示される名前です。</span><span class="sxs-lookup"><span data-stu-id="a914b-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="a914b-145">省略可能。</span><span class="sxs-lookup"><span data-stu-id="a914b-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="a914b-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="a914b-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="a914b-147">として使用するハイパーリンクでは、フィードの項目では、人の名前の人の名前が存在する場合、ユーザーのプロファイルの URL です。</span><span class="sxs-lookup"><span data-stu-id="a914b-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="a914b-148">省略可能。</span><span class="sxs-lookup"><span data-stu-id="a914b-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="a914b-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="a914b-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="a914b-150">Outlook で、このユーザーの連絡先情報を更新するために使用される電子メール アドレスです。</span><span class="sxs-lookup"><span data-stu-id="a914b-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="a914b-151">省略可能。</span><span class="sxs-lookup"><span data-stu-id="a914b-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="a914b-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="a914b-152">linkVariable</span></span>

|<span data-ttu-id="a914b-153">**要素**</span><span class="sxs-lookup"><span data-stu-id="a914b-153">**Element**</span></span>|<span data-ttu-id="a914b-154">**説明**</span><span class="sxs-lookup"><span data-stu-id="a914b-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a914b-155">**name**</span><span class="sxs-lookup"><span data-stu-id="a914b-155">**name**</span></span> <br/> |<span data-ttu-id="a914b-156">変数の名前です。</span><span class="sxs-lookup"><span data-stu-id="a914b-156">The name of the variable.</span></span> <span data-ttu-id="a914b-157">必須。</span><span class="sxs-lookup"><span data-stu-id="a914b-157">Required.</span></span>  <br/> |
|<span data-ttu-id="a914b-158">**value**</span><span class="sxs-lookup"><span data-stu-id="a914b-158">**value**</span></span> <br/> |<span data-ttu-id="a914b-159">このリンクの URL です。</span><span class="sxs-lookup"><span data-stu-id="a914b-159">The URL for this link.</span></span> <span data-ttu-id="a914b-160">必須。</span><span class="sxs-lookup"><span data-stu-id="a914b-160">Required.</span></span>  <br/> |
|<span data-ttu-id="a914b-161">**text**</span><span class="sxs-lookup"><span data-stu-id="a914b-161">**text**</span></span> <br/> |<span data-ttu-id="a914b-162">URL 自体の代わりに表示するリンク テキストです。</span><span class="sxs-lookup"><span data-stu-id="a914b-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="a914b-163">省略可能。</span><span class="sxs-lookup"><span data-stu-id="a914b-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="a914b-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="a914b-164">listVariable</span></span>

|<span data-ttu-id="a914b-165">**要素**</span><span class="sxs-lookup"><span data-stu-id="a914b-165">**Element**</span></span>|<span data-ttu-id="a914b-166">**説明**</span><span class="sxs-lookup"><span data-stu-id="a914b-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a914b-167">**name**</span><span class="sxs-lookup"><span data-stu-id="a914b-167">**name**</span></span> <br/> |<span data-ttu-id="a914b-168">変数の名前です。</span><span class="sxs-lookup"><span data-stu-id="a914b-168">The name of the variable.</span></span> <span data-ttu-id="a914b-169">必須。</span><span class="sxs-lookup"><span data-stu-id="a914b-169">Required.</span></span>  <br/> |
|<span data-ttu-id="a914b-170">**リスト項目**</span><span class="sxs-lookup"><span data-stu-id="a914b-170">**listItems**</span></span> <br/> |<span data-ttu-id="a914b-171">リスト内の項目のコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="a914b-171">A container for items in the list.</span></span> <span data-ttu-id="a914b-172">必須。</span><span class="sxs-lookup"><span data-stu-id="a914b-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="a914b-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="a914b-173">pictureVariable</span></span>

|<span data-ttu-id="a914b-174">**要素**</span><span class="sxs-lookup"><span data-stu-id="a914b-174">**Element**</span></span>|<span data-ttu-id="a914b-175">**説明**</span><span class="sxs-lookup"><span data-stu-id="a914b-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a914b-176">**name**</span><span class="sxs-lookup"><span data-stu-id="a914b-176">**name**</span></span> <br/> |<span data-ttu-id="a914b-177">変数の名前です。</span><span class="sxs-lookup"><span data-stu-id="a914b-177">The name of the variable.</span></span> <span data-ttu-id="a914b-178">必須。</span><span class="sxs-lookup"><span data-stu-id="a914b-178">Required.</span></span>  <br/> |
|<span data-ttu-id="a914b-179">**value**</span><span class="sxs-lookup"><span data-stu-id="a914b-179">**value**</span></span> <br/> |<span data-ttu-id="a914b-180">画像の URL です。</span><span class="sxs-lookup"><span data-stu-id="a914b-180">The URL for the picture.</span></span> <span data-ttu-id="a914b-181">必須。</span><span class="sxs-lookup"><span data-stu-id="a914b-181">Required.</span></span>  <br/> |
|<span data-ttu-id="a914b-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="a914b-182">**altText**</span></span> <br/> |<span data-ttu-id="a914b-183">ユーザー補助と、ユーザーが画像上でマウス ポインターを移動するとに表示する代替テキスト。</span><span class="sxs-lookup"><span data-stu-id="a914b-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="a914b-184">省略可能。</span><span class="sxs-lookup"><span data-stu-id="a914b-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="a914b-185">**href**</span><span class="sxs-lookup"><span data-stu-id="a914b-185">**href**</span></span> <br/> |<span data-ttu-id="a914b-186">目的のターゲット**値**の要素によって指定された画像の URL でない場合、画像をクリックするとを使用するハイパーリンク。</span><span class="sxs-lookup"><span data-stu-id="a914b-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="a914b-187">省略可能。</span><span class="sxs-lookup"><span data-stu-id="a914b-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="a914b-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="a914b-188">publisherVariable</span></span>

|<span data-ttu-id="a914b-189">**要素**</span><span class="sxs-lookup"><span data-stu-id="a914b-189">**Element**</span></span>|<span data-ttu-id="a914b-190">**説明**</span><span class="sxs-lookup"><span data-stu-id="a914b-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a914b-191">**name**</span><span class="sxs-lookup"><span data-stu-id="a914b-191">**name**</span></span> <br/> |<span data-ttu-id="a914b-192">変数の名前です。</span><span class="sxs-lookup"><span data-stu-id="a914b-192">The name of the variable.</span></span> <span data-ttu-id="a914b-193">必須。</span><span class="sxs-lookup"><span data-stu-id="a914b-193">Required.</span></span>  <br/> |
|<span data-ttu-id="a914b-194">**id**</span><span class="sxs-lookup"><span data-stu-id="a914b-194">**id**</span></span> <br/> |<span data-ttu-id="a914b-195">ユーザーの一意の ID です。</span><span class="sxs-lookup"><span data-stu-id="a914b-195">The unique ID of the user.</span></span> <span data-ttu-id="a914b-196">必須。</span><span class="sxs-lookup"><span data-stu-id="a914b-196">Required.</span></span>  <br/> |
|<span data-ttu-id="a914b-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="a914b-197">**nameHint**</span></span> <br/> |<span data-ttu-id="a914b-198">フィードの項目に表示される名前です。</span><span class="sxs-lookup"><span data-stu-id="a914b-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="a914b-199">省略可能。</span><span class="sxs-lookup"><span data-stu-id="a914b-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="a914b-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="a914b-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="a914b-201">として使用するハイパーリンクでは、フィードの項目では、人の名前の人の名前が存在する場合、ユーザーのプロファイルの URL です。</span><span class="sxs-lookup"><span data-stu-id="a914b-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="a914b-202">省略可能。</span><span class="sxs-lookup"><span data-stu-id="a914b-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="a914b-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="a914b-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="a914b-204">Outlook で、このユーザーの連絡先情報を更新するために使用される電子メール アドレスです。</span><span class="sxs-lookup"><span data-stu-id="a914b-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="a914b-205">省略可能。</span><span class="sxs-lookup"><span data-stu-id="a914b-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="a914b-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="a914b-206">textVariable</span></span>

|<span data-ttu-id="a914b-207">**要素**</span><span class="sxs-lookup"><span data-stu-id="a914b-207">**Element**</span></span>|<span data-ttu-id="a914b-208">**説明**</span><span class="sxs-lookup"><span data-stu-id="a914b-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a914b-209">**name**</span><span class="sxs-lookup"><span data-stu-id="a914b-209">**name**</span></span> <br/> |<span data-ttu-id="a914b-210">変数の名前です。</span><span class="sxs-lookup"><span data-stu-id="a914b-210">The name of the variable.</span></span> <span data-ttu-id="a914b-211">必須。</span><span class="sxs-lookup"><span data-stu-id="a914b-211">Required.</span></span>  <br/> |
|<span data-ttu-id="a914b-212">**value**</span><span class="sxs-lookup"><span data-stu-id="a914b-212">**value**</span></span> <br/> |<span data-ttu-id="a914b-213">表示するテキスト。</span><span class="sxs-lookup"><span data-stu-id="a914b-213">The text to display.</span></span> <span data-ttu-id="a914b-214">省略可能。</span><span class="sxs-lookup"><span data-stu-id="a914b-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a914b-215">関連項目</span><span class="sxs-lookup"><span data-stu-id="a914b-215">See also</span></span>

- [<span data-ttu-id="a914b-216">フィード アイテムの活動項目の XML の概要</span><span class="sxs-lookup"><span data-stu-id="a914b-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="a914b-217">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="a914b-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="a914b-218">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="a914b-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="a914b-219">アクティビティを正しく表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="a914b-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="a914b-220">活動の XML</span><span class="sxs-lookup"><span data-stu-id="a914b-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="a914b-221">Outlook ソーシャル コネクタ プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="a914b-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="a914b-222">OSC の XML スキーマを使用してプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="a914b-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

