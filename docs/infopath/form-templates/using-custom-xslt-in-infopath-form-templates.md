---
title: InfoPath フォーム テンプレートでカスタム XSLT を使用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Microsoft InfoPath フォーム デザイナーで必要となる可能性のあるビュー要素のほとんどは作成できます。ただし、InfoPath で作成できないカスタム ビュー要素が必要な場合は、ビューを生成するために InfoPath で使用される XSL 変換 (XSLT) を手動で変更することができます。そのためには、Microsoft Office Backstage の [発行] タブの [ソース ファイルのエクスポート] を使用してフォームをそのコンポーネント ファイルに抽出し、Microsoft Visual Studio、メモ帳など任意の XML エディターで変換を編集します。
ms.openlocfilehash: a61980191dbedeec33b06ad8173ce50126fea781
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428271"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a><span data-ttu-id="4b810-105">InfoPath フォーム テンプレートでカスタム XSLT を使用する</span><span class="sxs-lookup"><span data-stu-id="4b810-105">Using Custom XSLT in InfoPath Form Templates</span></span>

<span data-ttu-id="4b810-p102">Microsoft InfoPath フォーム デザイナーで必要となる可能性のあるビュー要素のほとんどは作成できます。ただし、InfoPath で作成できないカスタム ビュー要素が必要な場合は、ビューを生成するために InfoPath で使用される XSL 変換 (XSLT) を手動で変更することができます。そのためには、Microsoft Office Backstage の [ **発行**] タブの [ **ソース ファイルのエクスポート**] を使用してフォームをそのコンポーネント ファイルに抽出し、Microsoft Visual Studio、メモ帳など任意の XML エディターで変換を編集します。</span><span class="sxs-lookup"><span data-stu-id="4b810-p102">You can create most of the view elements you're likely to need in the Microsoft InfoPath form designer. If you need a custom view element that InfoPath can't create for you, however, you can manually modify the XSL Transformation (XSLT) that InfoPath uses to generate the view. To do so, extract the form into its component files by using **Export Source Files** on the **Publish** tab of the Microsoft Office Backstage, and then edit the transform in your preferred XML editor, such as Microsoft Visual Studio or Notepad.</span></span> 
  
<span data-ttu-id="4b810-p103">InfoPath の外部でビュー変換を変更し、そのビューをデザイン モードで表示して変更すると、手動で行った変更が上書きされます。InfoPath で変更が上書きされないようにするには、次に示すように、変更した内容を変換の  `<xsl:template>` 要素に配置し、  `xd:preserve` モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="4b810-p103">If you make changes to a view transform outside of InfoPath and then open the view in design mode and make changes, InfoPath will overwrite the changes you made manually. To keep InfoPath from overwriting the changes you make, you must place those changes in an  `<xsl:template>` element in the transform and use the  `xd:preserve` mode, as shown here:</span></span> 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

<span data-ttu-id="4b810-111">変換されたファイルにテンプレートを含めるには、同じ  `<xsl:apply-templates>` モードで  `xd:preserve` 要素を使用します。</span><span class="sxs-lookup"><span data-stu-id="4b810-111">To include the template in the transformed file, use the  `<xsl:apply-templates>` element with the same  `xd:preserve` mode:</span></span> 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

<span data-ttu-id="4b810-p104">`xd:preserve` モードを使用して XSL テンプレート内に定義された要素とコンストラクトは、InfoPath デザイン環境では表示されません。その代わり、カスタム セクションは [ **コード ブロックの保持**] というラベルのコントロールとして、赤い枠でマークされます。ユーザーがフォームを開いて入力すると、カスタム XSL 変換が適用され、[ **コード ブロックの保持**] コントロールは表示されません。</span><span class="sxs-lookup"><span data-stu-id="4b810-p104">Elements and constructs defined within XSL templates with the  `xd:preserve` mode will not be displayed in the InfoPath design environment. Instead, InfoPath will mark the custom section with a control labeled **Preserve Code Block** with a red border. When a user opens the form to fill it out, the custom XSL transforms are applied and the **Preserve Code Block** controls will not appear.</span></span> 
  

