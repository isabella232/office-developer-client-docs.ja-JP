---
title: Word におけるコンテンツ コントロール
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
keywords:
- コンテンツ コントロール [単語] で、コンテンツ コントロール、[Word] 新機能
localization_priority: Normal
ms.assetid: c0e6dd3b-fae1-453d-a9b4-7f456b5172db
description: Microsoft Word 2013 のコンテンツ コントロールが文書の構造化されたシナリオのより広い範囲を有効にする方法について説明します。
ms.openlocfilehash: 1b0b88da4bc3347ac6748ab57b99d45edd57558d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806892"
---
# <a name="content-controls-in-word"></a><span data-ttu-id="31a1b-104">Word におけるコンテンツ コントロール</span><span class="sxs-lookup"><span data-stu-id="31a1b-104">Content controls in Word</span></span>

<span data-ttu-id="31a1b-105">Microsoft Word 2013 のコンテンツ コントロールが文書の構造化されたシナリオのより広い範囲を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-105">Learn how Microsoft Word 2013 content controls enable a larger range of structured document scenarios.</span></span>

<span data-ttu-id="31a1b-106">このトピックでは、Microsoft Word 2013 とそれらの変更を有効にするドキュメントのシナリオ内のコンテンツ コントロールへの変更に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-106">This topic provides information about changes to content controls in Microsoft Word 2013 and the document scenarios that those changes enable.</span></span>
  
### <a name="structured-documents"></a><span data-ttu-id="31a1b-107">構造化文書</span><span class="sxs-lookup"><span data-stu-id="31a1b-107">Structured documents</span></span>
<span data-ttu-id="31a1b-108"><a name="WordCC_StructuredDocs"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-108"></span></span>

<span data-ttu-id="31a1b-109">構造化文書とは、文書上でコンテンツを配置できる場所や、文書に含めることのできるコンテンツの種類、コンテンツを編集できるかどうかを管理できる文書のことです。</span><span class="sxs-lookup"><span data-stu-id="31a1b-109">Structured documents are documents that control where content can appear on a document, what kind of content can appear in the document, and whether that content can be edited.</span></span>
  
<span data-ttu-id="31a1b-110">Microsoft Word での構造化コンテンツの一般的なシナリオを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-110">Here are some common scenarios for structured content in Microsoft Word:</span></span>
  
- <span data-ttu-id="31a1b-111">法律事務所で、ユーザーが変更してはならない法律用語が含まれている文書を作成する。</span><span class="sxs-lookup"><span data-stu-id="31a1b-111">A legal firm needs to create documents that contain legal language that should not be changed by the user.</span></span>
    
- <span data-ttu-id="31a1b-112">企業で、タイトル、作成者、日付だけをユーザーが入力する提案書の表紙を作成する。</span><span class="sxs-lookup"><span data-stu-id="31a1b-112">A business needs to create a proposal cover page where only the title, author, and date are entered by the user.</span></span>
    
- <span data-ttu-id="31a1b-113">企業で、事前に定義された場所に顧客データが入った請求書を作成する。</span><span class="sxs-lookup"><span data-stu-id="31a1b-113">A business needs to create invoices where the customer data is included in the invoice at predefined regions.</span></span>
    
### <a name="using-content-controls-to-structure-a-document"></a><span data-ttu-id="31a1b-114">コンテンツ コントロールを使用して文書を構造化する</span><span class="sxs-lookup"><span data-stu-id="31a1b-114">Using content controls to structure a document</span></span>
<span data-ttu-id="31a1b-115"><a name="WordCC_StructuredDocs"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-115"></span></span>

<span data-ttu-id="31a1b-116">コンテンツ コントロールは、文書内の特定のコンテンツのコンテナーとして機能する Microsoft Word のエンティティです。</span><span class="sxs-lookup"><span data-stu-id="31a1b-116">Content controls are Microsoft Word entities that act as containers for specific content in a document.</span></span> <span data-ttu-id="31a1b-117">個別のコンテンツ コントロールは、日付、リスト、書式設定されたテキストなどのコンテンツを格納できます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-117">Individual content controls can contain content such as dates, lists, or paragraphs of formatted text.</span></span> <span data-ttu-id="31a1b-118">コンテンツは、ヘルプ コンテンツのブロックの構造し、構造化ドキュメントを作成する、ドキュメントに明確に定義されたブロックを挿入するためのテンプレートで使用するために設計されていますが豊富で、作成することを制御します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-118">Content controls help you to create rich, structured blocks of content and are designed for use in templates that insert well-defined blocks into your documents, creating structured documents.</span></span>
  
<span data-ttu-id="31a1b-119">コンテンツ コントロールは、コンテンツの位置を固定したり、コンテンツの種類を指定したり (日付、画像、テキストなど)、編集を許可または禁止したり、コンテンツにセマンティックな意味を付与したりするため、構造化文書の作成に最適です。</span><span class="sxs-lookup"><span data-stu-id="31a1b-119">Content controls are ideal for creating structured documents because content controls help you fix the position of content, specify the kind of content (for example, a date, a picture, or text), restrict or enable editing, and add semantic meaning to content.</span></span>
  
### <a name="content-controls-in-word-2010"></a><span data-ttu-id="31a1b-120">Word 2010 でコンテンツ コントロール</span><span class="sxs-lookup"><span data-stu-id="31a1b-120">Content controls in Word 2010</span></span>
<span data-ttu-id="31a1b-121"><a name="WordCC_StructuredDocs"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-121"></span></span>

<span data-ttu-id="31a1b-122">以下のコンテンツ コントロールは、Word 2010 で使用できます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-122">The following content controls are available in Word 2010:</span></span>
  
- <span data-ttu-id="31a1b-123">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="31a1b-123">Rich Text</span></span>
    
- <span data-ttu-id="31a1b-124">プレーン テキスト</span><span class="sxs-lookup"><span data-stu-id="31a1b-124">Plain Text</span></span>
    
- <span data-ttu-id="31a1b-125">画像</span><span class="sxs-lookup"><span data-stu-id="31a1b-125">Picture</span></span>
    
- <span data-ttu-id="31a1b-126">文書パーツ ギャラリー</span><span class="sxs-lookup"><span data-stu-id="31a1b-126">Building Block Gallery</span></span>
    
- <span data-ttu-id="31a1b-127">コンボ ボックス</span><span class="sxs-lookup"><span data-stu-id="31a1b-127">Combo Box</span></span>
    
- <span data-ttu-id="31a1b-128">ドロップダウン リスト</span><span class="sxs-lookup"><span data-stu-id="31a1b-128">Drop-Down List</span></span>
    
- <span data-ttu-id="31a1b-129">日付</span><span class="sxs-lookup"><span data-stu-id="31a1b-129">Date</span></span>
    
- <span data-ttu-id="31a1b-130">チェックボックス</span><span class="sxs-lookup"><span data-stu-id="31a1b-130">Checkbox</span></span>
    
- <span data-ttu-id="31a1b-131">グループ</span><span class="sxs-lookup"><span data-stu-id="31a1b-131">Group</span></span>
    
<span data-ttu-id="31a1b-132">コンテンツ コントロールを Word 2010 は、さまざまな潜在的な構造化ドキュメント ソリューションを有効にするが、Word 2013 では、コンテンツ コントロールよりさまざまなシナリオを有効にします。</span><span class="sxs-lookup"><span data-stu-id="31a1b-132">Word 2010 content controls enable various potential structured document solutions, but in Word 2013 content controls enable a greater range of scenarios.</span></span>
  
## <a name="content-control-improvements-in-word-2013"></a><span data-ttu-id="31a1b-133">Word 2013 のコンテンツ コントロールの機能強化</span><span class="sxs-lookup"><span data-stu-id="31a1b-133">Content control improvements in Word 2013</span></span>
<span data-ttu-id="31a1b-134"><a name="WordCC_WhatsNew"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-134"></span></span>

<span data-ttu-id="31a1b-135">2013 年 Word のコンテンツ コントロールは、次の 3 つの大きな進歩を提供: ビジュアル化、リッチ テキスト コンテンツ コントロールの XML マッピングのサポートと繰り返されるコンテンツについての新しいコンテンツ コントロールを改善します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-135">In Word 2013, content controls provide three key improvements: improved visualization, support for XML Mapping for Rich Text content controls, and a new content control for repeating content.</span></span>
  
### <a name="improved-visualization"></a><span data-ttu-id="31a1b-136">視覚化の改善</span><span class="sxs-lookup"><span data-stu-id="31a1b-136">Improved visualization</span></span>

<span data-ttu-id="31a1b-137">Word 2013 では、個々 のコンテンツ コントロールに 3 つの状態のいずれかで表示されることができます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-137">Word 2013 allows an individual content control to appear in one of three possible states:</span></span>
  
- <span data-ttu-id="31a1b-138">境界ボックス</span><span class="sxs-lookup"><span data-stu-id="31a1b-138">Bounding box</span></span>
    
- <span data-ttu-id="31a1b-139">開始/終了タグ</span><span class="sxs-lookup"><span data-stu-id="31a1b-139">Start/End tags</span></span>
    
- <span data-ttu-id="31a1b-140">なし</span><span class="sxs-lookup"><span data-stu-id="31a1b-140">None</span></span>
    
> [!NOTE]
> <span data-ttu-id="31a1b-141">場合は明記されません、文書が**デザイン モード**で表示されていないときにこのセクションでコンテンツ コントロールのビジュアル化について説明します。コンテンツ コントロールの表示モードを設定するには、**コンテンツ コントロールのプロパティ**] ダイアログ ボックスでドロップ ダウン リスト**として表示する**コントロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-141">If not stated otherwise, this section discusses the visualization of content controls when the document is not viewed in **Design Mode**.You set the display mode for a content control by using the **Show as** drop-down list control in the **Content Control Properties** dialog box.</span></span> 
  
<span data-ttu-id="31a1b-142">**図 1 です。コンテンツ コントロールのプロパティ] ダイアログ ボックス**</span><span class="sxs-lookup"><span data-stu-id="31a1b-142">**Figure 1. Content Control Properties dialog box**</span></span>

<span data-ttu-id="31a1b-143">![コンテンツ コントロールのプロパティ] ダイアログ ボックス](media/DK2_WordCC_Fig01.jpg "コンテンツ コントロールのプロパティ] ダイアログ ボックス")</span><span class="sxs-lookup"><span data-stu-id="31a1b-143">![Content control properties dialog box](media/DK2_WordCC_Fig01.jpg "Content control properties dialog box")</span></span>
  
<span data-ttu-id="31a1b-144">( [Word 2013 の新しいコンテンツ コントロールのオブジェクト モデルのメンバー](#WordCC_NewOM)に後で説明します)、Word 2013 のオブジェクト モデルを使用してコンテンツ コントロールの表示モードを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-144">You can also set the display mode for a content control by using the Word 2013 object model (discussed later in [New Word 2013 content control object model members](#WordCC_NewOM)).</span></span>
  
### <a name="bounding-box"></a><span data-ttu-id="31a1b-145">境界ボックス</span><span class="sxs-lookup"><span data-stu-id="31a1b-145">Bounding box</span></span>
<span data-ttu-id="31a1b-146"><a name="WordCC_DefaultRendering"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-146"></span></span>

<span data-ttu-id="31a1b-147">Word 2007 および Word 2010 で表示されるコンテンツ コントロールの外観を保持するのには、Word 2013 のコンテンツ コントロールの既定のレンダリング外接するボックスをオンします。</span><span class="sxs-lookup"><span data-stu-id="31a1b-147">The default rendering for content controls in Word 2013 is to preserve the look of content controls as they appear in Word 2007 and Word 2010; that is, as a bounding box.</span></span> <span data-ttu-id="31a1b-148">**バウンディング ボックスで**、次のユーザーの操作に応じて表示の変更を表示するコンテンツ コントロールを設定するとします。</span><span class="sxs-lookup"><span data-stu-id="31a1b-148">When a content control is set to show as **Bounding Box**, the display changes depending upon the following user interaction:</span></span>
  
- <span data-ttu-id="31a1b-149">コンテンツ コントロールにフォーカスがないときには視覚化されません</span><span class="sxs-lookup"><span data-stu-id="31a1b-149">When the content control does not have the focus, no visualization occurs</span></span>
    
- <span data-ttu-id="31a1b-150">マウスを置くと、コンテンツ コントロールは影付きの四角形として表示されます</span><span class="sxs-lookup"><span data-stu-id="31a1b-150">On mouse-over, the content control appears as a shaded rectangle</span></span>
    
<span data-ttu-id="31a1b-151">**図 2 になります。マウス ポインターを上のコンテンツ コントロール**</span><span class="sxs-lookup"><span data-stu-id="31a1b-151">**Figure 2. Content control on mouse-over**</span></span>

<span data-ttu-id="31a1b-152">![上でマウスをコントロールのコンテンツ](media/DK2_WordCC_Fig02.jpg "上でマウスをコントロールのコンテンツ")</span><span class="sxs-lookup"><span data-stu-id="31a1b-152">![Content control on mouse over](media/DK2_WordCC_Fig02.jpg "Content control on mouse over")</span></span>
  
- <span data-ttu-id="31a1b-153">コンテンツ コントロールにフォーカスがある場合 (ユーザーがコンテンツ コントロールを選択した場合)、コントロールが「境界ボックス」として表示されます （コンテンツで線で囲まれ、タイトルを設定した場合にはそのタイトルが表示されます）</span><span class="sxs-lookup"><span data-stu-id="31a1b-153">When the content control has the focus (when the user chooses the content control), the control appears as a "bounding box" (with a line around the content and the title showing, if a title has been set)</span></span>
    
<span data-ttu-id="31a1b-154">**図 3 です。フォーカスを持つコントロールのコンテンツ**</span><span class="sxs-lookup"><span data-stu-id="31a1b-154">**Figure 3. Content control with focus**</span></span>

<span data-ttu-id="31a1b-155">![フォーカスを持つコントロールのコンテンツ](media/DK2_WordCC_Fig03.jpg "フォーカスを持つコントロールのコンテンツ")</span><span class="sxs-lookup"><span data-stu-id="31a1b-155">![Content control with focus](media/DK2_WordCC_Fig03.jpg "Content control with focus")</span></span>
  
### <a name="startend-tags"></a><span data-ttu-id="31a1b-156">開始/終了タグ</span><span class="sxs-lookup"><span data-stu-id="31a1b-156">Start/End tags</span></span>
<span data-ttu-id="31a1b-157"><a name="WordCC_StartEndTags"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-157"></span></span>

<span data-ttu-id="31a1b-158">**開始/終了タグ**で表示するコンテンツ コントロールを設定すると、タグがユーザーの操作に関係なく表示され、タイトルは表示されません。ですが、上でマウスのボタン、**ドロップダウン リスト**ボタンなどが表示されます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-158">When the content control is set to show as **Start/End tag**, the tags are displayed regardless of user interaction, and the title never appears; but buttons, such as the **Drop-Down List** button, appear on mouse over.</span></span> 
  
<span data-ttu-id="31a1b-159">**図 4 です。コンテンツ コントロールの開始/終了タグを表示する設定**</span><span class="sxs-lookup"><span data-stu-id="31a1b-159">**Figure 4. Content control set to show as start/end tags**</span></span>

<span data-ttu-id="31a1b-160">![開始タグと終了タグを表示するコンテンツ コントロールの設定](media/DK2_WordCC_Fig04.jpg "開始タグと終了タグを表示するコンテンツ コントロールの設定")</span><span class="sxs-lookup"><span data-stu-id="31a1b-160">![Content control set to show as start and end tags](media/DK2_WordCC_Fig04.jpg "Content control set to show as start and end tags")</span></span>
  
### <a name="none"></a><span data-ttu-id="31a1b-161">なし</span><span class="sxs-lookup"><span data-stu-id="31a1b-161">None</span></span>
<span data-ttu-id="31a1b-162"><a name="WordCC_Invisible"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-162"></span></span>

<span data-ttu-id="31a1b-163">**[なし]** として表示するコンテンツ コントロールを設定すると、コンテンツ コントロールは表示されません。</span><span class="sxs-lookup"><span data-stu-id="31a1b-163">When the content control is set to show as **None**, the content control is not displayed.</span></span>
  
### <a name="content-control-colorization"></a><span data-ttu-id="31a1b-164">コンテンツ コントロールの色</span><span class="sxs-lookup"><span data-stu-id="31a1b-164">Content control colorization</span></span>
<span data-ttu-id="31a1b-165"><a name="WordCC_CCColorization"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-165"></span></span>

<span data-ttu-id="31a1b-166">、別の種類のコンテンツ コントロールの表示を有効にするだけでなく Word 2013 も、個々 のコンテンツ コントロールの色を設定できます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-166">In addition to enabling a different kind of display for a content control, Word 2013 also helps you to set the color for an individual content control.</span></span> <span data-ttu-id="31a1b-167">コンテンツ コントロールの色を設定するには、**コンテンツ コントロールのプロパティ**] ダイアログ ボックスで [**色**] ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-167">You set the color of a content control by using the **Color** button in the **Content Control Properties** dialog box.</span></span> 
  
<span data-ttu-id="31a1b-168">( [Word 2013 の新しいコンテンツ コントロールのオブジェクト モデルのメンバー](#WordCC_NewOM)に後で説明します)、Word 2013 のオブジェクト モデルを使用してコンテンツ コントロールの色を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-168">You can also set the color of a content control by using the Word 2013 object model (discussed later in [New Word 2013 content control object model members](#WordCC_NewOM)).</span></span>
  
<span data-ttu-id="31a1b-169">**図 5。コンテンツ コントロールのプロパティ] ダイアログ ボックス**</span><span class="sxs-lookup"><span data-stu-id="31a1b-169">**Figure 5. Content Control Properties dialog box**</span></span>

<span data-ttu-id="31a1b-170">![コンテンツ コントロールのプロパティ] ダイアログ ボックス](media/DK2_WordCC_Fig05.jpg "コンテンツ コントロールのプロパティ] ダイアログ ボックス")</span><span class="sxs-lookup"><span data-stu-id="31a1b-170">![Content control properties dialog box](media/DK2_WordCC_Fig05.jpg "Content control properties dialog box")</span></span>
  
### <a name="support-for-xml-mapping-for-rich-text-content-controls"></a><span data-ttu-id="31a1b-171">リッチ テキスト コンテンツ コントロールの XML マッピングのサポート</span><span class="sxs-lookup"><span data-stu-id="31a1b-171">Support for XML mapping for rich text content controls</span></span>
<span data-ttu-id="31a1b-172"><a name="WordCC_XMLMapping"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-172"></span></span>

<span data-ttu-id="31a1b-173">Word 2013 では、リッチ テキスト コンテンツ コントロール、文書パーツ コンテンツ コントロールの内容を XML データ ストアにマップすることができます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-173">Word 2013 helps you to map the content of rich text content controls and document building block content controls to the XML data store.</span></span> <span data-ttu-id="31a1b-174">これを行うには、コンテンツ コントロールの*XML マッピング*を設定します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-174">To do this, you set the  *XML mapping*  for the content control.</span></span> <span data-ttu-id="31a1b-175">オブジェクト モデルでは、既存の**XMLMapping.SetMapping**メソッドを使用してこのプロパティを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-175">You can set this property by using the existing **XMLMapping.SetMapping** method in the object model.</span></span> <span data-ttu-id="31a1b-176">フラットの Open XML マークアップ文字列に変換 (を使用して、標準の XML エンコーディング)、ようにすると、カスタム XML パーツ内でカスタム XML が格納されるカスタム XML 部分内のテキスト ノードとして格納できます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-176">Within the custom XML part, the custom XML is stored as flat Open XML markup converted into a string (by using standard XML encoding), so that it can be stored as a text node in the custom XML part.</span></span> <span data-ttu-id="31a1b-177">ただし、マッピングは引き続き、リーフ ノードまたは属性にマップにのみ正常にできる制限があります。</span><span class="sxs-lookup"><span data-stu-id="31a1b-177">However, the mapping continues to have the limitation that it can only successfully map to leaf nodes or attributes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="31a1b-p105">リッチ テキスト コンテンツ コントロールに他のリッチ テキスト コンテンツ コントロールを含めることはできません。(ファイル形式の操作やコピーと貼り付けなどによって) リッチ コンテキスト コンテンツ コントロールが別のリッチ コンテキスト コントロールの中に入ると、それはマップされたリッチ テキスト コントロールの中に含まれなくなるまでリンク解除されます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-p105">Rich text content controls cannot contain other rich text content controls. If one exists inside of another (for example, because of file format manipulation, copy and paste, and so on), it is unlinked until it is no longer contained inside a mapped rich text control.</span></span> 
  
<span data-ttu-id="31a1b-180">XML マッピングを設定する方法の詳細については、このトピックの後半のセクション[Word 2013 の新しいコンテンツ コントロールのオブジェクト モデルのメンバー](#WordCC_NewOM)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31a1b-180">For more information about how to set up XML mapping, see the section [New Word 2013 content control object model members](#WordCC_NewOM) later in this topic.</span></span> 
  
### <a name="supporting-repeating-content"></a><span data-ttu-id="31a1b-181">繰り返しコンテンツのサポート</span><span class="sxs-lookup"><span data-stu-id="31a1b-181">Supporting repeating content</span></span>
<span data-ttu-id="31a1b-182"><a name="WordCC_SupportingRepeating"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-182"></span></span>

<span data-ttu-id="31a1b-183">視覚化機能の強化およびリッチ テキスト コンテンツ コントロールに XML マッピングのサポートに加え、Word 2013 は、新しいコンテンツ コントロールを使用すると、コンテンツを繰り返しているを追加します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-183">In addition to visualization enhancements and support for XML mapping to rich text content controls, Word 2013 also adds a new content control that enables you to repeat content.</span></span> <span data-ttu-id="31a1b-184">繰り返しセクションのコンテンツ コントロールには、他のコンテンツ コントロールを含む、内に含まれる内容が繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-184">The repeating section content control repeats the content contained within it, including other content controls.</span></span>
  
<span data-ttu-id="31a1b-p107">段落全体や表の行の周囲に繰り返しセクション コンテンツ コントロールを挿入します。あるセクションをこのコントロールで囲むと、中に含まれているセクションの上または下にそのセクションのコピーを挿入できます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-p107">You insert the repeating section content control around entire paragraphs or table rows. Once the control surrounds a section, you can insert copies of the section above or below the contained section.</span></span>
  
<span data-ttu-id="31a1b-187">**図 6 です。繰り返しセクションのコンテンツ コントロールのコンテキスト メニュー**</span><span class="sxs-lookup"><span data-stu-id="31a1b-187">**Figure 6. Repeating section content control context menu**</span></span>

<span data-ttu-id="31a1b-188">![繰り返しセクションのコンテンツ コントロールのコンテキスト](media/DK2_WordCC_Fig06.jpg "繰り返しセクションのコンテンツ コントロールのコンテキスト")</span><span class="sxs-lookup"><span data-stu-id="31a1b-188">![Repeating section content control context](media/DK2_WordCC_Fig06.jpg "Repeating section content control context")</span></span>
  
<span data-ttu-id="31a1b-189">繰り返して、[挿入] セクション (プラス記号 (![正符号](media/DK2_WordCC_Fig06A.jpg "プラス記号")) 付きのボタンとして表示されます)、コンテンツ コントロールの最後に、どちらのコントロールを使用するか、[コンテキスト] メニューのコマンドを選択することによって図 6 に示すように。</span><span class="sxs-lookup"><span data-stu-id="31a1b-189">You can repeat the inserted section by using either the control on the end of the content control (displayed as a button with a plus sign (![Plus sign](media/DK2_WordCC_Fig06A.jpg "Plus sign"))) or by choosing a command on the context menu, as shown in Figure 6.</span></span> <span data-ttu-id="31a1b-190">繰り返し出現するコンテンツは、**コンテンツ コントロールのプロパティ**] ダイアログ ボックスを使用してタイトルを割り当てることができますコントロールの個別のセクションになります。</span><span class="sxs-lookup"><span data-stu-id="31a1b-190">The repeated content becomes a separate section of the control that you can assign a title by using the **Content Control Properties** dialog box.</span></span> 
  
<span data-ttu-id="31a1b-191">**図 7 です。コンテンツ コントロールのプロパティ] ダイアログ ボックスで、セクションのタイトルを割り当てる**</span><span class="sxs-lookup"><span data-stu-id="31a1b-191">**Figure 7. Assign a section title in the Content Control Properties dialog box**</span></span>

<span data-ttu-id="31a1b-192">![コンテンツ コントロールのプロパティ] ダイアログ ボックス](media/DK2_WordCC_Fig07.jpg "コンテンツ コントロールのプロパティ] ダイアログ ボックス")</span><span class="sxs-lookup"><span data-stu-id="31a1b-192">![Content control properties dialog box](media/DK2_WordCC_Fig07.jpg "Content control properties dialog box")</span></span>
  
<span data-ttu-id="31a1b-193">指定するセクション、タイトル、**コンテンツ コントロールのプロパティ**] ダイアログ ボックスで**ユーザーを追加し、セクションの削除を許可する**を選択した場合、ユーザーを追加したり、名前でセクションを削除できます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-193">Once you have given the section a title, if you select **Allow users to add and remove sections** in the **Content Control Properties** dialog box, users can add or delete the section by name.</span></span> 
  
<span data-ttu-id="31a1b-194">**図 8 です。繰り返しセクションのコンテンツ コントロールのコンテキスト メニューを使用して、セクションを削除するのには**</span><span class="sxs-lookup"><span data-stu-id="31a1b-194">**Figure 8. Use the repeating section content control context menu to delete a section**</span></span>

<span data-ttu-id="31a1b-195">![繰り返しセクションのコンテンツ コントロールのコンテキスト](media/DK2_WordCC_Fig08.jpg "繰り返しセクションのコンテンツ コントロールのコンテキスト")</span><span class="sxs-lookup"><span data-stu-id="31a1b-195">![Repeating section content control context](media/DK2_WordCC_Fig08.jpg "Repeating section content control context")</span></span>
  
<span data-ttu-id="31a1b-p109">繰り返しセクション コンテンツ コントロールで他のコンテンツ コントロールを囲むと、中に含まれたコンテンツ コントロールは新しいアイテムごとに繰り返されます。ただし、そのようなコンテンツ コントロールのコンテンツはプレースホルダー テキストにリセットされます。以下の 2 つの例外の場合には子コントロール コンテンツが保持されます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-p109">When a repeating section content control surrounds other content controls, the enclosed content controls are repeated in each new item; but any such content controls have their contents reset to placeholder text. There are two exceptions where child control contents are preserved:</span></span> 
  
- <span data-ttu-id="31a1b-198">子コントロールが繰り返しセクション コントロールの場合。</span><span class="sxs-lookup"><span data-stu-id="31a1b-198">When a child control is a repeating section control.</span></span>
    
- <span data-ttu-id="31a1b-199">子コントロールが、繰り返しセクション コンテンツ コントロール外のノードに XML マッピングされている場合。</span><span class="sxs-lookup"><span data-stu-id="31a1b-199">When a child control is XML-mapped to a node outside the repeating section content control.</span></span>
    
<span data-ttu-id="31a1b-200">**図 9 です。反復する前に子コントロールを含むセクションのコンテンツ コントロールを繰り返し**</span><span class="sxs-lookup"><span data-stu-id="31a1b-200">**Figure 9. Repeating section content control containing child controls before repeat**</span></span>

<span data-ttu-id="31a1b-201">![繰り返しの前にコンテンツ コントロールをセクションを繰り返します](media/DK2_WordCC_Fig09.jpg "繰り返しの前にコンテンツ コントロールをセクションを繰り返します")</span><span class="sxs-lookup"><span data-stu-id="31a1b-201">![Repeating section content control before repeat](media/DK2_WordCC_Fig09.jpg "Repeating section content control before repeat")</span></span>
  
<span data-ttu-id="31a1b-202">**図 10 です。繰り返しの後に子コントロールを含むセクションのコンテンツ コントロールを繰り返し**</span><span class="sxs-lookup"><span data-stu-id="31a1b-202">**Figure 10. Repeating section content control containing child controls after repeat**</span></span>

<span data-ttu-id="31a1b-203">![繰り返しの後のセクションでコンテンツ コントロールを繰り返し](media/DK2_WordCC_Fig10.jpg "繰り返しの後のセクションでコンテンツ コントロールを繰り返し")</span><span class="sxs-lookup"><span data-stu-id="31a1b-203">![Repeating section content control after repeat](media/DK2_WordCC_Fig10.jpg "Repeating section content control after repeat")</span></span>
  
### <a name="repeating-section-content-controls-around-xml-mapped-controls"></a><span data-ttu-id="31a1b-204">XML マッピング コントロールを囲む繰り返しセクション コンテンツ コントロール</span><span class="sxs-lookup"><span data-stu-id="31a1b-204">Repeating section content controls around XML-mapped controls</span></span>
<span data-ttu-id="31a1b-205"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-205"></span></span>

<span data-ttu-id="31a1b-206">繰り返しセクションに含まれる XML マッピングでは、Word 2013 マップに次のようにします。</span><span class="sxs-lookup"><span data-stu-id="31a1b-206">For XML mappings that are contained in a repeating section, Word 2013 maps them as follows.</span></span>
  
<span data-ttu-id="31a1b-207">マッピングは、親チェーンの一部として設定されるノード内のアイテムと交差しない、バインディングは「絶対バインディング」と、すべての繰り返しセクション項目に同じ内容を示しています。</span><span class="sxs-lookup"><span data-stu-id="31a1b-207">If the mapping does not intersect with an item in the node set as part of its parent chain, the binding is an "absolute binding" and shows the same content in all repeating section items.</span></span>
  
<span data-ttu-id="31a1b-208">マッピングは、親チェーンの一部として設定されるノード内のアイテムに交差すると、バインドが「相対バインド"、次のように再マップされます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-208">If the mapping does intersect with an item in the node set as part of its parent chain, the binding is a "relative binding", and is remapped as follows:</span></span>
  
- <span data-ttu-id="31a1b-209">ノードの絶対バインディングが判別されます (クエリ式はすべて平坦化されます) - これは最初のマッピングで生じます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-209">The absolute binding for the node is determined (flattening out any query expressions)─this should happen on initial mapping</span></span>
    
- <span data-ttu-id="31a1b-210">ノード セットと重なるバインディングの軸が削除されます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-210">The axis of the binding that intersects with the node set is removed</span></span>
    
- <span data-ttu-id="31a1b-211">残りの XPath が、繰り返しセクション コンテンツ アイテムの XPath に基づいて相対評価されます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-211">The remainder of the XPath is evaluated relative to the XPath of the repeating section content item</span></span>
    
<span data-ttu-id="31a1b-212">たとえば、次のマッピングが生じるとします。</span><span class="sxs-lookup"><span data-stu-id="31a1b-212">For example, the following mappings might occur:</span></span>
  
- <span data-ttu-id="31a1b-213">繰り返しセクションが \root\next\path にマップされます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-213">The repeating section is mapped to \root\next\path</span></span>
    
- <span data-ttu-id="31a1b-214">サンプル アイテム内のコントロールが \root\next\path[2]\baz にマップされます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-214">The control in the sample item is mapped to \root\next\path[2]\baz</span></span>
    
- <span data-ttu-id="31a1b-215">Word が \root\next\path[2] をノード セット内のアイテムに対応付けます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-215">Word matches \root\next\path[2] to an item in the node set</span></span>
    
<span data-ttu-id="31a1b-216">結果としてバインディングは .\baz として評価されます。この場合、繰り返しコンテンツ アイテムのノードが基準となります。</span><span class="sxs-lookup"><span data-stu-id="31a1b-216">The binding is therefore evaluated as .\baz, where the base is the node of the repeating content item.</span></span>
  
<span data-ttu-id="31a1b-217">繰り返しコンテンツ コントロールを処理する際、データの損失を避けて障害を防止するには以下の提案が役立ちます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-217">The following suggestions for working with repeating content controls can help you prevent data loss and avoid frustration.</span></span>
  
### <a name="working-with-repeating-section-content-controls-that-are-mapped-to-xml-data"></a><span data-ttu-id="31a1b-218">XML データにマップされる繰り返しセクション コンテンツ コントロールを扱う</span><span class="sxs-lookup"><span data-stu-id="31a1b-218">Working with repeating section content controls that are mapped to XML data</span></span>
<span data-ttu-id="31a1b-219"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-219"></span></span>

<span data-ttu-id="31a1b-220">たびに、ユーザーには、ドキュメントが開かれた XML データにマップされている繰り返しセクションでコンテンツ コントロールを挿入すると、Word は、データ ストア内の情報に基づいて、繰り返しセクション項目を再作成されます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-220">If you insert a repeating section content control that is mapped to XML data, every time your user reopens the document, Word recreates the repeating section items, based on the information in the data store.</span></span> <span data-ttu-id="31a1b-221">文書を保存する場合でも、ユーザーは、繰り返しセクション内のアイテムに、ドキュメント データ ストアにマップされていないも、すべての変更は失われます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-221">Even if you save the document, any changes that the user makes in the repeating section items in the document that aren't also mapped into the data store are lost.</span></span>
  
<span data-ttu-id="31a1b-222">この事態が生じないようにするには、繰り返しセクション コンテンツ コントロールをロックし、同じように XML にマップされる、ロックされていない子コンテンツ コントロールでのみユーザーが編集を行えるようにします。</span><span class="sxs-lookup"><span data-stu-id="31a1b-222">To help prevent this from happening, lock the repeating section content control and allow the user to edit only in unlocked child content controls that are mapped to the XML as well.</span></span>
  
### <a name="binding-a-repeating-section-content-control-to-a-table"></a><span data-ttu-id="31a1b-223">繰り返しセクション コンテンツ コントロールを表にバインドする</span><span class="sxs-lookup"><span data-stu-id="31a1b-223">Binding a repeating section content control to a table</span></span>
<span data-ttu-id="31a1b-224"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-224"></span></span>

<span data-ttu-id="31a1b-225">テーブルに繰り返しセクションのコンテンツ コントロールをバインドする場合は、テーブル*し*挿入の繰り返しセクションでコンテンツ コントロールとその他の方法ではありません周囲を挿入します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-225">If you want to bind a repeating section content control to a table, insert the table and  *then*  the insert repeating section content control, and not the other way around.</span></span> <span data-ttu-id="31a1b-226">(それ以外の場合、ことはできませんテーブルのみを選択する)。</span><span class="sxs-lookup"><span data-stu-id="31a1b-226">(Otherwise, you won't be able to select only the table).</span></span> 
  
### <a name="nesting-repeating-section-content-controls-within-a-table"></a><span data-ttu-id="31a1b-227">繰り返しセクション コンテンツ コントロールを表の中に入れ子にする</span><span class="sxs-lookup"><span data-stu-id="31a1b-227">Nesting repeating section content controls within a table</span></span>
<span data-ttu-id="31a1b-228"><a name="WordCC_RepeatingSectionCCs"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-228"></span></span>

<span data-ttu-id="31a1b-229">繰り返しセクション コンテンツ コントロールを表の中に隣接して入れ子にする場合 (たとえば、親の繰り返しセクション コンテンツ コントロールの最後と子繰り返しセクション コンテンツ コントロールが同じセル内にある場合)、内部セクションでアイテムを追加したり削除したりすると、外部繰り返しセクションが削除されます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-229">Nesting repeating section content controls tightly within a table (for example, when the end of the parent and child repeating section content control is in the same cell) causes the outer repeating section to be deleted when the inner section has an item added or removed.</span></span>
  
<span data-ttu-id="31a1b-230">発生している間と次の 1 つの繰り返しセクションでコンテンツ コントロールの最後の段落記号を追加することによって、これを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-230">You can prevent this from happening by adding a paragraph marker between the end of one repeating section content control and the next.</span></span> <span data-ttu-id="31a1b-231">段落記号を非表示には、リボンの [**ホーム**] タブの**表示/非表示**オプションをオフにします。</span><span class="sxs-lookup"><span data-stu-id="31a1b-231">To hide the paragraph marker, deselect the **Show/Hide** option on the **Home** tab of the ribbon.</span></span> 
  
### <a name="open-xml-file-format-schema-additions"></a><span data-ttu-id="31a1b-232">Open XML ファイル形式スキーマにおける追加内容</span><span class="sxs-lookup"><span data-stu-id="31a1b-232">Open XML File Format schema additions</span></span>
<span data-ttu-id="31a1b-233"><a name="WordCC"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-233"></span></span>

<span data-ttu-id="31a1b-234">WordprocessingML Open XML ファイル形式スキーマに以下の要素が追加されました。</span><span class="sxs-lookup"><span data-stu-id="31a1b-234">The following elements were added to the WordprocessingML Open XML File Format schema.</span></span>
  
<span data-ttu-id="31a1b-235">**表 1 です。コンテンツ コントロールの Open XML ファイルの形式の WordprocessingML スキーマに新しい要素**</span><span class="sxs-lookup"><span data-stu-id="31a1b-235">**Table 1. New elements in the WordprocessingML Open XML File Format schema for content controls**</span></span>

|<span data-ttu-id="31a1b-236">**要素**</span><span class="sxs-lookup"><span data-stu-id="31a1b-236">**Element**</span></span>|<span data-ttu-id="31a1b-237">**説明**</span><span class="sxs-lookup"><span data-stu-id="31a1b-237">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31a1b-238">\<w:appearance\></span><span class="sxs-lookup"><span data-stu-id="31a1b-238">\<w:appearance\></span></span>  <br/> |<span data-ttu-id="31a1b-239">\<w:appearance\>の子要素は、 \<w:sdtPr\>。</span><span class="sxs-lookup"><span data-stu-id="31a1b-239">\<w:appearance\> is a child element of \<w:sdtPr\>.</span></span>  <br/> <span data-ttu-id="31a1b-240">val 属性には以下の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="31a1b-240">The following values are valid for the val attribute:</span></span>  <br/> <span data-ttu-id="31a1b-241">\<w:appearance val = boundingBox</span><span class="sxs-lookup"><span data-stu-id="31a1b-241">\<w:appearance val= boundingBox</span></span>|<span data-ttu-id="31a1b-242">タグの前に追加されるマークアップ</span><span class="sxs-lookup"><span data-stu-id="31a1b-242">tags</span></span>|<span data-ttu-id="31a1b-243">非表示にします。</span><span class="sxs-lookup"><span data-stu-id="31a1b-243">hidden.</span></span>  <br/> <span data-ttu-id="31a1b-244">既定値は boundingBox です。</span><span class="sxs-lookup"><span data-stu-id="31a1b-244">The default value is boundingBox.</span></span>  <br/> |
|<span data-ttu-id="31a1b-245">\<w:color\></span><span class="sxs-lookup"><span data-stu-id="31a1b-245">\<w:color\></span></span>  <br/> |<span data-ttu-id="31a1b-246">\<w:color\>の子要素は、 \<w:sdtPr\>。</span><span class="sxs-lookup"><span data-stu-id="31a1b-246">\<w:color\> is a child element of \<w:sdtPr\>.</span></span>  <br/> <span data-ttu-id="31a1b-p113">このコンテンツ モデルは、既存の CT_Color 複合型と一致します。既定値は Word 2010 で使用されている色です。</span><span class="sxs-lookup"><span data-stu-id="31a1b-p113">The content model matches the existing CT_Color complex type. The default value is the color used in Word 2010.</span></span>  <br/> |
   
## <a name="new-word-2013-content-control-object-model-members"></a><span data-ttu-id="31a1b-249">新しい Word 2013 のコンテンツ コントロール オブジェクト モデルのメンバー</span><span class="sxs-lookup"><span data-stu-id="31a1b-249">New Word 2013 content control object model members</span></span>
<span data-ttu-id="31a1b-250"><a name="WordCC_NewOM"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-250"></span></span>

<span data-ttu-id="31a1b-251">新しい拡張機能と Word 2013 のコンテンツ コントロールに追加された機能では、新しい機能セットをプログラムで操作できるように、Word のオブジェクト モデルが更新されました。</span><span class="sxs-lookup"><span data-stu-id="31a1b-251">With the new enhancements and additions to content controls in Word 2013, the object model for Word has been updated to allow for programmatic manipulation of the new feature set.</span></span> <span data-ttu-id="31a1b-252">さらに、また行ったワード プロセッシング ドキュメントの Open XML ファイルの基になる形式にします。</span><span class="sxs-lookup"><span data-stu-id="31a1b-252">In addition, changes have also been made to the underlying Open XML File Format for word processing documents.</span></span>
  
<span data-ttu-id="31a1b-253">以下のセクションでは、各コンテンツ コントロール機能拡張に関連する特有のオブジェクト モデルの変更内容について詳しく取り上げます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-253">The following sections provide more information about the specific object model changes related to each content control enhancement.</span></span>
  
### <a name="visualization-enhancements"></a><span data-ttu-id="31a1b-254">視覚化の機能拡張</span><span class="sxs-lookup"><span data-stu-id="31a1b-254">Visualization enhancements</span></span>
<span data-ttu-id="31a1b-255"><a name="WordCC_VisEnhancements"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-255"></span></span>

<span data-ttu-id="31a1b-256">コンテンツ コントロールのビジュアル化の拡張機能のいくつかのオブジェクト モデルの追加は Word 2013 で含まれます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-256">Several object model additions are included in Word 2013 for content control visualization enhancements.</span></span> <span data-ttu-id="31a1b-257">次の表は、 **ContentControl**オブジェクトのビジュアル化の新しいメンバーを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-257">The following table list new members of the **ContentControl** object for visualization.</span></span> 
  
<span data-ttu-id="31a1b-258">**表 2 になります。新しい ContentControl オブジェクトのメンバー**</span><span class="sxs-lookup"><span data-stu-id="31a1b-258">**Table 2. New ContentControl object members**</span></span>

|<span data-ttu-id="31a1b-259">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="31a1b-259">**Member**</span></span>|<span data-ttu-id="31a1b-260">**説明**</span><span class="sxs-lookup"><span data-stu-id="31a1b-260">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31a1b-261">.</span><span class="sxs-lookup"><span data-stu-id="31a1b-261"></span></span> <span data-ttu-id="31a1b-262">**WdContentControlAppearance**と**外観**</span><span class="sxs-lookup"><span data-stu-id="31a1b-262">**Appearance** as **WdContentControlAppearance**</span></span> <br/> |<span data-ttu-id="31a1b-263">コンテンツ コントロールの視覚化を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-263">Gets or sets the visualization of the content control.</span></span>  <br/> |
|<span data-ttu-id="31a1b-264">.</span><span class="sxs-lookup"><span data-stu-id="31a1b-264"></span></span> <span data-ttu-id="31a1b-265">**Wdcolor クラス**として**の色**</span><span class="sxs-lookup"><span data-stu-id="31a1b-265">**Color** as **WdColor**</span></span> <br/> |<span data-ttu-id="31a1b-266">コンテンツ コントロールの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-266">Gets or sets the color of the content control.</span></span>  <br/> |
   
<span data-ttu-id="31a1b-267">新しい**WdContentControlAppearance**列挙体の定数を次の表に一覧します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-267">The following table lists constants in the new **WdContentControlAppearance** enumeration.</span></span> 
  
<span data-ttu-id="31a1b-268">**表 3。新しい WdContentControlAppearance 列挙型定数**</span><span class="sxs-lookup"><span data-stu-id="31a1b-268">**Table 3. New WdContentControlAppearance enumeration constants**</span></span>

|<span data-ttu-id="31a1b-269">**定数**</span><span class="sxs-lookup"><span data-stu-id="31a1b-269">**Constant**</span></span>|<span data-ttu-id="31a1b-270">**説明**</span><span class="sxs-lookup"><span data-stu-id="31a1b-270">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31a1b-271">**wdContentControlBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="31a1b-271">**wdContentControlBoundingBox**</span></span> <br/> |<span data-ttu-id="31a1b-272">影付きの四角形/境界ボックスとして表示されるコンテンツ コントロールを表します (オプションとしてタイトルが表示されます)。</span><span class="sxs-lookup"><span data-stu-id="31a1b-272">Represents a content control shown as a shaded rectangle/bounding box (with optional title).</span></span>  <br/> |
|<span data-ttu-id="31a1b-273">**wdContentControlTags**</span><span class="sxs-lookup"><span data-stu-id="31a1b-273">**wdContentControlTags**</span></span> <br/> |<span data-ttu-id="31a1b-274">開始/終了マーカーとして表示されるコンテンツ コントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-274">Represents a content control shown as start/end markers.</span></span>  <br/> |
|<span data-ttu-id="31a1b-275">**wdContentControlHidden**</span><span class="sxs-lookup"><span data-stu-id="31a1b-275">**wdContentControlHidden**</span></span> <br/> |<span data-ttu-id="31a1b-276">コンテンツ コントロールが表示されないことを表します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-276">Represents a content control that is not shown.</span></span>  <br/> |
   
### <a name="code-sample"></a><span data-ttu-id="31a1b-277">コード サンプル</span><span class="sxs-lookup"><span data-stu-id="31a1b-277">Code sample</span></span>
<span data-ttu-id="31a1b-278"><a name="WordCC_VisEnhancements"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-278"></span></span>

<span data-ttu-id="31a1b-279">以下のコード サンプルは、プログラムを使用して、リッチ テキスト コンテンツ コントロールの作成と、視覚化の設定を行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31a1b-279">The following code sample shows how to create rich text content controls and set visualization programmatically.</span></span>
  
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

### <a name="xml-mapping"></a><span data-ttu-id="31a1b-280">XML マッピング</span><span class="sxs-lookup"><span data-stu-id="31a1b-280">XML mapping</span></span>
<span data-ttu-id="31a1b-281"><a name="WordCC_XMLMappingOM"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-281"></span></span>

<span data-ttu-id="31a1b-282">文書のデータ ストア内の XML ノードをリッチ テキストのマッピングに対応する Word 2013 のオブジェクト モデルに追加機能を加えていません。</span><span class="sxs-lookup"><span data-stu-id="31a1b-282">No additions were made to the Word 2013 object model to accommodate rich text mapping to XML nodes in the document data store.</span></span> <span data-ttu-id="31a1b-283">代わりに、リッチ テキスト コンテンツ コントロールを文書のデータ ストア内の XML ノードにマップするのに既存のオブジェクト モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-283">Instead, use the existing object model to map a rich text content control to an XML node in the document data store.</span></span> <span data-ttu-id="31a1b-284">さらに、XML の対応付けを具体的には新たに付属のリッチ テキスト コンテンツ コントロールのサポートの一環として開いた XML ファイル形式の WordprocessingML スキーマに変更を加えてないです。</span><span class="sxs-lookup"><span data-stu-id="31a1b-284">Additionally, no changes were made to the underlying Open XML File Format WordprocessingML schema as part of the newly included rich text content control support specifically for XML mapping.</span></span>
  
#### <a name="code-sample"></a><span data-ttu-id="31a1b-285">コード サンプル</span><span class="sxs-lookup"><span data-stu-id="31a1b-285">Code sample</span></span>

<span data-ttu-id="31a1b-286">以下のコード サンプルは、プログラムを使用して XML ノードにリッチ テキスト コンテンツ コントロールをマップする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31a1b-286">The following code sample shows how to map a rich text content control to an XML node programmatically.</span></span>
  
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

### <a name="repeating-section-content-controls-represented-in-the-object-model"></a><span data-ttu-id="31a1b-287">オブジェクト モデルで表される繰り返しセクション コンテンツ コントロール</span><span class="sxs-lookup"><span data-stu-id="31a1b-287">Repeating section content controls represented in the object model</span></span>
<span data-ttu-id="31a1b-288"><a name="WordCC_RepeatingSection"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-288"></span></span>

<span data-ttu-id="31a1b-289">繰り返しセクションのコンテンツ コントロールは、 **ContentControl**オブジェクトを新しい**RepeatingSectionItem**オブジェクトと**RepeatingSectionItemColl**オブジェクトは、以下の追加を使用してオブジェクト モデルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-289">The repeating section content control is available in the object model by using the following additions to the **ContentControl** object and the new **RepeatingSectionItem** and **RepeatingSectionItemColl** objects.</span></span> <span data-ttu-id="31a1b-290">表 4 には、繰り返しセクションのコンテンツ コントロールの**ContentControl**オブジェクトの最も重要な新しいメンバーが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-290">Table 4 lists the most important new members of the **ContentControl** object for repeating section content controls.</span></span> 
  
<span data-ttu-id="31a1b-291">**表 4 です。ContentControl オブジェクトのメンバー**</span><span class="sxs-lookup"><span data-stu-id="31a1b-291">**Table 4. ContentControl object members**</span></span>

|<span data-ttu-id="31a1b-292">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="31a1b-292">**Member**</span></span>|<span data-ttu-id="31a1b-293">**説明**</span><span class="sxs-lookup"><span data-stu-id="31a1b-293">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31a1b-294">**ブール値**として**AllowInsertDeleteSection**</span><span class="sxs-lookup"><span data-stu-id="31a1b-294">**AllowInsertDeleteSection** as **Boolean**</span></span> <br/> |<span data-ttu-id="31a1b-295">取得またはユーザーを追加したり、UI を使用してコンテンツ コントロールからセクションを削除するかどうかを設定します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-295">Gets or sets whether users can add or remove sections from the content control by using the UI.</span></span> <span data-ttu-id="31a1b-296">次のエラー メッセージが繰り返しセクションの種類ではありませんが、コンテンツ コントロールのこのプロパティを呼び出すと、呼び出しに失敗した:「このプロパティのみ使用できます繰り返しセクションのコンテンツ コントロールに」。</span><span class="sxs-lookup"><span data-stu-id="31a1b-296">If this property is called for a content control that is not of type repeating section, the call fails with the following error message: "This property can only be used with repeating section content controls."</span></span>  <br/> |
|<span data-ttu-id="31a1b-297">**文字列**として**RepeatingSectionItemTitle**</span><span class="sxs-lookup"><span data-stu-id="31a1b-297">**RepeatingSectionItemTitle** as **String**</span></span> <br/> |<span data-ttu-id="31a1b-298">取得または繰り返しセクションの項目のコンテキスト メニューで使用される名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-298">Gets or sets the name of repeating section items used in the context menu.</span></span> <span data-ttu-id="31a1b-299">繰り返しセクションの種類ではありませんが、コンテンツ コントロールのこのプロパティを呼び出すと、呼び出しに失敗した:「このプロパティのみ使用できます繰り返しセクションのコンテンツ コントロールに」。</span><span class="sxs-lookup"><span data-stu-id="31a1b-299">If this property is called for a content control that is not of type repeating section, the call fails with: "This property can only be used with repeating section content controls."</span></span>  <br/> |
|<span data-ttu-id="31a1b-300">**ContentControl**として**InsertRepeatingSectionItemBefore**</span><span class="sxs-lookup"><span data-stu-id="31a1b-300">**InsertRepeatingSectionItemBefore** as **ContentControl**</span></span> <br/> |<span data-ttu-id="31a1b-301">現在の項目の前に繰り返しセクション項目を追加し、新しい繰り返しセクション項目を返します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-301">Adds a repeating section item before the current item and returns the new repeating section item.</span></span> <span data-ttu-id="31a1b-302">繰り返しセクションの項目の種類ではありませんが、コンテンツ コントロールのこのメソッドを呼び出すと、呼び出しに失敗した:「このプロパティのみ使用できます繰り返しセクションの項目のコンテンツ コントロールに」。</span><span class="sxs-lookup"><span data-stu-id="31a1b-302">If this method is called for a content control that is not of type repeating section item, the call fails with: "This property can only be used with repeating section item content controls."</span></span>  <br/> |
|<span data-ttu-id="31a1b-303">**ContentControl**として**InsertRepeatingSectionItemAfter**</span><span class="sxs-lookup"><span data-stu-id="31a1b-303">**InsertRepeatingSectionItemAfter** as **ContentControl**</span></span> <br/> |<span data-ttu-id="31a1b-304">現在の項目の後に繰り返しセクション項目を追加し、繰り返しセクションの [新しい項目を返します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-304">Adds a repeating section item after the current item and returns the new repeating section item.</span></span> <span data-ttu-id="31a1b-305">繰り返しセクションの項目の種類ではありませんが、コンテンツ コントロールのこのメソッドを呼び出すと、呼び出しに失敗した:「このプロパティのみ使用できます繰り返しセクションの項目のコンテンツ コントロールに」。</span><span class="sxs-lookup"><span data-stu-id="31a1b-305">If this method is called for a content control that is not of type repeating section item, the call fails with: "This property can only be used with repeating section item content controls."</span></span>  <br/> |
   
<span data-ttu-id="31a1b-306">表 5 には、 **RepeatingSectionItem**オブジェクトの最も重要なメンバーが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-306">Table 5 lists the most important members of the **RepeatingSectionItem** object.</span></span> 
  
<span data-ttu-id="31a1b-307">**表 5 です。RepeatingSectionItem オブジェクトのメンバー**</span><span class="sxs-lookup"><span data-stu-id="31a1b-307">**Table 5. RepeatingSectionItem object members**</span></span>

|<span data-ttu-id="31a1b-308">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="31a1b-308">**Member**</span></span>|<span data-ttu-id="31a1b-309">**説明**</span><span class="sxs-lookup"><span data-stu-id="31a1b-309">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31a1b-310">**範囲**と**範囲**</span><span class="sxs-lookup"><span data-stu-id="31a1b-310">**Range** as **Range**</span></span> <br/> |<span data-ttu-id="31a1b-311">指定した繰り返しセクション項目を開始タグと終了タグを除外の範囲を返します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-311">Returns the range of the specified repeating section item, excluding the start and end tags.</span></span>  <br/> |
|<span data-ttu-id="31a1b-312">**Delete**</span><span class="sxs-lookup"><span data-stu-id="31a1b-312">**Delete**</span></span> <br/> |<span data-ttu-id="31a1b-313">指定の繰り返しセクションアイテムを削除します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-313">Deletes the specified repeating section item.</span></span>  <br/> |
|<span data-ttu-id="31a1b-314">**RepeatingSectionItem**と**InsertItemAfter**</span><span class="sxs-lookup"><span data-stu-id="31a1b-314">**InsertItemAfter** as **RepeatingSectionItem**</span></span> <br/> |<span data-ttu-id="31a1b-315">指定のアイテムの後に繰り返しセクション アイテムを追加し、新しいアイテムを返します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-315">Adds a repeating section item after the specified item and returns the new item.</span></span>  <br/> |
|<span data-ttu-id="31a1b-316">**RepeatingSectionItem**と**InsertItemBefore**</span><span class="sxs-lookup"><span data-stu-id="31a1b-316">**InsertItemBefore** as **RepeatingSectionItem**</span></span> <br/> |<span data-ttu-id="31a1b-317">指定のアイテムの前に繰り返しセクション アイテムを追加し、新しいアイテムを返します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-317">Adds a repeating section item before the specified item and returns the new item.</span></span>  <br/> |
   
<span data-ttu-id="31a1b-318">表 6 には、 **RepeatingSectionItemColl**オブジェクトの最も重要なメンバーが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-318">Table 6 lists the most important members of the **RepeatingSectionItemColl** object.</span></span> 
  
<span data-ttu-id="31a1b-319">**表 6 です。RepeatingSectionItemColl オブジェクトのメンバー**</span><span class="sxs-lookup"><span data-stu-id="31a1b-319">**Table 6. RepeatingSectionItemColl object members**</span></span>

|<span data-ttu-id="31a1b-320">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="31a1b-320">**Member**</span></span>|<span data-ttu-id="31a1b-321">**説明**</span><span class="sxs-lookup"><span data-stu-id="31a1b-321">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31a1b-322">**項目** **RepeatingSectionItem**として</span><span class="sxs-lookup"><span data-stu-id="31a1b-322">**Item** as **RepeatingSectionItem**</span></span> <br/> |<span data-ttu-id="31a1b-323">個々の繰り返しセクション アイテムを返します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-323">Returns an individual repeating section item.</span></span>  <br/> |
   
<span data-ttu-id="31a1b-324">表 7 は、繰り返しセクションのコンテンツ コントロールの**WdContentControlType**列挙型の新しいメンバーを示しています。</span><span class="sxs-lookup"><span data-stu-id="31a1b-324">Table 7 shows the new member of the **WdContentControlType** enumeration for repeating section content controls.</span></span> 
  
<span data-ttu-id="31a1b-325">**表 7。WdContentControlType 列挙型の加算**</span><span class="sxs-lookup"><span data-stu-id="31a1b-325">**Table 7. WdContentControlType enumeration addition**</span></span>

|<span data-ttu-id="31a1b-326">**定数**</span><span class="sxs-lookup"><span data-stu-id="31a1b-326">**Constant**</span></span>|<span data-ttu-id="31a1b-327">**説明**</span><span class="sxs-lookup"><span data-stu-id="31a1b-327">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31a1b-328">**wdContentControlRepeatingSection**</span><span class="sxs-lookup"><span data-stu-id="31a1b-328">**wdContentControlRepeatingSection**</span></span> <br/> |<span data-ttu-id="31a1b-329">1 つの繰り返しセクションに 1 つのアイテムが含まれるコンテンツ コントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-329">Represents a content control that contains a single item in a repeating section.</span></span>  <br/> |
   
### <a name="code-sample"></a><span data-ttu-id="31a1b-330">コード サンプル</span><span class="sxs-lookup"><span data-stu-id="31a1b-330">Code sample</span></span>
<span data-ttu-id="31a1b-331"><a name="WordCC_RepeatingSection"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-331"></span></span>

<span data-ttu-id="31a1b-332">以下のコード サンプルは、繰り返しセクション コンテンツ コントロールをプログラムによって使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31a1b-332">The following code sample shows how to use repeating section content controls programmatically.</span></span>
  
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

### <a name="open-xml-file-format-changes-for-repeating-section-content-controls"></a><span data-ttu-id="31a1b-333">繰り返しセクション コンテンツ コントロールにおける Open XML ファイル形式の変更点</span><span class="sxs-lookup"><span data-stu-id="31a1b-333">Open XML File Format changes for repeating section content controls</span></span>
<span data-ttu-id="31a1b-334"><a name="WordCC_RepeatingSection"> </a></span><span class="sxs-lookup"><span data-stu-id="31a1b-334"></span></span>

<span data-ttu-id="31a1b-335">繰り返しセクションのコンテンツ コントロールのファイル形式の表現一般にである、同じ要素の名前、値というように既存の XML のマークアップです。ただし、 \<sdt\>以前のバージョンの Word との互換性を確保するのには Word 2013 の名前空間に繰り返しセクションの外側のコンテナーを表す要素が存在します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-335">The file format representation of a repeating section content control generally uses the same element names, values, and so on as the existing XML markup; however, the \<sdt\> element representing the outer repeating section container exists in the Word 2013 namespace, to ensure compatibility with earlier versions of Word.</span></span>
  
<span data-ttu-id="31a1b-p124">繰り返しセクション コンテンツ コントロールによって囲まれた、内側の個々の繰り返しアイテムは、既存の WordprocessingML 表記を使用してリッチ テキスト コンテンツ コントロールとして保存されます。表 8 に、繰り返しセクション コンテンツ コントロール用 WordprocessingML スキーマの新しい要素をまとめます。</span><span class="sxs-lookup"><span data-stu-id="31a1b-p124">The individual repeating items within the repeating section content control (that surround each individual item) are saved as rich text content controls using the existing WordprocessingML representation. Table 8 lists new elements in the WordprocessingML schema for repeating section content controls.</span></span>
  
<span data-ttu-id="31a1b-338">**表 8。繰り返しセクションの WordprocessingML スキーマに新しい要素のコンテンツ コントロール**</span><span class="sxs-lookup"><span data-stu-id="31a1b-338">**Table 8. New elements in the WordprocessingML schema for repeating section content controls**</span></span>

|<span data-ttu-id="31a1b-339">**要素**</span><span class="sxs-lookup"><span data-stu-id="31a1b-339">**Element**</span></span>|<span data-ttu-id="31a1b-340">**説明**</span><span class="sxs-lookup"><span data-stu-id="31a1b-340">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31a1b-341">\<w15:repeatingSection\></span><span class="sxs-lookup"><span data-stu-id="31a1b-341">\<w15:repeatingSection\></span></span>  <br/> |<span data-ttu-id="31a1b-p125">繰り返しセクション コンテンツ コントロールを指定します。この要素は、他のすべてのコントロール タイプと互いに排他的で、子要素も子属性もありません。</span><span class="sxs-lookup"><span data-stu-id="31a1b-p125">Specifies a repeating section content control. This element is mutually exclusive with all other control types and has no child elements or attributes.</span></span>  <br/> |
|<span data-ttu-id="31a1b-344">\<w15:repeatingSectionItem\></span><span class="sxs-lookup"><span data-stu-id="31a1b-344">\<w15:repeatingSectionItem\></span></span>  <br/> |<span data-ttu-id="31a1b-p126">繰り返しセクション アイテム コンテンツ コントロールを指定します。この要素は他のコントロール タイプすべてと互いに排他的で、子要素も子属性もありません。</span><span class="sxs-lookup"><span data-stu-id="31a1b-p126">Specifies a repeating section item content control. This element is mutually exclusive with all other control types, and has no child elements or attributes.</span></span>  <br/> |
|<span data-ttu-id="31a1b-347">\<w15:doNotAllowInsertDeleteSection\></span><span class="sxs-lookup"><span data-stu-id="31a1b-347">\<w15:doNotAllowInsertDeleteSection\></span></span>  <br/> |<span data-ttu-id="31a1b-348">ユーザーが追加または Word 2013 でユーザー インターフェイスを使用してセクションを削除できないを指定します。</span><span class="sxs-lookup"><span data-stu-id="31a1b-348">Specifies that the user cannot add or delete sections by using the user interface in Word 2013.</span></span>  <br/> |
|<span data-ttu-id="31a1b-349">\<w15:sectionTitle\></span><span class="sxs-lookup"><span data-stu-id="31a1b-349">\<w15:sectionTitle\></span></span>  <br/> |<span data-ttu-id="31a1b-350">繰り返しセクション アイテムの名前を指定します (コントロールが選択されるときにコンテキスト メニューで使用されます)。</span><span class="sxs-lookup"><span data-stu-id="31a1b-350">Specifies the name of repeating section items (and is used in the context menu when the control is chosen).</span></span>  <br/> |
   

  

