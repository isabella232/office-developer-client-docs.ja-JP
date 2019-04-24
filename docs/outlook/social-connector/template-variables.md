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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329177"
---
# <a name="template-variables"></a><span data-ttu-id="32ef7-103">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="32ef7-103">Template variables</span></span>

<span data-ttu-id="32ef7-104">テンプレート変数のインスタンス ( **templateVariable**要素で表されます) は、アクティビティテンプレート内のアクティビティフィードアイテムのデータを指定します。</span><span class="sxs-lookup"><span data-stu-id="32ef7-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="32ef7-105">アクティビティフィード xml の例については、「[アクティビティフィード xml の例](activity-feed-xml-example.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="32ef7-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="32ef7-106">次の表に、対応する XML 列挙値で表される、サポートされるテンプレート変数の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="32ef7-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="32ef7-107">**テンプレート変数の種類**</span><span class="sxs-lookup"><span data-stu-id="32ef7-107">**Type of template variable**</span></span>|<span data-ttu-id="32ef7-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="32ef7-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32ef7-109">**entityvariable**</span><span class="sxs-lookup"><span data-stu-id="32ef7-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="32ef7-110">個人、グループ、または事柄。</span><span class="sxs-lookup"><span data-stu-id="32ef7-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="32ef7-111">**linkvariable**</span><span class="sxs-lookup"><span data-stu-id="32ef7-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="32ef7-112">リンク。</span><span class="sxs-lookup"><span data-stu-id="32ef7-112">A link.</span></span>  <br/> |
|<span data-ttu-id="32ef7-113">**listvariable**</span><span class="sxs-lookup"><span data-stu-id="32ef7-113">**listVariable**</span></span> <br/> |<span data-ttu-id="32ef7-114">オブジェクトのグループ。</span><span class="sxs-lookup"><span data-stu-id="32ef7-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="32ef7-115">**ピクチャ変数**</span><span class="sxs-lookup"><span data-stu-id="32ef7-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="32ef7-116">画像です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="32ef7-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="32ef7-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="32ef7-118">アクティビティフィードアイテムの発行元。</span><span class="sxs-lookup"><span data-stu-id="32ef7-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="32ef7-119">**textvariable**</span><span class="sxs-lookup"><span data-stu-id="32ef7-119">**textVariable**</span></span> <br/> |<span data-ttu-id="32ef7-120">テキストのブロック。</span><span class="sxs-lookup"><span data-stu-id="32ef7-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="32ef7-121">各種類のテンプレート変数には、その変数に関するデータを指定するために必要な要素があります。</span><span class="sxs-lookup"><span data-stu-id="32ef7-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="32ef7-122">テンプレート変数は次のように指定されます。</span><span class="sxs-lookup"><span data-stu-id="32ef7-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="32ef7-123">リストテンプレート変数</span><span class="sxs-lookup"><span data-stu-id="32ef7-123">List template variable</span></span>

<span data-ttu-id="32ef7-124">リスト内に含まれるテンプレート変数 ( **listvariable**および**listItems**要素で区切られたもの) を次のように指定できます。</span><span class="sxs-lookup"><span data-stu-id="32ef7-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="32ef7-125">**listvariable**型のテンプレート変数は、オブジェクトのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="32ef7-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="32ef7-126">このオブジェクトには、( **linkvariable**または**textvariable**型の) (または、図の**変数**型の) コンマ区切りのアイテムを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="32ef7-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="32ef7-127">リストには最大5つのリンク項目、5つのテキスト項目、または5つの画像を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="32ef7-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="32ef7-128">Outlook Social Connector (.osc) は、Windows システムロケールに従って、リンクまたはテキストリストアイテムをローカライズします。</span><span class="sxs-lookup"><span data-stu-id="32ef7-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="32ef7-129">アクティビティフィードアイテムで画像を正しく解析して表示するには、画像をリストに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="32ef7-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="32ef7-130">すべての図の高さを52ピクセルに変更します。</span><span class="sxs-lookup"><span data-stu-id="32ef7-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="32ef7-131">図の幅は変更されません。</span><span class="sxs-lookup"><span data-stu-id="32ef7-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="32ef7-132">テンプレート変数要素</span><span class="sxs-lookup"><span data-stu-id="32ef7-132">Template variable elements</span></span>

<span data-ttu-id="32ef7-133">このセクションでは、テンプレート変数の種類ごとに、必要な要素とオプションの要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="32ef7-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="32ef7-134">entityvariable</span><span class="sxs-lookup"><span data-stu-id="32ef7-134">entityVariable</span></span>

|<span data-ttu-id="32ef7-135">**要素**</span><span class="sxs-lookup"><span data-stu-id="32ef7-135">**Element**</span></span>|<span data-ttu-id="32ef7-136">**説明**</span><span class="sxs-lookup"><span data-stu-id="32ef7-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32ef7-137">**name**</span><span class="sxs-lookup"><span data-stu-id="32ef7-137">**name**</span></span> <br/> |<span data-ttu-id="32ef7-138">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="32ef7-138">The name of the variable.</span></span> <span data-ttu-id="32ef7-139">必須です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-139">Required.</span></span>  <br/> |
|<span data-ttu-id="32ef7-140">**id**</span><span class="sxs-lookup"><span data-stu-id="32ef7-140">**id**</span></span> <br/> |<span data-ttu-id="32ef7-141">ユーザーの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="32ef7-141">The unique ID of the user.</span></span> <span data-ttu-id="32ef7-142">必須です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-142">Required.</span></span>  <br/> |
|<span data-ttu-id="32ef7-143">**namehint**</span><span class="sxs-lookup"><span data-stu-id="32ef7-143">**nameHint**</span></span> <br/> |<span data-ttu-id="32ef7-144">フィードアイテムに表示する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="32ef7-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="32ef7-145">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="32ef7-146">**profileurl**</span><span class="sxs-lookup"><span data-stu-id="32ef7-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="32ef7-147">ユーザーの名前が存在する場合に、フィードアイテムでのユーザー名のハイパーリンクとして使用される個人のプロファイルの URL。</span><span class="sxs-lookup"><span data-stu-id="32ef7-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="32ef7-148">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="32ef7-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="32ef7-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="32ef7-150">このユーザーの連絡先情報を Outlook で更新するために使用される電子メールアドレス。</span><span class="sxs-lookup"><span data-stu-id="32ef7-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="32ef7-151">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="32ef7-152">linkvariable</span><span class="sxs-lookup"><span data-stu-id="32ef7-152">linkVariable</span></span>

|<span data-ttu-id="32ef7-153">**要素**</span><span class="sxs-lookup"><span data-stu-id="32ef7-153">**Element**</span></span>|<span data-ttu-id="32ef7-154">**説明**</span><span class="sxs-lookup"><span data-stu-id="32ef7-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32ef7-155">**name**</span><span class="sxs-lookup"><span data-stu-id="32ef7-155">**name**</span></span> <br/> |<span data-ttu-id="32ef7-156">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="32ef7-156">The name of the variable.</span></span> <span data-ttu-id="32ef7-157">必須です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-157">Required.</span></span>  <br/> |
|<span data-ttu-id="32ef7-158">**value**</span><span class="sxs-lookup"><span data-stu-id="32ef7-158">**value**</span></span> <br/> |<span data-ttu-id="32ef7-159">このリンクの URL。</span><span class="sxs-lookup"><span data-stu-id="32ef7-159">The URL for this link.</span></span> <span data-ttu-id="32ef7-160">必須です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-160">Required.</span></span>  <br/> |
|<span data-ttu-id="32ef7-161">**text**</span><span class="sxs-lookup"><span data-stu-id="32ef7-161">**text**</span></span> <br/> |<span data-ttu-id="32ef7-162">URL 自体の代わりに表示するリンクテキスト。</span><span class="sxs-lookup"><span data-stu-id="32ef7-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="32ef7-163">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="32ef7-164">listvariable</span><span class="sxs-lookup"><span data-stu-id="32ef7-164">listVariable</span></span>

|<span data-ttu-id="32ef7-165">**要素**</span><span class="sxs-lookup"><span data-stu-id="32ef7-165">**Element**</span></span>|<span data-ttu-id="32ef7-166">**説明**</span><span class="sxs-lookup"><span data-stu-id="32ef7-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32ef7-167">**name**</span><span class="sxs-lookup"><span data-stu-id="32ef7-167">**name**</span></span> <br/> |<span data-ttu-id="32ef7-168">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="32ef7-168">The name of the variable.</span></span> <span data-ttu-id="32ef7-169">必須です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-169">Required.</span></span>  <br/> |
|<span data-ttu-id="32ef7-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="32ef7-170">**listItems**</span></span> <br/> |<span data-ttu-id="32ef7-171">リスト内のアイテムのコンテナー。</span><span class="sxs-lookup"><span data-stu-id="32ef7-171">A container for items in the list.</span></span> <span data-ttu-id="32ef7-172">必須です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="32ef7-173">ピクチャ変数</span><span class="sxs-lookup"><span data-stu-id="32ef7-173">pictureVariable</span></span>

|<span data-ttu-id="32ef7-174">**要素**</span><span class="sxs-lookup"><span data-stu-id="32ef7-174">**Element**</span></span>|<span data-ttu-id="32ef7-175">**説明**</span><span class="sxs-lookup"><span data-stu-id="32ef7-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32ef7-176">**name**</span><span class="sxs-lookup"><span data-stu-id="32ef7-176">**name**</span></span> <br/> |<span data-ttu-id="32ef7-177">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="32ef7-177">The name of the variable.</span></span> <span data-ttu-id="32ef7-178">必須です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-178">Required.</span></span>  <br/> |
|<span data-ttu-id="32ef7-179">**value**</span><span class="sxs-lookup"><span data-stu-id="32ef7-179">**value**</span></span> <br/> |<span data-ttu-id="32ef7-180">図の URL を示します。</span><span class="sxs-lookup"><span data-stu-id="32ef7-180">The URL for the picture.</span></span> <span data-ttu-id="32ef7-181">必須です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-181">Required.</span></span>  <br/> |
|<span data-ttu-id="32ef7-182">**alttext**</span><span class="sxs-lookup"><span data-stu-id="32ef7-182">**altText**</span></span> <br/> |<span data-ttu-id="32ef7-183">ユーザー補助のために表示する代替テキスト、およびユーザーがマウスポインターを画像の上に移動したとき。</span><span class="sxs-lookup"><span data-stu-id="32ef7-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="32ef7-184">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="32ef7-185">**href**</span><span class="sxs-lookup"><span data-stu-id="32ef7-185">**href**</span></span> <br/> |<span data-ttu-id="32ef7-186">目的のターゲットが**value**要素で指定された画像の URL ではない場合に、ユーザーがピクチャをクリックしたときに使用するハイパーリンク。</span><span class="sxs-lookup"><span data-stu-id="32ef7-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="32ef7-187">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="32ef7-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="32ef7-188">publisherVariable</span></span>

|<span data-ttu-id="32ef7-189">**要素**</span><span class="sxs-lookup"><span data-stu-id="32ef7-189">**Element**</span></span>|<span data-ttu-id="32ef7-190">**説明**</span><span class="sxs-lookup"><span data-stu-id="32ef7-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32ef7-191">**name**</span><span class="sxs-lookup"><span data-stu-id="32ef7-191">**name**</span></span> <br/> |<span data-ttu-id="32ef7-192">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="32ef7-192">The name of the variable.</span></span> <span data-ttu-id="32ef7-193">必須です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-193">Required.</span></span>  <br/> |
|<span data-ttu-id="32ef7-194">**id**</span><span class="sxs-lookup"><span data-stu-id="32ef7-194">**id**</span></span> <br/> |<span data-ttu-id="32ef7-195">ユーザーの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="32ef7-195">The unique ID of the user.</span></span> <span data-ttu-id="32ef7-196">必須です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-196">Required.</span></span>  <br/> |
|<span data-ttu-id="32ef7-197">**namehint**</span><span class="sxs-lookup"><span data-stu-id="32ef7-197">**nameHint**</span></span> <br/> |<span data-ttu-id="32ef7-198">フィードアイテムに表示する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="32ef7-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="32ef7-199">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="32ef7-200">**profileurl**</span><span class="sxs-lookup"><span data-stu-id="32ef7-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="32ef7-201">ユーザーの名前が存在する場合に、フィードアイテムでのユーザー名のハイパーリンクとして使用される個人のプロファイルの URL。</span><span class="sxs-lookup"><span data-stu-id="32ef7-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="32ef7-202">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="32ef7-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="32ef7-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="32ef7-204">このユーザーの連絡先情報を Outlook で更新するために使用される電子メールアドレス。</span><span class="sxs-lookup"><span data-stu-id="32ef7-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="32ef7-205">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="32ef7-206">textvariable</span><span class="sxs-lookup"><span data-stu-id="32ef7-206">textVariable</span></span>

|<span data-ttu-id="32ef7-207">**要素**</span><span class="sxs-lookup"><span data-stu-id="32ef7-207">**Element**</span></span>|<span data-ttu-id="32ef7-208">**説明**</span><span class="sxs-lookup"><span data-stu-id="32ef7-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32ef7-209">**name**</span><span class="sxs-lookup"><span data-stu-id="32ef7-209">**name**</span></span> <br/> |<span data-ttu-id="32ef7-210">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="32ef7-210">The name of the variable.</span></span> <span data-ttu-id="32ef7-211">必須です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-211">Required.</span></span>  <br/> |
|<span data-ttu-id="32ef7-212">**value**</span><span class="sxs-lookup"><span data-stu-id="32ef7-212">**value**</span></span> <br/> |<span data-ttu-id="32ef7-213">表示するテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="32ef7-213">The text to display.</span></span> <span data-ttu-id="32ef7-214">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="32ef7-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32ef7-215">関連項目</span><span class="sxs-lookup"><span data-stu-id="32ef7-215">See also</span></span>

- [<span data-ttu-id="32ef7-216">アクティビティフィードアイテムの XML の概要</span><span class="sxs-lookup"><span data-stu-id="32ef7-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="32ef7-217">activitydetails 要素</span><span class="sxs-lookup"><span data-stu-id="32ef7-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="32ef7-218">activitytemplatecontainer 要素</span><span class="sxs-lookup"><span data-stu-id="32ef7-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="32ef7-219">アクティビティを適切に表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="32ef7-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="32ef7-220">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="32ef7-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="32ef7-221">Outlook Social Connector プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="32ef7-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="32ef7-222">.osc XML スキーマを使用してプロバイダーを開発する</span><span class="sxs-lookup"><span data-stu-id="32ef7-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

