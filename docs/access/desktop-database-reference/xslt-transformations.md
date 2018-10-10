---
title: XSLT 変換
TOCTitle: XSLT Transformations
ms:assetid: 6a19310d-027f-e8d6-9859-0b545ae7e2f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249418(v=office.15)
ms:contentKeyID: 48545425
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 733dd62122ee99d4e243c2af724f709a15333d51
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478219"
---
# <a name="xslt-transformations"></a>XSLT 変換


**適用されます**Access 2013 |。Office 2013

## <a name="xslt-transformations"></a>XSLT 変換

XSLT を生成された XML に適用し、別の形式に変換できます。ADO での XML 形式を理解すると、さらにユーザー フレンドリな形式に変換できる XSLT テンプレートの開発に役立ちます。

たとえば、 **Recordset** 内の各行は、rs:data 要素内の z:row 要素として保存されます。同様に、 **Recordset** 内の各フィールドは、この要素の属性と値のペアとして保存されます。

次の XSLT スクリプトを前のセクションで示した XML に適用すると、ブラウザーで表示できる HTML テーブルに変換されます。

```xml 
 
<?xml version="1.0" encoding="ISO-8859-1"?> 
<html xmlns:xsl="https://www.w3.org/TR/WD-xsl"> 
<body STYLE="font-family:Arial, helvetica, sans-serif; font-size:12pt; background-color:white"> 
<table border="1" style="table-layout:fixed" width="600"> 
  <col width="200"></col> 
  <tr bgcolor="teal"> 
    <th><font color="white">CustomerId</font></th> 
    <th><font color="white">CompanyName</font></th> 
    <th><font color="white">ContactName</font></th> 
  </tr> 
<xsl:for-each select="xml/rs:data/z:row"> 
  <tr bgcolor="navy"> 
    <td><font color="white"><xsl:value-of select="@CustomerID"/></font></td> 
    <td><font color="white"><xsl:value-of select="@CompanyName"/></font></td> 
    <td><font color="white"><xsl:value-of select="@ContactName"/></font></td>  
  </tr> 
</xsl:for-each> 
</table> 

</body> 
</html> 
```

XSLT は、ADO **Save** メソッドで生成された XML ストリームを、テーブルの見出しおよび **Recordset** の各フィールドを表示する HTML テーブルに変換します。テーブルの見出しにも行にも、異なるフォントと色が割り当てられます。

