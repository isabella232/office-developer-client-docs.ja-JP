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
# <a name="template-variables"></a><span data-ttu-id="d8f87-103">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="d8f87-103">Template variables</span></span>

<span data-ttu-id="d8f87-104">テンプレート変数のインスタンス **(templateVariable** 要素で表されます) は、アクティビティ テンプレート内のアクティビティ フィード アイテムのデータを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8f87-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="d8f87-105">アクティビティ フィード XML の例については、「アクティビティ フィード [XML の例」を参照してください](activity-feed-xml-example.md)。</span><span class="sxs-lookup"><span data-stu-id="d8f87-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="d8f87-106">次の表に、サポートされているテンプレート変数の種類を示します。各変数は、対応する XML 列挙値で表されます。</span><span class="sxs-lookup"><span data-stu-id="d8f87-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="d8f87-107">**テンプレート変数の種類**</span><span class="sxs-lookup"><span data-stu-id="d8f87-107">**Type of template variable**</span></span>|<span data-ttu-id="d8f87-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8f87-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8f87-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="d8f87-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="d8f87-110">人、グループ、または物。</span><span class="sxs-lookup"><span data-stu-id="d8f87-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="d8f87-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="d8f87-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="d8f87-112">リンク。</span><span class="sxs-lookup"><span data-stu-id="d8f87-112">A link.</span></span>  <br/> |
|<span data-ttu-id="d8f87-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="d8f87-113">**listVariable**</span></span> <br/> |<span data-ttu-id="d8f87-114">オブジェクトのグループ。</span><span class="sxs-lookup"><span data-stu-id="d8f87-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="d8f87-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="d8f87-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="d8f87-116">画像です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="d8f87-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="d8f87-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="d8f87-118">アクティビティ フィード アイテムの発行元。</span><span class="sxs-lookup"><span data-stu-id="d8f87-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="d8f87-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="d8f87-119">**textVariable**</span></span> <br/> |<span data-ttu-id="d8f87-120">テキストのブロック。</span><span class="sxs-lookup"><span data-stu-id="d8f87-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="d8f87-121">テンプレート変数の各種類には、その変数に関するデータを指定するために必要な要素があります。</span><span class="sxs-lookup"><span data-stu-id="d8f87-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="d8f87-122">テンプレート変数は次のように指定されます。</span><span class="sxs-lookup"><span data-stu-id="d8f87-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="d8f87-123">リスト テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="d8f87-123">List template variable</span></span>

<span data-ttu-id="d8f87-124">リスト内に含まれるテンプレート変数 **(listVariable** 要素と **listItems** 要素で区切られた) を次のように指定できます。</span><span class="sxs-lookup"><span data-stu-id="d8f87-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="d8f87-125">**listVariable 型のテンプレート変数は**、オブジェクトのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="d8f87-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="d8f87-126">コンマで区切られた項目 **(linkVariable** または **textVariable 型** ) またはピクチャ **(pictureVariable** 型の) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d8f87-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="d8f87-127">リストには、最大 5 つのリンク アイテム、5 つのテキスト アイテム、または 5 つの画像を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d8f87-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="d8f87-128">Outlook Social Connector (OSC) は、Windows システム ロケールに従ってリンクまたはテキスト リスト アイテムをローカライズします。</span><span class="sxs-lookup"><span data-stu-id="d8f87-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="d8f87-129">アクティビティ フィード アイテム内の画像を正しく解析して表示するには、画像をリストに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8f87-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="d8f87-130">すべての画像のサイズは、高さ 52 ピクセルに変更されます。</span><span class="sxs-lookup"><span data-stu-id="d8f87-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="d8f87-131">画像の幅はサイズ変更されません。</span><span class="sxs-lookup"><span data-stu-id="d8f87-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="d8f87-132">テンプレート変数要素</span><span class="sxs-lookup"><span data-stu-id="d8f87-132">Template variable elements</span></span>

<span data-ttu-id="d8f87-133">このセクションでは、テンプレート変数の種類ごとにサポートされる必須要素と省略可能な要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="d8f87-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="d8f87-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="d8f87-134">entityVariable</span></span>

|<span data-ttu-id="d8f87-135">**要素**</span><span class="sxs-lookup"><span data-stu-id="d8f87-135">**Element**</span></span>|<span data-ttu-id="d8f87-136">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8f87-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8f87-137">**name**</span><span class="sxs-lookup"><span data-stu-id="d8f87-137">**name**</span></span> <br/> |<span data-ttu-id="d8f87-138">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="d8f87-138">The name of the variable.</span></span> <span data-ttu-id="d8f87-139">必須です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-139">Required.</span></span>  <br/> |
|<span data-ttu-id="d8f87-140">**id**</span><span class="sxs-lookup"><span data-stu-id="d8f87-140">**id**</span></span> <br/> |<span data-ttu-id="d8f87-141">ユーザーの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="d8f87-141">The unique ID of the user.</span></span> <span data-ttu-id="d8f87-142">必須です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-142">Required.</span></span>  <br/> |
|<span data-ttu-id="d8f87-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="d8f87-143">**nameHint**</span></span> <br/> |<span data-ttu-id="d8f87-144">フィード アイテムに表示する名前。</span><span class="sxs-lookup"><span data-stu-id="d8f87-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="d8f87-145">オプション。</span><span class="sxs-lookup"><span data-stu-id="d8f87-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="d8f87-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="d8f87-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="d8f87-147">ユーザーの名前が存在する場合、フィード アイテム内のユーザー名のハイパーリンクとして使用されるユーザーのプロファイルの URL。</span><span class="sxs-lookup"><span data-stu-id="d8f87-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="d8f87-148">オプション。</span><span class="sxs-lookup"><span data-stu-id="d8f87-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="d8f87-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="d8f87-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="d8f87-150">Outlook でこのユーザーの連絡先情報を更新するために使用される電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="d8f87-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="d8f87-151">オプション。</span><span class="sxs-lookup"><span data-stu-id="d8f87-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="d8f87-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="d8f87-152">linkVariable</span></span>

|<span data-ttu-id="d8f87-153">**要素**</span><span class="sxs-lookup"><span data-stu-id="d8f87-153">**Element**</span></span>|<span data-ttu-id="d8f87-154">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8f87-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8f87-155">**name**</span><span class="sxs-lookup"><span data-stu-id="d8f87-155">**name**</span></span> <br/> |<span data-ttu-id="d8f87-156">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="d8f87-156">The name of the variable.</span></span> <span data-ttu-id="d8f87-157">必須です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-157">Required.</span></span>  <br/> |
|<span data-ttu-id="d8f87-158">**value**</span><span class="sxs-lookup"><span data-stu-id="d8f87-158">**value**</span></span> <br/> |<span data-ttu-id="d8f87-159">このリンクの URL。</span><span class="sxs-lookup"><span data-stu-id="d8f87-159">The URL for this link.</span></span> <span data-ttu-id="d8f87-160">必須です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-160">Required.</span></span>  <br/> |
|<span data-ttu-id="d8f87-161">**text**</span><span class="sxs-lookup"><span data-stu-id="d8f87-161">**text**</span></span> <br/> |<span data-ttu-id="d8f87-162">URL 自体の代わりに表示するリンク テキスト。</span><span class="sxs-lookup"><span data-stu-id="d8f87-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="d8f87-163">オプション。</span><span class="sxs-lookup"><span data-stu-id="d8f87-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="d8f87-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="d8f87-164">listVariable</span></span>

|<span data-ttu-id="d8f87-165">**要素**</span><span class="sxs-lookup"><span data-stu-id="d8f87-165">**Element**</span></span>|<span data-ttu-id="d8f87-166">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8f87-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8f87-167">**name**</span><span class="sxs-lookup"><span data-stu-id="d8f87-167">**name**</span></span> <br/> |<span data-ttu-id="d8f87-168">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="d8f87-168">The name of the variable.</span></span> <span data-ttu-id="d8f87-169">必須です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-169">Required.</span></span>  <br/> |
|<span data-ttu-id="d8f87-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="d8f87-170">**listItems**</span></span> <br/> |<span data-ttu-id="d8f87-171">リスト内のアイテムのコンテナー。</span><span class="sxs-lookup"><span data-stu-id="d8f87-171">A container for items in the list.</span></span> <span data-ttu-id="d8f87-172">必須です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="d8f87-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="d8f87-173">pictureVariable</span></span>

|<span data-ttu-id="d8f87-174">**要素**</span><span class="sxs-lookup"><span data-stu-id="d8f87-174">**Element**</span></span>|<span data-ttu-id="d8f87-175">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8f87-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8f87-176">**name**</span><span class="sxs-lookup"><span data-stu-id="d8f87-176">**name**</span></span> <br/> |<span data-ttu-id="d8f87-177">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="d8f87-177">The name of the variable.</span></span> <span data-ttu-id="d8f87-178">必須です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-178">Required.</span></span>  <br/> |
|<span data-ttu-id="d8f87-179">**value**</span><span class="sxs-lookup"><span data-stu-id="d8f87-179">**value**</span></span> <br/> |<span data-ttu-id="d8f87-180">画像の URL。</span><span class="sxs-lookup"><span data-stu-id="d8f87-180">The URL for the picture.</span></span> <span data-ttu-id="d8f87-181">必須です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-181">Required.</span></span>  <br/> |
|<span data-ttu-id="d8f87-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="d8f87-182">**altText**</span></span> <br/> |<span data-ttu-id="d8f87-183">ユーザー補助のために、およびユーザーが画像の上にマウス ポインターを移動するときに表示する代替テキスト。</span><span class="sxs-lookup"><span data-stu-id="d8f87-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="d8f87-184">オプション。</span><span class="sxs-lookup"><span data-stu-id="d8f87-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="d8f87-185">**href**</span><span class="sxs-lookup"><span data-stu-id="d8f87-185">**href**</span></span> <br/> |<span data-ttu-id="d8f87-186">目的のターゲットが value 要素で指定されたピクチャ URL ではない場合、ユーザーが画像をクリックするときに使用する **ハイパーリンク** 。</span><span class="sxs-lookup"><span data-stu-id="d8f87-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="d8f87-187">オプション。</span><span class="sxs-lookup"><span data-stu-id="d8f87-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="d8f87-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="d8f87-188">publisherVariable</span></span>

|<span data-ttu-id="d8f87-189">**要素**</span><span class="sxs-lookup"><span data-stu-id="d8f87-189">**Element**</span></span>|<span data-ttu-id="d8f87-190">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8f87-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8f87-191">**name**</span><span class="sxs-lookup"><span data-stu-id="d8f87-191">**name**</span></span> <br/> |<span data-ttu-id="d8f87-192">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="d8f87-192">The name of the variable.</span></span> <span data-ttu-id="d8f87-193">必須です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-193">Required.</span></span>  <br/> |
|<span data-ttu-id="d8f87-194">**id**</span><span class="sxs-lookup"><span data-stu-id="d8f87-194">**id**</span></span> <br/> |<span data-ttu-id="d8f87-195">ユーザーの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="d8f87-195">The unique ID of the user.</span></span> <span data-ttu-id="d8f87-196">必須です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-196">Required.</span></span>  <br/> |
|<span data-ttu-id="d8f87-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="d8f87-197">**nameHint**</span></span> <br/> |<span data-ttu-id="d8f87-198">フィード アイテムに表示する名前。</span><span class="sxs-lookup"><span data-stu-id="d8f87-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="d8f87-199">オプション。</span><span class="sxs-lookup"><span data-stu-id="d8f87-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="d8f87-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="d8f87-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="d8f87-201">ユーザーの名前が存在する場合、フィード アイテム内のユーザー名のハイパーリンクとして使用されるユーザーのプロファイルの URL。</span><span class="sxs-lookup"><span data-stu-id="d8f87-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="d8f87-202">オプション。</span><span class="sxs-lookup"><span data-stu-id="d8f87-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="d8f87-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="d8f87-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="d8f87-204">Outlook でこのユーザーの連絡先情報を更新するために使用される電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="d8f87-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="d8f87-205">オプション。</span><span class="sxs-lookup"><span data-stu-id="d8f87-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="d8f87-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="d8f87-206">textVariable</span></span>

|<span data-ttu-id="d8f87-207">**要素**</span><span class="sxs-lookup"><span data-stu-id="d8f87-207">**Element**</span></span>|<span data-ttu-id="d8f87-208">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8f87-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8f87-209">**name**</span><span class="sxs-lookup"><span data-stu-id="d8f87-209">**name**</span></span> <br/> |<span data-ttu-id="d8f87-210">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="d8f87-210">The name of the variable.</span></span> <span data-ttu-id="d8f87-211">必須です。</span><span class="sxs-lookup"><span data-stu-id="d8f87-211">Required.</span></span>  <br/> |
|<span data-ttu-id="d8f87-212">**value**</span><span class="sxs-lookup"><span data-stu-id="d8f87-212">**value**</span></span> <br/> |<span data-ttu-id="d8f87-213">表示するテキスト。</span><span class="sxs-lookup"><span data-stu-id="d8f87-213">The text to display.</span></span> <span data-ttu-id="d8f87-214">オプション。</span><span class="sxs-lookup"><span data-stu-id="d8f87-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8f87-215">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8f87-215">See also</span></span>

- [<span data-ttu-id="d8f87-216">アクティビティ フィード アイテムの XML の概要</span><span class="sxs-lookup"><span data-stu-id="d8f87-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="d8f87-217">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="d8f87-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="d8f87-218">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="d8f87-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="d8f87-219">アクティビティを適切に表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="d8f87-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="d8f87-220">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="d8f87-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="d8f87-221">Outlook ソーシャル コネクタ プロバイダー XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="d8f87-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="d8f87-222">OSC XML スキーマを使用したプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="d8f87-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

