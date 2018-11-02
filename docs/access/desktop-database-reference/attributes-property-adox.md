---
title: Attributes プロパティ (ADOX)
TOCTitle: Attributes property (ADOX)
ms:assetid: d5227b10-4a9b-5a57-d5ab-bbdd3e89aa95
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250072(v=office.15)
ms:contentKeyID: 48547959
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d39f05ecac42d416456e107b5a084797e034a0c3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931156"
---
# <a name="attributes-property-adox"></a>Attributes プロパティ (ADOX)


**適用されます**Access 2013、Office 2013。

列の属性を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

長整数型 ( **Long** ) の値を設定または返します。この値は [Column](column-object-adox.md) オブジェクトによって表されるテーブルの属性を指定し、 [ColumnAttributesEnum](columnattributesenum.md) 定数を組み合わせることができます。既定値は 0 (ゼロ) です。 **adColFixed** でも **adColNullable** でもありません。

