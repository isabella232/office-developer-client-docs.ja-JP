---
title: InfoPath フォーム テンプレートでカスタム XSLT を使用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Microsoft InfoPath フォーム デザイナーで必要となる可能性のあるビュー要素のほとんどは作成できます。ただし、InfoPath で作成できないカスタム ビュー要素が必要な場合は、ビューを生成するために InfoPath で使用される XSL 変換 (XSLT) を手動で変更することができます。そのためには、Microsoft Office Backstage の [発行] タブの [ソース ファイルのエクスポート] を使用してフォームをそのコンポーネント ファイルに抽出し、Microsoft Visual Studio、メモ帳など任意の XML エディターで変換を編集します。
ms.openlocfilehash: a61980191dbedeec33b06ad8173ce50126fea781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299904"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a>InfoPath フォーム テンプレートでカスタム XSLT を使用する

Microsoft InfoPath フォーム デザイナーで必要となる可能性のあるビュー要素のほとんどは作成できます。ただし、InfoPath で作成できないカスタム ビュー要素が必要な場合は、ビューを生成するために InfoPath で使用される XSL 変換 (XSLT) を手動で変更することができます。そのためには、Microsoft Office Backstage の [ **発行**] タブの [ **ソース ファイルのエクスポート**] を使用してフォームをそのコンポーネント ファイルに抽出し、Microsoft Visual Studio、メモ帳など任意の XML エディターで変換を編集します。 
  
InfoPath の外部でビュー変換を変更し、そのビューをデザイン モードで表示して変更すると、手動で行った変更が上書きされます。InfoPath で変更が上書きされないようにするには、次に示すように、変更した内容を変換の  `<xsl:template>` 要素に配置し、  `xd:preserve` モードを使用します。 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

変換されたファイルにテンプレートを含めるには、同じ  `<xsl:apply-templates>` モードで  `xd:preserve` 要素を使用します。 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

`xd:preserve` モードを使用して XSL テンプレート内に定義された要素とコンストラクトは、InfoPath デザイン環境では表示されません。その代わり、カスタム セクションは [ **コード ブロックの保持**] というラベルのコントロールとして、赤い枠でマークされます。ユーザーがフォームを開いて入力すると、カスタム XSL 変換が適用され、[ **コード ブロックの保持**] コントロールは表示されません。 
  

