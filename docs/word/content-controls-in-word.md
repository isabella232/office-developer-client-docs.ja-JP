---
title: Word におけるコンテンツ コントロール
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
keywords:
- コンテンツ コントロール [Word],コンテンツ コントロール [Word],新機能
ms.assetid: c0e6dd3b-fae1-453d-a9b4-7f456b5172db
description: Microsoft Word 2013 のコンテンツ コントロールによって、どのように構造化文書のシナリオの幅が広がるかについて説明します。
localization_priority: Priority
ms.openlocfilehash: 4234425cc8398d87b72108d389953fc0eb802c87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358681"
---
# <a name="content-controls-in-word"></a><span data-ttu-id="0cf8a-104">Word におけるコンテンツ コントロール</span><span class="sxs-lookup"><span data-stu-id="0cf8a-104">Content controls in Word</span></span>

<span data-ttu-id="0cf8a-105">Microsoft Word 2013 のコンテンツ コントロールによって、どのように構造化文書のシナリオの幅が広がるかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-105">Learn how Microsoft Word 2013 content controls enable a larger range of structured document scenarios.</span></span>

<span data-ttu-id="0cf8a-106">このトピックでは、Microsoft Word 2013 のコンテンツ コントロールに加えられた変更点と、それらの変更内容によって可能になる文書のシナリオについて取り上げます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-106">This topic provides information about changes to content controls in Microsoft Word 2013 and the document scenarios that those changes enable.</span></span>
  
### <a name="structured-documents"></a><span data-ttu-id="0cf8a-107">構造化文書</span><span class="sxs-lookup"><span data-stu-id="0cf8a-107">Structured documents</span></span>
<span data-ttu-id="0cf8a-108"><a name="WordCC_StructuredDocs"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-108"></span></span>

<span data-ttu-id="0cf8a-109">構造化文書とは、文書上でコンテンツを配置できる場所や、文書に含めることのできるコンテンツの種類、コンテンツを編集できるかどうかを管理できる文書のことです。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-109">Structured documents are documents that control where content can appear on a document, what kind of content can appear in the document, and whether that content can be edited.</span></span>
  
<span data-ttu-id="0cf8a-110">Microsoft Word の構造化コンテンツが求められる一般的なシナリオのいくつかを次に示します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-110">Here are some common scenarios for structured content in Microsoft Word:</span></span>
  
- <span data-ttu-id="0cf8a-111">法律事務所で、ユーザーが変更してはならない法律用語が含まれている文書を作成する。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-111">A legal firm needs to create documents that contain legal language that should not be changed by the user.</span></span>
    
- <span data-ttu-id="0cf8a-112">企業で、タイトル、作成者、日付だけをユーザーが入力する提案書の表紙を作成する。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-112">A business needs to create a proposal cover page where only the title, author, and date are entered by the user.</span></span>
    
- <span data-ttu-id="0cf8a-113">企業で、事前に定義された場所に顧客データが入った請求書を作成する。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-113">A business needs to create invoices where the customer data is included in the invoice at predefined regions.</span></span>
    
### <a name="using-content-controls-to-structure-a-document"></a><span data-ttu-id="0cf8a-114">コンテンツ コントロールを使用して文書を構造化する</span><span class="sxs-lookup"><span data-stu-id="0cf8a-114">Using content controls to structure a document</span></span>
<span data-ttu-id="0cf8a-115"><a name="WordCC_StructuredDocs"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-115"></span></span>

<span data-ttu-id="0cf8a-116">コンテンツ コントロールとは、文書内の特定のコンテンツ用のコンテナーとして機能する Microsoft Word のエンティティのことです。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-116">Content controls are Microsoft Word entities that act as containers for specific content in a document.</span></span> <span data-ttu-id="0cf8a-117">それぞれのコンテンツ コントロールには、日付、リスト、書式設定された段落などを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-117">Individual content controls can contain content such as dates, lists, or paragraphs of formatted text.</span></span> <span data-ttu-id="0cf8a-118">コンテンツ コントロールは、リッチな構造化されたコンテンツ ブロックを作成する際に役立つものであり、構造化されたドキュメントを作成するために、適切に定義されたブロックを文書に挿入するテンプレートでの使用を意図しています。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-118">Content controls help you to create rich, structured blocks of content and are designed for use in templates that insert well-defined blocks into your documents, creating structured documents.</span></span>
  
<span data-ttu-id="0cf8a-119">コンテンツ コントロールは、コンテンツの位置を固定したり、コンテンツの種類を指定したり (日付、画像、テキストなど)、編集を許可または禁止したり、コンテンツにセマンティックな意味を付与したりするため、構造化文書の作成に最適です。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-119">Content controls are ideal for creating structured documents because content controls help you fix the position of content, specify the kind of content (for example, a date, a picture, or text), restrict or enable editing, and add semantic meaning to content.</span></span>
  
### <a name="content-controls-in-word-2010"></a><span data-ttu-id="0cf8a-120">Word 2010 のコンテンツ コントロール</span><span class="sxs-lookup"><span data-stu-id="0cf8a-120">Content controls in Word 2010</span></span>
<span data-ttu-id="0cf8a-121"><a name="WordCC_StructuredDocs"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-121"></span></span>

<span data-ttu-id="0cf8a-122">Word 2010 では、次のコンテンツ コントロールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-122">The following content controls are available in Word 2010:</span></span>
  
- <span data-ttu-id="0cf8a-123">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="0cf8a-123">Rich Text</span></span>
    
- <span data-ttu-id="0cf8a-124">プレーン テキスト</span><span class="sxs-lookup"><span data-stu-id="0cf8a-124">Plain Text</span></span>
    
- <span data-ttu-id="0cf8a-125">画像</span><span class="sxs-lookup"><span data-stu-id="0cf8a-125">Picture</span></span>
    
- <span data-ttu-id="0cf8a-126">文書パーツ ギャラリー</span><span class="sxs-lookup"><span data-stu-id="0cf8a-126">Building Block Gallery</span></span>
    
- <span data-ttu-id="0cf8a-127">コンボ ボックス</span><span class="sxs-lookup"><span data-stu-id="0cf8a-127">Combo Box</span></span>
    
- <span data-ttu-id="0cf8a-128">ドロップダウン リスト</span><span class="sxs-lookup"><span data-stu-id="0cf8a-128">Drop-Down List</span></span>
    
- <span data-ttu-id="0cf8a-129">日付</span><span class="sxs-lookup"><span data-stu-id="0cf8a-129">Date</span></span>
    
- <span data-ttu-id="0cf8a-130">チェックボックス</span><span class="sxs-lookup"><span data-stu-id="0cf8a-130">Checkbox</span></span>
    
- <span data-ttu-id="0cf8a-131">グループ</span><span class="sxs-lookup"><span data-stu-id="0cf8a-131">Group</span></span>
    
<span data-ttu-id="0cf8a-132">Word 2010 のコンテンツ コントロールにより、さまざまな構造化文書ソリューションの可能性に対応できますが、Word 2013 のコンテンツ コントロールでは、それよりも広範囲なシナリオに対応できます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-132">Word 2010 content controls enable various potential structured document solutions, but in Word 2013 content controls enable a greater range of scenarios.</span></span>
  
## <a name="content-control-improvements-in-word-2013"></a><span data-ttu-id="0cf8a-133">Word 2013 におけるコンテンツ コントロールの機能強化</span><span class="sxs-lookup"><span data-stu-id="0cf8a-133">Content control improvements in Word 2013</span></span>
<span data-ttu-id="0cf8a-134"><a name="WordCC_WhatsNew"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-134"></span></span>

<span data-ttu-id="0cf8a-135">Word 2013 では、コンテンツ コントロールに 3 つの主要な機能強化が加えられました。その内容は、視覚化の改善、リッチ テキスト コンテンツ コントロールの XML マッピングのサポート、新しい繰り返しコンテンツ用のコンテンツ コントロールです。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-135">In Word 2013, content controls provide three key improvements: improved visualization, support for XML Mapping for Rich Text content controls, and a new content control for repeating content.</span></span>
  
### <a name="improved-visualization"></a><span data-ttu-id="0cf8a-136">視覚化の改善</span><span class="sxs-lookup"><span data-stu-id="0cf8a-136">Improved visualization</span></span>

<span data-ttu-id="0cf8a-137">Word 2013 では、次の 3 つの状態のいずれかで個々のコンテンツ コントロールを表示できます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-137">Word 2013 allows an individual content control to appear in one of three possible states:</span></span>
  
- <span data-ttu-id="0cf8a-138">境界ボックス</span><span class="sxs-lookup"><span data-stu-id="0cf8a-138">Bounding box</span></span>
    
- <span data-ttu-id="0cf8a-139">開始/終了タグ</span><span class="sxs-lookup"><span data-stu-id="0cf8a-139">Start/End tags</span></span>
    
- <span data-ttu-id="0cf8a-140">なし</span><span class="sxs-lookup"><span data-stu-id="0cf8a-140">None</span></span>
    
> [!NOTE]
> <span data-ttu-id="0cf8a-141">特に明記されていない限り、このセクションでは、文書が [**デザイン モード**] で表示されていない場合のコンテンツ コントロールの視覚化について取り上げます。コンテンツ コントロールの表示モードは、[**コンテンツ コントロールのプロパティ**] ダイアログ ボックスの [**表示方法**] ドロップダウン リスト コントロールを使用して設定します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-141">If not stated otherwise, this section discusses the visualization of content controls when the document is not viewed in **Design Mode**.You set the display mode for a content control by using the **Show as** drop-down list control in the **Content Control Properties** dialog box.</span></span> 
  
<span data-ttu-id="0cf8a-142">**図 1. ［コンテンツ コントロールのプロパティ］ ダイアログ ボックス**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-142">**Figure 1. Content Control Properties dialog box**</span></span>

<span data-ttu-id="0cf8a-143">![コンテンツ コントロールのプロパティ ダイアログ ボックス](media/DK2_WordCC_Fig01.jpg "コンテンツ コントロールのプロパティ ダイアログ ボックス")</span><span class="sxs-lookup"><span data-stu-id="0cf8a-143">![Content control properties dialog box](media/DK2_WordCC_Fig01.jpg "Content control properties dialog box")</span></span>
  
<span data-ttu-id="0cf8a-144">コンテンツ コントロールの表示モードは、Word 2013 オブジェクト モデル (「[新しい Word 2013 のコンテンツ コントロール オブジェクト モデルのメンバー](#WordCC_NewOM)」で後述) を使用して設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-144">You can also set the display mode for a content control by using the Word 2013 object model (discussed later in [New Word 2013 content control object model members](#WordCC_NewOM)).</span></span>
  
### <a name="bounding-box"></a><span data-ttu-id="0cf8a-145">境界ボックス</span><span class="sxs-lookup"><span data-stu-id="0cf8a-145">Bounding box</span></span>
<span data-ttu-id="0cf8a-146"><a name="WordCC_DefaultRendering"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-146"></span></span>

<span data-ttu-id="0cf8a-147">Word 2013 のコンテンツ コントロールの既定の表示形式は、Word 2007 および Word 2010 のコンテンツ コントロールの表示と同じ境界ボックスとしての外観が維持されています。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-147">The default rendering for content controls in Word 2013 is to preserve the look of content controls as they appear in Word 2007 and Word 2010; that is, as a bounding box.</span></span> <span data-ttu-id="0cf8a-148">コンテンツ コントロールを **[境界ボックス]** として表示するように設定すると、次のユーザー操作によって表示が変化します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-148">When a content control is set to show as **Bounding Box**, the display changes depending upon the following user interaction:</span></span>
  
- <span data-ttu-id="0cf8a-149">コンテンツ コントロールにフォーカスがないときには視覚化されません</span><span class="sxs-lookup"><span data-stu-id="0cf8a-149">When the content control does not have the focus, no visualization occurs</span></span>
    
- <span data-ttu-id="0cf8a-150">マウスを置くと、コンテンツ コントロールは影付きの四角形として表示されます</span><span class="sxs-lookup"><span data-stu-id="0cf8a-150">On mouse-over, the content control appears as a shaded rectangle</span></span>
    
<span data-ttu-id="0cf8a-151">**図 2. マウスを置いたときのコンテンツ コントロール**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-151">**Figure 2. Content control on mouse-over**</span></span>

<span data-ttu-id="0cf8a-152">![マウスを置いたときのコンテンツ コントロール](media/DK2_WordCC_Fig02.jpg "マウスを置いたときのコンテンツ コントロール")</span><span class="sxs-lookup"><span data-stu-id="0cf8a-152">![Content control on mouse over](media/DK2_WordCC_Fig02.jpg "Content control on mouse over")</span></span>
  
- <span data-ttu-id="0cf8a-153">コンテンツ コントロールにフォーカスがある場合 (ユーザーがコンテンツ コントロールを選択した場合)、コントロールが「境界ボックス」として表示されます （コンテンツで線で囲まれ、タイトルを設定した場合にはそのタイトルが表示されます）</span><span class="sxs-lookup"><span data-stu-id="0cf8a-153">When the content control has the focus (when the user chooses the content control), the control appears as a "bounding box" (with a line around the content and the title showing, if a title has been set)</span></span>
    
<span data-ttu-id="0cf8a-154">**図 3. フォーカスがあるコンテンツ コントロール**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-154">**Figure 3. Content control with focus**</span></span>

<span data-ttu-id="0cf8a-155">![フォーカスがあるコンテンツ コントロール](media/DK2_WordCC_Fig03.jpg "フォーカスがあるコンテンツ コントロール")</span><span class="sxs-lookup"><span data-stu-id="0cf8a-155">![Content control with focus](media/DK2_WordCC_Fig03.jpg "Content control with focus")</span></span>
  
### <a name="startend-tags"></a><span data-ttu-id="0cf8a-156">開始/終了タグ</span><span class="sxs-lookup"><span data-stu-id="0cf8a-156">Start/End tags</span></span>
<span data-ttu-id="0cf8a-157"><a name="WordCC_StartEndTags"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-157"></span></span>

<span data-ttu-id="0cf8a-158">コンテンツ コントロールを ［**開始/終了タグ**］ として表示するように設定すると、ユーザー操作に関係なくタグが表示され、タイトルは表示されません。ただし、［**ドロップダウン リスト**］ ボタンなどのボタンは、マウスと置くと表示されます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-158">When the content control is set to show as **Start/End tag**, the tags are displayed regardless of user interaction, and the title never appears; but buttons, such as the **Drop-Down List** button, appear on mouse over.</span></span> 
  
<span data-ttu-id="0cf8a-159">**図 4. ［開始/終了タグ］ として表示するよう設定されているコンテンツ コントロール**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-159">**Figure 4. Content control set to show as start/end tags**</span></span>

<span data-ttu-id="0cf8a-160">![開始タグと終了タグとして表されるように設定されたコンテンツ コントロール](media/DK2_WordCC_Fig04.jpg "開始タグと終了タグとして表されるように設定されたコンテンツ コントロール")</span><span class="sxs-lookup"><span data-stu-id="0cf8a-160">![Content control set to show as start and end tags](media/DK2_WordCC_Fig04.jpg "Content control set to show as start and end tags")</span></span>
  
### <a name="none"></a><span data-ttu-id="0cf8a-161">なし</span><span class="sxs-lookup"><span data-stu-id="0cf8a-161">None</span></span>
<span data-ttu-id="0cf8a-162"><a name="WordCC_Invisible"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-162"></span></span>

<span data-ttu-id="0cf8a-163">コンテンツ コントロールを **［なし］** として表示するように設定すると、コンテンツ コントロールは表示されません。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-163">When the content control is set to show as **None**, the content control is not displayed.</span></span>
  
### <a name="content-control-colorization"></a><span data-ttu-id="0cf8a-164">コンテンツ コントロールの色</span><span class="sxs-lookup"><span data-stu-id="0cf8a-164">Content control colorization</span></span>
<span data-ttu-id="0cf8a-165"><a name="WordCC_CCColorization"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-165"></span></span>

<span data-ttu-id="0cf8a-166">コンテンツ コントロールに対する各種の表示が可能なことに加えて、Word 2013 では個別のコンテンツ コントロールの色を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-166">In addition to enabling a different kind of display for a content control, Word 2013 also helps you to set the color for an individual content control.</span></span> <span data-ttu-id="0cf8a-167">コンテンツ コントロールの色を設定するには、**[コンテンツ コントロールのプロパティ]** ダイアログ ボックスの **[色]** ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-167">You set the color of a content control by using the **Color** button in the **Content Control Properties** dialog box.</span></span> 
  
<span data-ttu-id="0cf8a-168">また、コンテンツ コントロールの色は、Word 2013 オブジェクト モデル (「[新しい Word 2013 のコンテンツ コントロール オブジェクト モデルのメンバー](#WordCC_NewOM)」で後述) を使用して設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-168">You can also set the color of a content control by using the Word 2013 object model (discussed later in [New Word 2013 content control object model members](#WordCC_NewOM)).</span></span>
  
<span data-ttu-id="0cf8a-169">**図 5. ［コンテンツ コントロールのプロパティ］ ダイアログ ボックス**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-169">**Figure 5. Content Control Properties dialog box**</span></span>

<span data-ttu-id="0cf8a-170">![コンテンツ コントロールのプロパティ ダイアログ ボックス](media/DK2_WordCC_Fig05.jpg "コンテンツ コントロールのプロパティ ダイアログ ボックス")</span><span class="sxs-lookup"><span data-stu-id="0cf8a-170">![Content control properties dialog box](media/DK2_WordCC_Fig05.jpg "Content control properties dialog box")</span></span>
  
### <a name="support-for-xml-mapping-for-rich-text-content-controls"></a><span data-ttu-id="0cf8a-171">リッチ テキスト コンテンツ コントロールの XML マッピングのサポート</span><span class="sxs-lookup"><span data-stu-id="0cf8a-171">Support for XML mapping for rich text content controls</span></span>
<span data-ttu-id="0cf8a-172"><a name="WordCC_XMLMapping"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-172"></span></span>

<span data-ttu-id="0cf8a-173">Word 2013 では、リッチ テキスト コンテンツ コントロールと文書パーツ コンテンツ コントロールのコンテンツを XML データ ストアにマップできます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-173">Word 2013 helps you to map the content of rich text content controls and document building block content controls to the XML data store.</span></span> <span data-ttu-id="0cf8a-174">そうするには、コンテンツ コントロールの *XML マッピング*を設定します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-174">To do this, you set the  *XML mapping*  for the content control.</span></span> <span data-ttu-id="0cf8a-175">このプロパティは、オブジェクト モデルにある **XMLMapping.SetMapping** メソッドを使用して設定します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-175">You can set this property by using the existing **XMLMapping.SetMapping** method in the object model.</span></span> <span data-ttu-id="0cf8a-176">カスタム XML パーツ内では、カスタム XML が文字列に変換されたフラットな Open XML マークアップ (標準 XML エンコーディングを使用) として保存されます。これにより、カスタム XML はカスタム XML パーツのテキスト ノードとして保存できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-176">Within the custom XML part, the custom XML is stored as flat Open XML markup converted into a string (by using standard XML encoding), so that it can be stored as a text node in the custom XML part.</span></span> <span data-ttu-id="0cf8a-177">ただし、マッピングには、リーフ ノードまたは属性へのマッピングのみが成功するという以前からの制限があります。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-177">However, the mapping continues to have the limitation that it can only successfully map to leaf nodes or attributes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0cf8a-p105">リッチ テキスト コンテンツ コントロールに他のリッチ テキスト コンテンツ コントロールを含めることはできません。(ファイル形式の操作やコピーと貼り付けなどによって) リッチ コンテキスト コンテンツ コントロールが別のリッチ コンテキスト コントロールの中に入ると、それはマップされたリッチ テキスト コントロールの中に含まれなくなるまでリンク解除されます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-p105">Rich text content controls cannot contain other rich text content controls. If one exists inside of another (for example, because of file format manipulation, copy and paste, and so on), it is unlinked until it is no longer contained inside a mapped rich text control.</span></span> 
  
<span data-ttu-id="0cf8a-180">XML マッピングの設定方法について詳しくは、このトピックで後述する「[新しい Word 2013 のコンテンツ コントロール オブジェクト モデルのメンバー](#WordCC_NewOM)」というセクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-180">For more information about how to set up XML mapping, see the section [New Word 2013 content control object model members](#WordCC_NewOM) later in this topic.</span></span> 
  
### <a name="supporting-repeating-content"></a><span data-ttu-id="0cf8a-181">繰り返しコンテンツのサポート</span><span class="sxs-lookup"><span data-stu-id="0cf8a-181">Supporting repeating content</span></span>
<span data-ttu-id="0cf8a-182"><a name="WordCC_SupportingRepeating"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-182"></span></span>

<span data-ttu-id="0cf8a-183">表示の機能拡張とリッチ テキスト コンテンツ コントロールへの XML マッピングのサポートに加えて、Word 2013 には、コンテンツの繰り返しが可能になる新しいコンテンツ コントロールも追加されています。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-183">In addition to visualization enhancements and support for XML mapping to rich text content controls, Word 2013 also adds a new content control that enables you to repeat content.</span></span> <span data-ttu-id="0cf8a-184">繰り返しセクション コンテンツ コントロールにより、そのコントロールに含まれている (別のコンテンツ コントロールを含んでいる) コンテンツを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-184">The repeating section content control repeats the content contained within it, including other content controls.</span></span>
  
<span data-ttu-id="0cf8a-p107">段落全体や表の行の周囲に繰り返しセクション コンテンツ コントロールを挿入します。あるセクションをこのコントロールで囲むと、中に含まれているセクションの上または下にそのセクションのコピーを挿入できます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-p107">You insert the repeating section content control around entire paragraphs or table rows. Once the control surrounds a section, you can insert copies of the section above or below the contained section.</span></span>
  
<span data-ttu-id="0cf8a-187">**図 6. 繰り返しセクション コンテンツ コンソールのコンテキスト メニュー**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-187">**Figure 6. Repeating section content control context menu**</span></span>

<span data-ttu-id="0cf8a-188">![繰り返しセクション コンテンツ コンソールのコンテキスト](media/DK2_WordCC_Fig06.jpg "繰り返しセクション コンテンツ コンソールのコンテキスト")</span><span class="sxs-lookup"><span data-stu-id="0cf8a-188">![Repeating section content control context](media/DK2_WordCC_Fig06.jpg "Repeating section content control context")</span></span>
  
<span data-ttu-id="0cf8a-189">挿入されたセクションの繰り返しは、コンテンツ コントロールの末尾のコントロール (プラス記号の付いたボタンとして表示されます (![プラス記号](media/DK2_WordCC_Fig06A.jpg "プラス記号"))) を使用するか、コンテキスト メニューのコマンド (図 6 を参照) を選択することで可能です。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-189">You can repeat the inserted section by using either the control on the end of the content control (displayed as a button with a plus sign (![Plus sign](media/DK2_WordCC_Fig06A.jpg "Plus sign"))) or by choosing a command on the context menu, as shown in Figure 6.</span></span> <span data-ttu-id="0cf8a-190">繰り返されるコンテンツは、個別のコンテンツのセクションになります。このセクションには、**[コンテンツ コントロールのプロパティ]** ダイアログ ボックスを使用してタイトルを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-190">The repeated content becomes a separate section of the control that you can assign a title by using the **Content Control Properties** dialog box.</span></span> 
  
<span data-ttu-id="0cf8a-191">**図 7. [コンテンツ コントロールのプロパティ] ダイアログ ボックスによるセクション タイトルの割り当**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-191">**Figure 7. Assign a section title in the Content Control Properties dialog box**</span></span>

<span data-ttu-id="0cf8a-192">![コンテンツ コントロールのプロパティ ダイアログ ボックス](media/DK2_WordCC_Fig07.jpg "コンテンツ コントロールのプロパティ ダイアログ ボックス")</span><span class="sxs-lookup"><span data-stu-id="0cf8a-192">![Content control properties dialog box](media/DK2_WordCC_Fig07.jpg "Content control properties dialog box")</span></span>
  
<span data-ttu-id="0cf8a-193">セクションにタイトルを指定した場合に [**コンテンツ コントロールのプロパティ**] ダイアログ ボックスの [**他のユーザーがセクションを追加したり削除したりすることを許可する**] を選択すると、ユーザーは名前で選択対象を追加または削除できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-193">Once you have given the section a title, if you select **Allow users to add and remove sections** in the **Content Control Properties** dialog box, users can add or delete the section by name.</span></span> 
  
<span data-ttu-id="0cf8a-194">**図 8. 繰り返しセクション コンテンツ コントロールのコンテキスト メニューによるセクションの削除**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-194">**Figure 8. Use the repeating section content control context menu to delete a section**</span></span>

<span data-ttu-id="0cf8a-195">![繰り返しセクション コンテンツ コンソールのコンテキスト](media/DK2_WordCC_Fig08.jpg "繰り返しセクション コンテンツ コンソールのコンテキスト")</span><span class="sxs-lookup"><span data-stu-id="0cf8a-195">![Repeating section content control context](media/DK2_WordCC_Fig08.jpg "Repeating section content control context")</span></span>
  
<span data-ttu-id="0cf8a-p109">繰り返しセクション コンテンツ コントロールで他のコンテンツ コントロールを囲むと、中に含まれたコンテンツ コントロールは新しいアイテムごとに繰り返されます。ただし、そのようなコンテンツ コントロールのコンテンツはプレースホルダー テキストにリセットされます。以下の 2 つの例外の場合には子コントロール コンテンツが保持されます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-p109">When a repeating section content control surrounds other content controls, the enclosed content controls are repeated in each new item; but any such content controls have their contents reset to placeholder text. There are two exceptions where child control contents are preserved:</span></span> 
  
- <span data-ttu-id="0cf8a-198">子コントロールが繰り返しセクション コントロールの場合。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-198">When a child control is a repeating section control.</span></span>
    
- <span data-ttu-id="0cf8a-199">子コントロールが、繰り返しセクション コンテンツ コントロール外のノードに XML マッピングされている場合。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-199">When a child control is XML-mapped to a node outside the repeating section content control.</span></span>
    
<span data-ttu-id="0cf8a-200">**図 9. 繰り返しの前に子コントロールが含まれる繰り返しセクション コンテンツ コントロール**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-200">**Figure 9. Repeating section content control containing child controls before repeat**</span></span>

<span data-ttu-id="0cf8a-201">![繰り返しの前に子コントロールが含まれる繰り返しセクション コンテンツ コントロール](media/DK2_WordCC_Fig09.jpg "繰り返しの前に子コントロールが含まれる繰り返しセクション コンテンツ コントロール")</span><span class="sxs-lookup"><span data-stu-id="0cf8a-201">![Repeating section content control before repeat](media/DK2_WordCC_Fig09.jpg "Repeating section content control before repeat")</span></span>
  
<span data-ttu-id="0cf8a-202">**図 10. 繰り返しの後に子コントロールが含まれる繰り返しセクション コンテンツ コントロール**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-202">**Figure 10. Repeating section content control containing child controls after repeat**</span></span>

<span data-ttu-id="0cf8a-203">![繰り返しの後に子コントロールが含まれる繰り返しセクション コンテンツ コントロール](media/DK2_WordCC_Fig10.jpg "繰り返しの後に子コントロールが含まれる繰り返しセクション コンテンツ コントロール")</span><span class="sxs-lookup"><span data-stu-id="0cf8a-203">![Repeating section content control after repeat](media/DK2_WordCC_Fig10.jpg "Repeating section content control after repeat")</span></span>
  
### <a name="repeating-section-content-controls-around-xml-mapped-controls"></a><span data-ttu-id="0cf8a-204">XML マッピング コントロールを囲む繰り返しセクション コンテンツ コントロール</span><span class="sxs-lookup"><span data-stu-id="0cf8a-204">Repeating section content controls around XML-mapped controls</span></span>
<span data-ttu-id="0cf8a-205"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-205"></span></span>

<span data-ttu-id="0cf8a-206">Word 2013 は、繰り返しセクションに含まれている XML マッピングを次のようにマップします。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-206">For XML mappings that are contained in a repeating section, Word 2013 maps them as follows.</span></span>
  
<span data-ttu-id="0cf8a-207">マッピングがその親チェーンの一部としてノード セット内のアイテムと重ならない場合、バインディングは「絶対バインディング」となり、すべての繰り返しセクション アイテム内で同じコンテンツが示されます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-207">If the mapping does not intersect with an item in the node set as part of its parent chain, the binding is an "absolute binding" and shows the same content in all repeating section items.</span></span>
  
<span data-ttu-id="0cf8a-208">マッピングがその親チェーンの一部としてノード セット内のアイテムと重なる場合、バインディングは「相対バインディング」となり、次のように再マップされます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-208">If the mapping does intersect with an item in the node set as part of its parent chain, the binding is a "relative binding", and is remapped as follows:</span></span>
  
- <span data-ttu-id="0cf8a-209">ノードの絶対バインディングが判別されます (クエリ式はすべて平坦化されます) - これは最初のマッピングで生じます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-209">The absolute binding for the node is determined (flattening out any query expressions)─this should happen on initial mapping</span></span>
    
- <span data-ttu-id="0cf8a-210">ノード セットと重なるバインディングの軸が削除されます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-210">The axis of the binding that intersects with the node set is removed</span></span>
    
- <span data-ttu-id="0cf8a-211">残りの XPath が、繰り返しセクション コンテンツ アイテムの XPath に基づいて相対評価されます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-211">The remainder of the XPath is evaluated relative to the XPath of the repeating section content item</span></span>
    
<span data-ttu-id="0cf8a-212">たとえば、次のマッピングが生じるとします。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-212">For example, the following mappings might occur:</span></span>
  
- <span data-ttu-id="0cf8a-213">繰り返しセクションが \root\next\path にマップされます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-213">The repeating section is mapped to \root\next\path</span></span>
    
- <span data-ttu-id="0cf8a-214">サンプル アイテム内のコントロールが \root\next\path[2]\baz にマップされます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-214">The control in the sample item is mapped to \root\next\path[2]\baz</span></span>
    
- <span data-ttu-id="0cf8a-215">Word が \root\next\path[2] をノード セット内のアイテムに対応付けます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-215">Word matches \root\next\path[2] to an item in the node set</span></span>
    
<span data-ttu-id="0cf8a-216">結果としてバインディングは .\baz として評価されます。この場合、繰り返しコンテンツ アイテムのノードが基準となります。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-216">The binding is therefore evaluated as .\baz, where the base is the node of the repeating content item.</span></span>
  
<span data-ttu-id="0cf8a-217">繰り返しコンテンツ コントロールを処理する際、データの損失を避けて障害を防止するには以下の提案が役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-217">The following suggestions for working with repeating content controls can help you prevent data loss and avoid frustration.</span></span>
  
### <a name="working-with-repeating-section-content-controls-that-are-mapped-to-xml-data"></a><span data-ttu-id="0cf8a-218">XML データにマップされる繰り返しセクション コンテンツ コントロールを扱う</span><span class="sxs-lookup"><span data-stu-id="0cf8a-218">Working with repeating section content controls that are mapped to XML data</span></span>
<span data-ttu-id="0cf8a-219"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-219"></span></span>

<span data-ttu-id="0cf8a-220">XML データにマップされた繰り返しセクション コンテンツ コントロールを挿入すると、ユーザーが文書を再度開くたびに、データ ストアの情報に基づいて、繰り返しセクションのアイテムが Word によって繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-220">If you insert a repeating section content control that is mapped to XML data, every time your user reopens the document, Word recreates the repeating section items, based on the information in the data store.</span></span> <span data-ttu-id="0cf8a-221">文書を保存しても、ユーザーがドキュメントの繰り返しセクションのアイテムに行った変更がデータ ストアにもマップされていないと、その変更内容は失われます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-221">Even if you save the document, any changes that the user makes in the repeating section items in the document that aren't also mapped into the data store are lost.</span></span>
  
<span data-ttu-id="0cf8a-222">この事態が生じないようにするには、繰り返しセクション コンテンツ コントロールをロックし、同じように XML にマップされる、ロックされていない子コンテンツ コントロールでのみユーザーが編集を行えるようにします。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-222">To help prevent this from happening, lock the repeating section content control and allow the user to edit only in unlocked child content controls that are mapped to the XML as well.</span></span>
  
### <a name="binding-a-repeating-section-content-control-to-a-table"></a><span data-ttu-id="0cf8a-223">繰り返しセクション コンテンツ コントロールを表にバインドする</span><span class="sxs-lookup"><span data-stu-id="0cf8a-223">Binding a repeating section content control to a table</span></span>
<span data-ttu-id="0cf8a-224"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-224"></span></span>

<span data-ttu-id="0cf8a-225">繰り返しセクション コンテンツ コントロールを表にバインドする場合は、表を挿入した*後*、繰り返しセクション コンテンツ コントロールを挿入するようにします。この順序は逆にしないでください </span><span class="sxs-lookup"><span data-stu-id="0cf8a-225">If you want to bind a repeating section content control to a table, insert the table and  *then*  the insert repeating section content control, and not the other way around.</span></span> <span data-ttu-id="0cf8a-226">(逆にすると、表だけを選択することができなくなります)。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-226">(Otherwise, you won't be able to select only the table).</span></span> 
  
### <a name="nesting-repeating-section-content-controls-within-a-table"></a><span data-ttu-id="0cf8a-227">繰り返しセクション コンテンツ コントロールを表の中に入れ子にする</span><span class="sxs-lookup"><span data-stu-id="0cf8a-227">Nesting repeating section content controls within a table</span></span>
<span data-ttu-id="0cf8a-228"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-228"></span></span>

<span data-ttu-id="0cf8a-229">繰り返しセクション コンテンツ コントロールを表の中に隣接して入れ子にする場合 (たとえば、親の繰り返しセクション コンテンツ コントロールの最後と子繰り返しセクション コンテンツ コントロールが同じセル内にある場合)、内部セクションでアイテムを追加したり削除したりすると、外部繰り返しセクションが削除されます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-229">Nesting repeating section content controls tightly within a table (for example, when the end of the parent and child repeating section content control is in the same cell) causes the outer repeating section to be deleted when the inner section has an item added or removed.</span></span>
  
<span data-ttu-id="0cf8a-p112">この事態が生じるのを避けるには、繰り返しセクション コンテンツ コントロールの最後と次の繰り返しセクション コンテンツ コントロール間に段落記号を追加できます。段落記号を非表示にするには、リボンの [**ホーム**] タブの [**表示/非表示**] オプションの選択を解除します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-p112">You can prevent this from happening by adding a paragraph marker between the end of one repeating section content control and the next. To hide the paragraph marker, deselect the **Show/Hide** option on the **Home** tab of the ribbon.</span></span> 
  
### <a name="open-xml-file-format-schema-additions"></a><span data-ttu-id="0cf8a-232">Open XML ファイル形式スキーマにおける追加内容</span><span class="sxs-lookup"><span data-stu-id="0cf8a-232">Open XML File Format schema additions</span></span>
<span data-ttu-id="0cf8a-233"><a name="WordCC"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-233"></span></span>

<span data-ttu-id="0cf8a-234">WordprocessingML Open XML ファイル形式スキーマに次の要素が追加されました。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-234">The following elements were added to the WordprocessingML Open XML File Format schema.</span></span>
  
<span data-ttu-id="0cf8a-235">**表 1. コンテンツ コントロール用 WordprocessingML Open XML ファイル形式スキーマの新しい要素**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-235">**Table 1. New elements in the WordprocessingML Open XML File Format schema for content controls**</span></span>

|<span data-ttu-id="0cf8a-236">**要素**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-236">**Element**</span></span>|<span data-ttu-id="0cf8a-237">**説明**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-237">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cf8a-238">\<w:appearance\></span><span class="sxs-lookup"><span data-stu-id="0cf8a-238">\<w:appearance\></span></span>  <br/> |<span data-ttu-id="0cf8a-239">\<w:appearance\> は、\<w:sdtPr\> の子要素です。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-239">\<w:appearance\> is a child element of \<w:sdtPr\>.</span></span>  <br/> <span data-ttu-id="0cf8a-240">val 属性には次の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-240">The following values are valid for the val attribute:</span></span>  <br/> <span data-ttu-id="0cf8a-241">\<w:appearance val= boundingBox</span><span class="sxs-lookup"><span data-stu-id="0cf8a-241">\<w:appearance val= boundingBox</span></span>|<span data-ttu-id="0cf8a-242">tags</span><span class="sxs-lookup"><span data-stu-id="0cf8a-242">tags</span></span>|<span data-ttu-id="0cf8a-243">hidden。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-243">hidden.</span></span>  <br/> <span data-ttu-id="0cf8a-244">既定値は boundingBox です。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-244">The default value is boundingBox.</span></span>  <br/> |
|<span data-ttu-id="0cf8a-245">\<w:color\></span><span class="sxs-lookup"><span data-stu-id="0cf8a-245">\<w:color\></span></span>  <br/> |<span data-ttu-id="0cf8a-246">\<w:color\> は \<w:sdtPr\> の子要素です。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-246">\<w:color\> is a child element of \<w:sdtPr\>.</span></span>  <br/> <span data-ttu-id="0cf8a-p113">このコンテンツ モデルは、既存の CT_Color 複合型と一致します。既定値は Word 2010 で使用されている色です。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-p113">The content model matches the existing CT_Color complex type. The default value is the color used in Word 2010.</span></span>  <br/> |
   
## <a name="new-word-2013-content-control-object-model-members"></a><span data-ttu-id="0cf8a-249">新しい Word 2013 のコンテンツ コントロール オブジェクト モデルのメンバー</span><span class="sxs-lookup"><span data-stu-id="0cf8a-249">New Word 2013 content control object model members</span></span>
<span data-ttu-id="0cf8a-250"><a name="WordCC_NewOM"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-250"></span></span>

<span data-ttu-id="0cf8a-251">Word 2013 の新しい機能拡張とコンテンツ コントロールへの追加機能によって、Word のオブジェクト モデルは、新しい機能セットをプログラムで操作できるように更新されています。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-251">With the new enhancements and additions to content controls in Word 2013, the object model for Word has been updated to allow for programmatic manipulation of the new feature set.</span></span> <span data-ttu-id="0cf8a-252">さらに、ワード処理文書の基礎となる Open XML ファイル形式にも変更が加えられています。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-252">In addition, changes have also been made to the underlying Open XML File Format for word processing documents.</span></span>
  
<span data-ttu-id="0cf8a-253">次からのセクションでは、各コンテンツ コントロール機能拡張に関連する特有のオブジェクト モデルの変更内容について詳しく取り上げます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-253">The following sections provide more information about the specific object model changes related to each content control enhancement.</span></span>
  
### <a name="visualization-enhancements"></a><span data-ttu-id="0cf8a-254">視覚化の機能拡張</span><span class="sxs-lookup"><span data-stu-id="0cf8a-254">Visualization enhancements</span></span>
<span data-ttu-id="0cf8a-255"><a name="WordCC_VisEnhancements"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-255"></span></span>

<span data-ttu-id="0cf8a-256">Word 2013 に含まれている複数のオブジェクト モデル追加機能は、コンテンツ コントロールの視覚化の機能拡張に向けたものです。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-256">Several object model additions are included in Word 2013 for content control visualization enhancements.</span></span> <span data-ttu-id="0cf8a-257">次の表に、視覚化のための **ContentControl** オブジェクトの新しいメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-257">The following table list new members of the **ContentControl** object for visualization.</span></span> 
  
<span data-ttu-id="0cf8a-258">**表 2. 新しい ContentControl オブジェクトのメンバー**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-258">**Table 2. New ContentControl object members**</span></span>

|<span data-ttu-id="0cf8a-259">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-259">**Member**</span></span>|<span data-ttu-id="0cf8a-260">**説明**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-260">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cf8a-261">.</span><span class="sxs-lookup"><span data-stu-id="0cf8a-261"></span></span> <span data-ttu-id="0cf8a-262">**Appearance** (**WdContentControlAppearance** として)</span><span class="sxs-lookup"><span data-stu-id="0cf8a-262">**Appearance** as **WdContentControlAppearance**</span></span> <br/> |<span data-ttu-id="0cf8a-263">コンテンツ コントロールの視覚化を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-263">Gets or sets the visualization of the content control.</span></span>  <br/> |
|<span data-ttu-id="0cf8a-264">.</span><span class="sxs-lookup"><span data-stu-id="0cf8a-264"></span></span> <span data-ttu-id="0cf8a-265">**Color** (**WdColor** として)</span><span class="sxs-lookup"><span data-stu-id="0cf8a-265">**Color** as **WdColor**</span></span> <br/> |<span data-ttu-id="0cf8a-266">コンテンツ コントロールの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-266">Gets or sets the color of the content control.</span></span>  <br/> |
   
<span data-ttu-id="0cf8a-267">次の表に、新しい **WdContentControlAppearance** 列挙体の定数を示します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-267">The following table lists constants in the new **WdContentControlAppearance** enumeration.</span></span> 
  
<span data-ttu-id="0cf8a-268">**表 3. 新しい WdContentControlAppearance 列挙体の定数**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-268">**Table 3. New WdContentControlAppearance enumeration constants**</span></span>

|<span data-ttu-id="0cf8a-269">**定数**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-269">**Constant**</span></span>|<span data-ttu-id="0cf8a-270">**説明**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-270">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cf8a-271">**wdContentControlBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-271">**wdContentControlBoundingBox**</span></span> <br/> |<span data-ttu-id="0cf8a-272">影付きの四角形/境界ボックスとして表示されるコンテンツ コントロールを表します (オプションとしてタイトルが表示されます)。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-272">Represents a content control shown as a shaded rectangle/bounding box (with optional title).</span></span>  <br/> |
|<span data-ttu-id="0cf8a-273">**wdContentControlTags**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-273">**wdContentControlTags**</span></span> <br/> |<span data-ttu-id="0cf8a-274">開始/終了マーカーとして表示されるコンテンツ コントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-274">Represents a content control shown as start/end markers.</span></span>  <br/> |
|<span data-ttu-id="0cf8a-275">**wdContentControlHidden**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-275">**wdContentControlHidden**</span></span> <br/> |<span data-ttu-id="0cf8a-276">表示されていないコンテンツ コントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-276">Represents a content control that is not shown.</span></span>  <br/> |
   
### <a name="code-sample"></a><span data-ttu-id="0cf8a-277">コード サンプル</span><span class="sxs-lookup"><span data-stu-id="0cf8a-277">Code sample</span></span>
<span data-ttu-id="0cf8a-278"><a name="WordCC_VisEnhancements"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-278"></span></span>

<span data-ttu-id="0cf8a-279">次のコード サンプルは、プログラムを使用して、リッチ テキスト コンテンツ コントロールの作成と、視覚化の設定を行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-279">The following code sample shows how to create rich text content controls and set visualization programmatically.</span></span>
  
```vb
Sub testVisualization()
   Dim objcc As ContentControl
   Dim objRange As Range
   
   ' Get the first paragraph as a range object.
   Set objRange = ActiveDocument.Paragraphs(1).Range
   ' Create a rich text content control around the first paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Default Bounding Box"
   ' Set visualization to the default.
   objcc.Appearance = wdContentControlBoundingBox
   
   ' Create a new paragraph.
   objRange.InsertParagraphAfter
   Set objRange = ActiveDocument.Paragraphs(2).Range
   ' Create a rich text content control around the second paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Non Bounding"
   ' Set visualization to invisible.
   objcc.Appearance = wdContentControlHidden
   
   ' Create a new paragraph.
   objRange.InsertParagraphAfter
   Set objRange = ActiveDocument.Paragraphs(3).Range
   ' Create a rich text content control around the third paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Tags Only with Pink color"
   ' Set visualization to Start/End tags with pink color.
   objcc.Appearance = wdContentControlTags
   objcc.Color = wdColorPink
End Sub
```

### <a name="xml-mapping"></a><span data-ttu-id="0cf8a-280">XML マッピング</span><span class="sxs-lookup"><span data-stu-id="0cf8a-280">XML mapping</span></span>
<span data-ttu-id="0cf8a-281"><a name="WordCC_XMLMappingOM"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-281"></span></span>

<span data-ttu-id="0cf8a-282">Word 2013 オブジェクト モデルには、文書のデータ ストア内の XML ノードにリッチ テキストをマップするための追加機能はありません。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-282">No additions were made to the Word 2013 object model to accommodate rich text mapping to XML nodes in the document data store.</span></span> <span data-ttu-id="0cf8a-283">その代わりに、文書のデータ ストア内の XML ノードにリッチ テキスト コンテンツ コントロールをマップする既存のオブジェクト モデルを使用してください。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-283">Instead, use the existing object model to map a rich text content control to an XML node in the document data store.</span></span> <span data-ttu-id="0cf8a-284">また、特に XML マッピングのために新しく取り入れられたテキスト コンテンツ コントロールのサポートの一部として、基盤となる Open XML ファイル形式の WordprocessingML スキーマに加えられた変更もありません。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-284">Additionally, no changes were made to the underlying Open XML File Format WordprocessingML schema as part of the newly included rich text content control support specifically for XML mapping.</span></span>
  
#### <a name="code-sample"></a><span data-ttu-id="0cf8a-285">コード サンプル</span><span class="sxs-lookup"><span data-stu-id="0cf8a-285">Code sample</span></span>

<span data-ttu-id="0cf8a-286">以下のコード サンプルは、プログラムを使用して XML ノードにリッチ テキスト コンテンツ コントロールをマップする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-286">The following code sample shows how to map a rich text content control to an XML node programmatically.</span></span>
  
```vb
Sub testRichBinding()
   Dim objRange As Range
   Dim objcc As ContentControl
   Dim objCustomPart As CustomXMLPart
   Dim blnMap As Boolean
   
   ' Add a custom XML part to the data store.
   Set objCustomPart = ActiveDocument.CustomXMLParts.Add
   ' Load XML fragment into the custom XML part.
   objCustomPart.LoadXML ("<x>Rich Text Databinding</x>")
   ' Get the first paragraph as a range object.
   Set objRange = ActiveDocument.Paragraphs(1).Range
   ' Create a rich text content control around the first paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   ' Bind the XML node to the rich text content control.
   blnMap = objcc.XMLMapping.SetMapping("/x")
   ' Return whether mapping worked.
   MsgBox objcc.XMLMapping.IsMapped
End Sub
```

### <a name="repeating-section-content-controls-represented-in-the-object-model"></a><span data-ttu-id="0cf8a-287">オブジェクト モデルで表される繰り返しセクション コンテンツ コントロール</span><span class="sxs-lookup"><span data-stu-id="0cf8a-287">Repeating section content controls represented in the object model</span></span>
<span data-ttu-id="0cf8a-288"><a name="WordCC_RepeatingSection"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-288"></span></span>

<span data-ttu-id="0cf8a-p119">繰り返しセクション コンテンツ コントロールをオブジェクト モデルで使用できます。そのためには、以下に示されている、**ContentControl** オブジェクトに対する追加機能と、新しい **RepeatingSectionItem** オブジェクトと **RepeatingSectionItemColl** オブジェクトを使用します。表 4 に、繰り返しセクション コンテンツ コントロール用の **ContentControl** オブジェクトの新しいメンバーのうち、重要性が最も高いものをいくつか取り上げます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-p119">The repeating section content control is available in the object model by using the following additions to the **ContentControl** object and the new **RepeatingSectionItem** and **RepeatingSectionItemColl** objects. Table 4 lists the most important new members of the **ContentControl** object for repeating section content controls.</span></span> 
  
<span data-ttu-id="0cf8a-291">**表 4. ContentControl オブジェクトのメンバー**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-291">**Table 4. ContentControl object members**</span></span>

|<span data-ttu-id="0cf8a-292">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-292">**Member**</span></span>|<span data-ttu-id="0cf8a-293">**説明**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-293">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cf8a-294">**AllowInsertDeleteSection** (**Boolean** として)</span><span class="sxs-lookup"><span data-stu-id="0cf8a-294">**AllowInsertDeleteSection** as **Boolean**</span></span> <br/> |<span data-ttu-id="0cf8a-295">ユーザーが UI を使用してコンテンツ コントロールからセクションを追加または削除できるかどうかを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-295">Gets or sets whether users can add or remove sections from the content control by using the UI.</span></span> <span data-ttu-id="0cf8a-296">このプロパティが繰り返しセクションの種類以外のコンテンツ コントロールに対して呼び出されると、「このプロパティは、繰り返しセクション コンテンツ コントロールにのみ使用できます。」というエラー メッセージが表示されて失敗します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-296">If this property is called for a content control that is not of type repeating section, the call fails with the following error message: "This property can only be used with repeating section content controls."</span></span>  <br/> |
|<span data-ttu-id="0cf8a-297">**RepeatingSectionItemTitle** (**String** として)</span><span class="sxs-lookup"><span data-stu-id="0cf8a-297">**RepeatingSectionItemTitle** as **String**</span></span> <br/> |<span data-ttu-id="0cf8a-298">コンテキスト メニューで使用される繰り返しセクション アイテムの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-298">Gets or sets the name of repeating section items used in the context menu.</span></span> <span data-ttu-id="0cf8a-299">このプロパティが繰り返しセクションの種類以外のコンテンツ コントロールに対して呼び出されると、「このプロパティは、繰り返しセクション コンテンツ コントロールにのみ使用できます。」というメッセージが表示されて失敗します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-299">If this property is called for a content control that is not of type repeating section, the call fails with: "This property can only be used with repeating section content controls."</span></span>  <br/> |
|<span data-ttu-id="0cf8a-300">**InsertRepeatingSectionItemBefore** (**ContentControl** として)</span><span class="sxs-lookup"><span data-stu-id="0cf8a-300">**InsertRepeatingSectionItemBefore** as **ContentControl**</span></span> <br/> |<span data-ttu-id="0cf8a-301">現在のアイテムの前に繰り返しセクション アイテムを追加して、新しい繰り返しセクション アイテムを返します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-301">Adds a repeating section item before the current item and returns the new repeating section item.</span></span> <span data-ttu-id="0cf8a-302">このメソッドが繰り返しセクション アイテムの種類以外のコンテンツ コントロールに対して呼び出されると、「このプロパティは、繰り返しセクション アイテムにのみ使用できます。」というメッセージが表示されて失敗します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-302">If this method is called for a content control that is not of type repeating section item, the call fails with: "This property can only be used with repeating section item content controls."</span></span>  <br/> |
|<span data-ttu-id="0cf8a-303">**InsertRepeatingSectionItemAfter** (**ContentControl** として)</span><span class="sxs-lookup"><span data-stu-id="0cf8a-303">**InsertRepeatingSectionItemAfter** as **ContentControl**</span></span> <br/> |<span data-ttu-id="0cf8a-304">現在のアイテムの後に繰り返しセクション アイテムを追加して、新しい繰り返しセクション アイテムを返します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-304">Adds a repeating section item after the current item and returns the new repeating section item.</span></span> <span data-ttu-id="0cf8a-305">このメソッドが繰り返しセクション アイテムの種類以外のコンテンツ コントロールに対して呼び出されると、「このプロパティは、繰り返しセクション アイテムにのみ使用できます。」というメッセージが表示されて失敗します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-305">If this method is called for a content control that is not of type repeating section item, the call fails with: "This property can only be used with repeating section item content controls."</span></span>  <br/> |
   
<span data-ttu-id="0cf8a-306">表 5 に、**RepeatingSectionItem** オブジェクトのメンバーのうち、最も重要性が高いものを示します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-306">Table 5 lists the most important members of the **RepeatingSectionItem** object.</span></span> 
  
<span data-ttu-id="0cf8a-307">**表 5. RepeatingSectionItem オブジェクトのメンバー**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-307">**Table 5. RepeatingSectionItem object members**</span></span>

|<span data-ttu-id="0cf8a-308">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-308">**Member**</span></span>|<span data-ttu-id="0cf8a-309">**説明**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-309">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cf8a-310">**Range** (**Range** として)</span><span class="sxs-lookup"><span data-stu-id="0cf8a-310">**Range** as **Range**</span></span> <br/> |<span data-ttu-id="0cf8a-311">指定の繰り返しセクション アイテムの範囲を返します (開始タグと終了タグは含まれません)。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-311">Returns the range of the specified repeating section item, excluding the start and end tags.</span></span>  <br/> |
|<span data-ttu-id="0cf8a-312">**Delete**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-312">**Delete**</span></span> <br/> |<span data-ttu-id="0cf8a-313">指定の繰り返しセクション アイテムを削除します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-313">Deletes the specified repeating section item.</span></span>  <br/> |
|<span data-ttu-id="0cf8a-314">**InsertItemAfter** (**RepeatingSectionItem** として)</span><span class="sxs-lookup"><span data-stu-id="0cf8a-314">**InsertItemAfter** as **RepeatingSectionItem**</span></span> <br/> |<span data-ttu-id="0cf8a-315">指定のアイテムの後に繰り返しセクション アイテムを追加して、新しいアイテムを返します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-315">Adds a repeating section item after the specified item and returns the new item.</span></span>  <br/> |
|<span data-ttu-id="0cf8a-316">**InsertItemBefore** (**RepeatingSectionItem** として)</span><span class="sxs-lookup"><span data-stu-id="0cf8a-316">**InsertItemBefore** as **RepeatingSectionItem**</span></span> <br/> |<span data-ttu-id="0cf8a-317">指定のアイテムの前に繰り返しセクション アイテムを追加して、新しいアイテムを返します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-317">Adds a repeating section item before the specified item and returns the new item.</span></span>  <br/> |
   
<span data-ttu-id="0cf8a-318">表 6 に、**RepeatingSectionItemColl** オブジェクトのメンバーのうち、最も重要性が高いものを示します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-318">Table 6 lists the most important members of the **RepeatingSectionItemColl** object.</span></span> 
  
<span data-ttu-id="0cf8a-319">**表 6. RepeatingSectionItemColl オブジェクトのメンバー**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-319">**Table 6. RepeatingSectionItemColl object members**</span></span>

|<span data-ttu-id="0cf8a-320">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-320">**Member**</span></span>|<span data-ttu-id="0cf8a-321">**説明**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-321">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cf8a-322">**Item** (**RepeatingSectionItem** として)</span><span class="sxs-lookup"><span data-stu-id="0cf8a-322">**Item** as **RepeatingSectionItem**</span></span> <br/> |<span data-ttu-id="0cf8a-323">個別の繰り返しセクション アイテムを返します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-323">Returns an individual repeating section item.</span></span>  <br/> |
   
<span data-ttu-id="0cf8a-324">表 7 に、繰り返しセクション コンテンツ コントロール用の **WdContentControlType** 列挙体の新しいメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-324">Table 7 shows the new member of the **WdContentControlType** enumeration for repeating section content controls.</span></span> 
  
<span data-ttu-id="0cf8a-325">**表 7. WdContentControlType 列挙体の追加内容**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-325">**Table 7. WdContentControlType enumeration addition**</span></span>

|<span data-ttu-id="0cf8a-326">**定数**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-326">**Constant**</span></span>|<span data-ttu-id="0cf8a-327">**説明**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-327">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cf8a-328">**wdContentControlRepeatingSection**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-328">**wdContentControlRepeatingSection**</span></span> <br/> |<span data-ttu-id="0cf8a-329">1 つの繰り返しセクションに 1 つのアイテムが含まれるコンテンツ コントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-329">Represents a content control that contains a single item in a repeating section.</span></span>  <br/> |
   
### <a name="code-sample"></a><span data-ttu-id="0cf8a-330">コード サンプル</span><span class="sxs-lookup"><span data-stu-id="0cf8a-330">Code sample</span></span>
<span data-ttu-id="0cf8a-331"><a name="WordCC_RepeatingSection"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-331"></span></span>

<span data-ttu-id="0cf8a-332">次のコード サンプルは、繰り返しセクション コンテンツ コントロールをプログラムで使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-332">The following code sample shows how to use repeating section content controls programmatically.</span></span>
  
```vb
Sub testRepeatingSectionControl()
   Dim objRange As Range
   Dim objTable As Table
   Dim objCustomPart As CustomXMLPart
   Dim objCC As ContentControl
   Dim objCustomNode As CustomXMLNode
   
   Set objCustomPart = ActiveDocument.CustomXMLParts.Add
   objCustomPart.LoadXML ("<books>" & _
       "<book><title>Everyday Italian</title>" & _
       "<author>Giada De Laurentiis</author></book>" & _
       "<book><title>Harry Potter</title>" & _
       "<author>J K. Rowling</author></book>" & _
       "<book><title>Learning XML</title>" & _
       "<author>Erik T. Ray</author></book></books>")
   
   Set objRange = ActiveDocument.Paragraphs(1).Range
   Set objTable = ActiveDocument.Tables.Add(objRange, 2, 2)
   With objTable.Borders
       .InsideLineStyle = wdLineStyleSingle
       .OutsideLineStyle = wdLineStyleDouble
   End With
   Set objRange = objTable.Cell(1, 1).Range
   Set objCustomNode = objCustomPart.SelectSingleNode("/books[1]/book[1]/title[1]")
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlText, objRange)
   objCC.XMLMapping.SetMappingByNode objCustomNode
   Set objRange = objTable.Cell(1, 2).Range
   Set objCustomNode = objCustomPart.SelectSingleNode("/books[1]/book[1]/author[1]")
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlText, objRange)
   objCC.XMLMapping.SetMappingByNode objCustomNode
   Set objRange = objTable.Rows(1).Range
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlRepeatingSection, objRange)
   objCC.XMLMapping.SetMapping ("/books[1]/book")
End Sub
```

### <a name="open-xml-file-format-changes-for-repeating-section-content-controls"></a><span data-ttu-id="0cf8a-333">繰り返しセクション コンテンツ コントロールの Open XML ファイル形式の変更点</span><span class="sxs-lookup"><span data-stu-id="0cf8a-333">Open XML File Format changes for repeating section content controls</span></span>
<span data-ttu-id="0cf8a-334"><a name="WordCC_RepeatingSection"> </a></span><span class="sxs-lookup"><span data-stu-id="0cf8a-334"></span></span>

<span data-ttu-id="0cf8a-335">通常、繰り返しセクション コンテンツ コントロールのファイル形式表記では、既存の XML マークアップと同じ要素名や値などを使用します。ただし、外側の繰り返しセクション コンテナーを表す \<sdt\> 要素は、以前のバージョンの Word との互換性を確保するために Word 2013 名前空間内に置かれています。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-335">The file format representation of a repeating section content control generally uses the same element names, values, and so on as the existing XML markup; however, the \<sdt\> element representing the outer repeating section container exists in the Word 2013 namespace, to ensure compatibility with earlier versions of Word.</span></span>
  
<span data-ttu-id="0cf8a-p124">繰り返しセクション コンテンツ コントロールによって囲まれた、内側の個々の繰り返しアイテムは、既存の WordprocessingML 表記を使用してリッチ テキスト コンテンツ コントロールとして保存されます。表 8 に、繰り返しセクション コンテンツ コントロール用 WordprocessingML スキーマの新しい要素をまとめます。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-p124">The individual repeating items within the repeating section content control (that surround each individual item) are saved as rich text content controls using the existing WordprocessingML representation. Table 8 lists new elements in the WordprocessingML schema for repeating section content controls.</span></span>
  
<span data-ttu-id="0cf8a-338">**表 8. 繰り返しセクション コンテンツ コントロール用 WordprocessingML スキーマの新しい要素**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-338">**Table 8. New elements in the WordprocessingML schema for repeating section content controls**</span></span>

|<span data-ttu-id="0cf8a-339">**要素**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-339">**Element**</span></span>|<span data-ttu-id="0cf8a-340">**説明**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-340">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cf8a-341">\<w15:repeatingSection\></span><span class="sxs-lookup"><span data-stu-id="0cf8a-341">\<w15:repeatingSection\></span></span>  <br/> |<span data-ttu-id="0cf8a-p125">繰り返しセクション コンテンツ コントロールを指定します。この要素は、他のすべてのコントロール タイプと互いに排他的で、子要素も子属性もありません。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-p125">Specifies a repeating section content control. This element is mutually exclusive with all other control types and has no child elements or attributes.</span></span>  <br/> |
|<span data-ttu-id="0cf8a-344">\<w15:repeatingSectionItem\></span><span class="sxs-lookup"><span data-stu-id="0cf8a-344">\<w15:repeatingSectionItem\></span></span>  <br/> |<span data-ttu-id="0cf8a-p126">繰り返しセクション アイテム コンテンツ コントロールを指定します。この要素は他のコントロール タイプすべてと互いに排他的で、子要素も子属性もありません。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-p126">Specifies a repeating section item content control. This element is mutually exclusive with all other control types, and has no child elements or attributes.</span></span>  <br/> |
|<span data-ttu-id="0cf8a-347">\<w15:doNotAllowInsertDeleteSection\></span><span class="sxs-lookup"><span data-stu-id="0cf8a-347">\<w15:doNotAllowInsertDeleteSection\></span></span>  <br/> |<span data-ttu-id="0cf8a-348">ユーザーが Word 2013 のユーザー インターフェイスを使用してセクションを追加または削除できないように指定します。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-348">Specifies that the user cannot add or delete sections by using the user interface in Word 2013.</span></span>  <br/> |
|<span data-ttu-id="0cf8a-349">\<w15:sectionTitle\></span><span class="sxs-lookup"><span data-stu-id="0cf8a-349">\<w15:sectionTitle\></span></span>  <br/> |<span data-ttu-id="0cf8a-350">繰り返しセクション アイテムの名前を指定します (コントロールが選択されるときにコンテキスト メニューで使用されます)。</span><span class="sxs-lookup"><span data-stu-id="0cf8a-350">Specifies the name of repeating section items (and is used in the context menu when the control is chosen).</span></span>  <br/> |
   

  

